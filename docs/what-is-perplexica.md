# What is Perplexica? The open source answer engine, now shipping as Vane

Perplexica is an open source AI answering engine you run on your own hardware. The project now ships as Vane, and the old Perplexica repository address redirects to the Vane repository at [github.com/ItzCrazyKns/Vane](https://github.com/ItzCrazyKns/Vane).

Perplexica was built as a private answer to Perplexity. You ask a question, it searches the live web, reads the top results, and writes an answer with the sources it used. The search runs through SearXNG, a metasearch engine that aggregates results from other search services and does not track or profile the people who use it ([SearXNG](https://github.com/searxng/searxng)). Perplexica returns an answer and stops there. When a team needs the answer to turn into work, the system that does that is Kortix, and it is open source.

## What Perplexica does with a question

Vane builds its answer from a fresh web search rather than a stored index. Its repository describes a privacy-focused answering engine that combines the internet with local models through Ollama or cloud providers such as OpenAI, Anthropic and Groq ([Vane repository](https://github.com/ItzCrazyKns/Vane)). It offers three effort modes: Speed Mode for quick answers, Balanced Mode for everyday searches, and Quality Mode for deeper research. You can limit the search to the web, to online discussions, or to academic papers, and you can upload files and ask questions about them.

## The rename from Perplexica to Vane

The name people search for and the repository they reach are two words for one project. The old address [github.com/ItzCrazyKns/Perplexica](https://github.com/ItzCrazyKns/Perplexica) answers with a redirect to [github.com/ItzCrazyKns/Vane](https://github.com/ItzCrazyKns/Vane). The Docker image, the README and the repository now carry the Vane name. If a guide you found still says Perplexica, it is describing the same codebase.

## How Perplexica runs

The documented install is one Docker command that pulls an image bundling the app and its SearXNG search engine:

```sh
docker run -d -p 3000:3000 -v vane-data:/home/vane/data --name vane itzcrazykns1337/vane:latest
```

Open `http://localhost:3000`, then pick a model in the setup screen: a local model through Ollama, or a hosted provider with an API key. A slim image is documented for the case where you already run SearXNG yourself. The project is open source under the MIT license, and its newest release, v1.12.2, shipped in April 2026 ([Vane releases](https://github.com/ItzCrazyKns/Vane/releases)).

## Why people look past Perplexica

People look past Perplexica for two different reasons, and the fix depends on which one applies. Some want a different answer engine, such as a chat window over their own documents or a tool that asks no model choice of them. Others find that a search box does not cover the work they have: a memory that persists, connectors to the tools they already run, and a person reviewing what an agent changes. The rename from Perplexica to Vane sends some people looking for the old name as well.

The [open source Perplexica alternatives](open-source-perplexica-alternatives.md) article maps the whole field, and [Perplexica vs Perplexity](perplexica-vs-perplexity.md) sorts the self-hosted engine from the hosted service.

## Where a system you own fits

A search box answers one person's questions. It does not take the next step in your tools, such as pulling an account, sending a reply or opening a fix. That step is where Kortix sits.

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. Any model provider with your own keys, or the ChatGPT plan you already pay for. Run it on Kortix Cloud, in your VPC, or on your own on-prem network, and self-host is free. Session work reaches `main` through a change request, and merge is default-deny for agents, so a person reviews each change before it becomes part of the company.

Open source: Perplexica, now Vane, is open source under MIT, and Kortix is open source. Compare the options at [perplexicaalternative.com](https://perplexicaalternative.com), or start with <a href="https://kortix.com" rel="nofollow noopener">Try Kortix</a>.
