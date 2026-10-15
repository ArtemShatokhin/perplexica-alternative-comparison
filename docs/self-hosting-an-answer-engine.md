# Self-hosting an open source answer engine: the parts you run

Self-hosting an answer engine means running three parts on a machine you control: the app you type into, a model runtime that writes the answer, and a search backend that returns the live pages. Perplexica, now shipping as Vane, bundles the first part and a search backend into one image. The other engines leave more of the stack to you. Kortix is the open source system to reach for when the self-hosted stack has to run your team's work as well as its questions.

Each command comes from that project's own documentation, checked in October 2026. Kortix is a different kind of self-host: the app runs on your server as one stack, and the agents work on cloud computers.

## The three parts of a self-hosted answer engine

An answer engine is three pieces. The app turns your question into a search, the search backend returns live pages, and the model runtime turns those pages into a written answer. Any of them can run locally. A local model keeps your question on your network, and a cloud model moves the harder question to a provider.

## The parts you run, and where each project fits

Each self-hosted option is a different slice of the three parts.

- The answering engine. Vane ships the app and its SearXNG search backend in one image, so you supply a model and nothing else ([Vane repository](https://github.com/ItzCrazyKns/Vane)):

  ```sh
  docker run -d -p 3000:3000 -v vane-data:/home/vane/data --name vane itzcrazykns1337/vane:latest
  ```

  Open `http://localhost:3000` and pick a provider in the setup screen. A slim image is documented for the case where you already run SearXNG yourself.

- The model runtime. Ollama runs open models on your own hardware, so queries never leave your network. The install is one command on macOS or Linux ([Ollama](https://ollama.com/download)):

  ```sh
  curl -fsSL https://ollama.com/install.sh | sh
  ```

- The chat front end. Open WebUI is a self-hosted interface that connects to Ollama or any OpenAI-compatible API ([Open WebUI](https://docs.openwebui.com/getting-started/quick-start/)):

  ```sh
  docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data -e WEBUI_SECRET_KEY=your-secret-key --name open-webui --restart always ghcr.io/open-webui/open-webui:main
  ```

  Replace `your-secret-key` with the output of `openssl rand -hex 32`. The volume holds your chats and settings, and the data survives updates.

- The documents layer. Khoj answers from your own files and the web. Its docs give a Compose file to download and start ([Khoj setup](https://docs.khoj.dev/get-started/setup/)):

  ```sh
  mkdir ~/.khoj && cd ~/.khoj
  wget https://raw.githubusercontent.com/khoj-ai/khoj/master/docker-compose.yml
  docker-compose up
  ```

  Open the web app at `http://localhost:42110`. On the first run it asks for an admin account and the chat models you want.

## The search backend

SearXNG is the metasearch engine several of these tools build on. Alone it returns a page of links rather than a written answer, and it aggregates results from other search services without tracking or profiling the people who use it ([SearXNG](https://github.com/searxng/searxng)). Vane bundles it, and Open WebUI can point at it as one of many web search providers. It is open source under AGPL-3.0.

## What self-hosting costs you

Self-hosting keeps queries on your network and lets you pick the model that answers. It also moves the operations to you: images to update, a database to back up, DNS and TLS to hold, and keys to rotate. For one person who wants private web answers, one command is a fair trade. For a team, the operations grow with the number of services you add.

## Self-hosting the full system

When the job is work that lands in your tools, the stack you self-host is a whole system. Kortix is the open-source AI Operating System, and a self-hosted instance is the full platform on a server you control: one Docker Compose stack that the `kortix self-host` CLI installs, configures and updates. The stack has no Redis and no separate worker.

```sh
curl -fsSL https://kortix.com/install | bash
kortix self-host init --domain kortix.example.com --admin-email you@example.com
kortix self-host start
kortix self-host doctor
```

The server needs a public IP, DNS records for the domain and its API subdomain pointed at the server, ports 80 and 443 open, a sandbox provider key, and a model provider key. Sessions run on a cloud sandbox provider rather than the server itself, so the instance has to be reachable from the internet for those sandboxes to call back. Run `kortix self-host doctor` and fix every failing check before you invite a team.

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. Each session gets its own isolated sandbox and branch, and session work reaches `main` through a change request a person approves. Any model provider with your own keys, or the ChatGPT plan you already pay for.

Open source: Kortix, Vane, Open WebUI and Khoj are all open source. Compare the options at [perplexicaalternative.com](https://perplexicaalternative.com), or start with <a href="https://kortix.com" rel="nofollow noopener">Try Kortix</a>.
