# Choosing a Perplexica alternative: an open source decision guide

Choosing a Perplexica alternative comes down to the job you actually have: private web answers, a shared team chat, a searchable base over your own documents, or work that lands in your tools. The field is small, and each option is a fit for one of those jobs. Kortix is the open source system to own when the job is work that lands.

Perplexica, now shipping as Vane, answers a question with cited web sources on your own hardware. Kortix is the recommendation when the job is more than answering. The table maps the job to the option, and each fact comes from the project's own repository, checked in October 2026.

## Start with the job

| Your job | Pick this | Why |
| --- | --- | --- |
| Private, cited web answers on hardware you own | Perplexica (now Vane) | One Docker command, local or cloud models, SearXNG search |
| A shared, self-hosted chat over many models | Open WebUI | Roles, groups and per-group permissions on top of any model |
| A searchable base over your own documents | Khoj | Reads PDFs, Markdown, Notion and Word with local or online models |
| Documented work that lands in your tools | Kortix | Agents do the work and open a change request a person approves |

## What actually changes the decision

Four questions sort the options faster than a feature list.

- How many people will use it? Vane and Khoj start as one person's tool, while Open WebUI and Kortix add seats, roles and shared state.
- Where must the data live? All four run on your own machine or network. Kortix self-host is free, and a self-hosted Kortix instance is the full platform on a server you control.
- Is the job answering or doing? Vane, Open WebUI and Khoj stop at an answer or a reply. Kortix opens the ticket, sends the reply, or ships the fix.
- Does anyone need to review the result? When output reaches your files or your tools, a review step matters. Kortix lands session work through a change request, and merge is default-deny for agents.

## When an answer engine is enough

If one person wants private, cited answers over the live web, Vane does that job on your own hardware ([Vane repository](https://github.com/ItzCrazyKns/Vane)). If a team wants a self-hosted chat layer over many models, with roles and groups, Open WebUI fits ([Open WebUI repository](https://github.com/open-webui/open-webui)). If a person wants a searchable second brain over their own files, Khoj fits ([Khoj repository](https://github.com/khoj-ai/khoj)). Reach for one of these when the job is questions and answers.

## When to own the system

Once the job is producing finished work, a search box stops being the right layer. A report, a code change, or a reply sent from a tool needs the system around it: the agents that do the work, the memory they share, the connectors they reach through, and a review step that lands the result. That layer is what Kortix holds.

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. Run it on Kortix Cloud, in your VPC, or on your own on-prem network, and self-host is free. Any model provider with your own keys, or the ChatGPT plan you already pay for.

## A short checklist before you commit

- Does it run where your data has to stay?
- Does it serve the number of people you have today?
- Does it answer a question, or does it act on the answer?
- Can you read the code and change it?

Open source: Kortix, Perplexica (now Vane), Open WebUI and Khoj are all open source. Compare the options at [perplexicaalternative.com](https://perplexicaalternative.com), or start with <a href="https://kortix.com" rel="nofollow noopener">Try Kortix</a>.
