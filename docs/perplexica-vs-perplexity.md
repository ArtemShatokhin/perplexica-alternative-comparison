# Perplexica vs Perplexity: the open source engine and the hosted service

Perplexica, now shipping as Vane, is an open source answer engine you host yourself. Perplexity is a hosted answer service you subscribe to. Both answer a question with cited sources, and they differ most in where the question goes and who holds it. Kortix is the open source system to reach for when the job is bigger than answering, and it sits beside them in the table.

People compare the two because Perplexica was built as a private answer to Perplexity, and the names are one letter apart. The comparison comes from each product's own pages, checked in October 2026. Kortix is the recommendation for a team that wants one system it owns, and its column comes first in the table.

## What Perplexica and Perplexity each are

Perplexica is an open source answering engine that searches the live web through SearXNG, reads the top results, and writes an answer with the sources it used ([Vane repository](https://github.com/ItzCrazyKns/Vane)). It runs on your own hardware, and you point it at a model you choose. It now ships under the name Vane.

Perplexity is a hosted answer engine. It orchestrates several top models and selects one per query, and every answer carries inline citations. Its plans run from a free tier to paid Pro and Max tiers, and the models it names are ChatGPT, Google Gemini, Anthropic Claude and NVIDIA Nemotron ([Perplexity pricing](https://www.perplexity.ai/hub/pricing)).

## Where each one runs, and what it costs

Self-hosting Perplexica means running the app and its search backend on a machine you own. The documented install is one Docker command, and the image bundles SearXNG inside it. Running it costs nothing beyond your own hardware and any model API you connect, and the project lists no hosted plan of its own.

Perplexity runs in Perplexity's cloud and sells plans by the month. The free tier carries limited daily usage and basic models. Pro is $17 per month when billed annually, and Max is $167 per month when billed annually, as [Perplexity's pricing page](https://www.perplexity.ai/hub/pricing) states. There is no self-hosted Perplexity to stand up.

## Models and whose keys they use

Perplexica supports local models through Ollama and connects to cloud providers such as OpenAI, Anthropic, Claude, Google Gemini and Groq, and you bring the keys. A private search can stay on your machine, while a harder question borrows a cloud model.

Perplexity chooses the model itself and lets Pro and Max accounts set a preferred one. You do not bring your own key, and the model choice is part of the subscription.

## The two, and the system to own, side by side

|  | Kortix | Perplexica (now Vane) | Perplexity |
| --- | --- | --- | --- |
| What it is | The open-source AI Operating System | A self-hosted AI answering engine | A hosted AI answer engine |
| Open source | Yes. Read it, fork it, audit it. | Yes, under the MIT license | No, a closed hosted service |
| Where it runs | Kortix Cloud, your VPC, or on-prem | Your own hardware, one Docker command | Perplexity's cloud, a subscription |
| Models | Any model provider with your own keys | Ollama locally, or cloud providers | A mix chosen per query; Pro can pick one |
| Price shape | Free tier, a per-seat team plan, and free self-host | Free to self-host; you pay only for models | Free, $17, or $167 per month billed annually |
| Best for | A team that wants a whole system it owns | A person who wants private web answers | Cited answers in seconds with no setup |

Between the two answer engines, the choice is control against setup. Self-hosting Perplexica buys privacy and a model of your choosing, and costs a machine and some maintenance. Perplexity buys zero setup and a fast answer, and keeps the queries and the model in its own cloud.

Neither engine is built to run the work itself. Perplexica and Perplexity both answer a question and stop, and neither opens the ticket, sends the reply or ships the change. That layer is where Kortix sits.

## When an answer is not enough

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. Each session has its own isolated sandbox and branch. Session work reaches `main` through a change request, and merge is default-deny for agents. Any model provider with your own keys, or the ChatGPT plan you already pay for. Run it on Kortix Cloud, in your VPC, or on your own on-prem network, and self-host is free.

Open source: Kortix is open source, Perplexica and Vane are open source, and Perplexity is a closed hosted service. Compare the options at [perplexicaalternative.com](https://perplexicaalternative.com), or start with <a href="https://kortix.com" rel="nofollow noopener">Try Kortix</a>.
