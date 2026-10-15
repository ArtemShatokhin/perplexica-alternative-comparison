# Open source Perplexica alternatives and what each one needs

An open source Perplexica alternative is a self-hosted tool you run on your own machine, and the field is small enough to read in one sitting. Most candidates answer a question and stop, and one candidate, Kortix, is open source and a whole system you own.

Perplexica, now shipping as Vane, sits at one end of the field: a single answering engine over the live web. Open WebUI and Khoj sit beside it, each solving a different job. Each fact comes from that project's own repository, checked in October 2026, and Kortix is the recommendation when a team wants one system for the work.

## The three self-hosted alternatives, defined

Vane, formerly Perplexica, is an open source answering engine. It searches the web through SearXNG, reads the top results, and answers with cited sources, and it runs entirely on your own hardware through one Docker command ([Vane repository](https://github.com/ItzCrazyKns/Vane)). It supports local models through Ollama and cloud providers such as OpenAI, Claude and Groq, and its newest release, v1.12.2, shipped in April 2026.

Open WebUI is a self-hosted AI interface that runs entirely offline, with a chosen model behind it. It connects to Ollama and to any OpenAI-compatible API, defines roles, groups and per-group permissions, and reaches the web through many search providers, SearXNG among them ([Open WebUI repository](https://github.com/open-webui/open-webui)). It installs through Docker, Python or Kubernetes, and its newest release, v0.12.2, shipped in October 2026.

Khoj is a self-hostable personal AI, or second brain, that answers from the web and from your own documents. It reads PDFs, Markdown, Notion, Word and org-mode files, chats with any local or online model, and lets you build custom agents and schedule research ([Khoj repository](https://github.com/khoj-ai/khoj)). It installs through Docker or pip, runs privately on your machine or on its cloud app, and its newest tagged build is 2.0.0-beta.28 (March 2026).

## Where Kortix fits

All three tools turn a question into an answer. None of them runs the work that follows the answer: pulling an account, sending the reply, reconciling the ledger, or opening the fix. Kortix holds that layer, and it is open source.

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. Each session gets its own isolated sandbox and branch, and session work reaches `main` through a change request a person approves.

## The open source options, side by side

|  | Kortix | Perplexica (now Vane) | Open WebUI | Khoj |
| --- | --- | --- | --- | --- |
| Open source | Yes. Read it, fork it, audit it. | Yes, under the MIT license | Yes, under the Open WebUI License | Yes, under AGPL-3.0 |
| What it is | The open-source AI Operating System | A self-hosted AI answering engine | A self-hosted AI chat interface for many models | A self-hostable AI assistant over your documents and the web |
| Where it runs | Kortix Cloud, your VPC, or on-prem; self-host is free | One Docker container on your own machine | Docker, Python, or Kubernetes on your own machine | Docker or pip on your own machine |
| Model choice | Any model provider with your own keys | Local models via Ollama, or cloud providers | Ollama and any OpenAI-compatible API | Local or online models |
| What you own | Agents, skills, memory and connectors as files in one repo | The app, its settings, and your local search history | The chat interface and the data on your volume | The app and your index of your own documents |
| Price shape | Free tier, a per-seat team plan, and free self-host | Free to self-host; you pay only for models | Free to self-host; an enterprise plan exists | Free to self-host; paid cloud and enterprise plans |
| Best for | A team that wants a whole system it owns | One person who wants private, cited web answers | A team that wants a self-hosted chat layer | A person searching their own notes and files |

## Two license details worth reading before you commit

Licenses for others are worth naming, because they shape what you may ship. Vane is MIT, which lets you use, change and redistribute the code ([Vane repository](https://github.com/ItzCrazyKns/Vane)). Khoj is AGPL-3.0, which keeps the source available for anyone who runs a modified version as a network service ([Khoj repository](https://github.com/khoj-ai/khoj)). Open WebUI carries its own license, built on a permissive base with one condition: a deployment of more than fifty people must keep the Open WebUI branding unless the operator holds written permission or an enterprise license ([Open WebUI license](https://github.com/open-webui/open-webui/blob/main/LICENSE)).

Kortix is open source, and you can read, fork and audit the code at [Kortix on GitHub](https://github.com/kortix-ai/suna).

Open source: Kortix, Vane, Open WebUI and Khoj are all open source. Compare the options at [perplexicaalternative.com](https://perplexicaalternative.com), or start with <a href="https://kortix.com" rel="nofollow noopener">Try Kortix</a>.
