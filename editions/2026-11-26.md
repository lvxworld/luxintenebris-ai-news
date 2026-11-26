# Lux in Tenebris — AI dispatches · November 26, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 154 · https://luxintenebris.news/

## Lead Privacy, productized: OpenAI begins testing Private Inference for enterprise customers

Sam Altman said OpenAI is testing Private Inference with a small group of customers as part of a new Private Intelligence offering, aimed at stronger privacy protections so that frontier models can be used for more of the work enterprises have kept off-limits. No pricing, capacity or broader availability details were disclosed.

Source: [Sam Altman (X)](https://x.com/sama/status/2125638790593274259)

## Top stories

### Anthropic moves its production Messages API from Python to Rust

Anthropic rewrote the path customers, Claude Code and Cowork use to reach Claude, using the live Python service as a verifier on production traffic and dispatching teams of Claude agents to hunt down behavioural divergences. The Rust API uses about 70% less CPU per request and cuts median time to first token by roughly 20%, with no downtime or feature freeze.

Source: [Anthropic](https://www.anthropic.com/research/migrating-api-to-rust)

### Epochal launches with $100M to train predictive AI models

Three ex-xAI founders launched Epochal with $100M funded directly by CEO Guodong Zhang rather than a VC round. Its flagship is the Epochal Time Portal, a 1-trillion-page timestamped web archive used to backtest forecasting models.

Source: [SiliconANGLE](https://siliconangle.com/2026/11/24/epochal-launches-with-100m-to-help-developers-train-predictive-ai-models/)

### DeepMind skills let Gemini interpret mass spectra and name the molecule

Mass Spec Skills for Google Antigravity lets Gemini drive established mass-spectrometry tools and query public chemical databases to lay out the chemical evidence behind a reading. Built with analytical chemists, it identifies and verifies the exact molecule in roughly 97% of attempts, even with a lightweight model driving it.

Source: [Google DeepMind](https://deepmind.google/blog/interpreting-mass-spectra-with-google-antigravity/)

## Research & Papers

- **[Coding agents out-reason video models on visual tasks when they write code](https://arxiv.org/abs/2611.34813)** — On VBVR-Pro-Bench, agents that write programs to render the answer video scored 0.923, 0.894 and 0.893 — each more than 0.22 above the strongest video generation model. The best open-weight agent, GLM-5, reached 0.572. *(arXiv)*
- **[Kolpona lifts chip design pass rates with gradient-free neuron programming](https://arxiv.org/abs/2611.33973)** — Editing single neurons in closed form plus a tool-using agent raises Qwen3.5-4B VerilogEval v2 pass@1 from 31.7% to 55.4%, and to 77.6% with the full framework. On Qwen3.8-27B it goes from 73.1% to 94.9% on a single 32 GB GPU. *(arXiv)*
- **[Maco-RL stabilises mixed-task RL and adds 10.6 points to a 27B model](https://arxiv.org/abs/2611.34703)** — A quota-based asynchronous rollout scheduler with Tri-Buffer Sampling raises Qwen3.5-27B's overall score from 43.6 to 54.2 across five benchmarks, and to 60.1 once training expands continually across domains. *(arXiv)*
- **[Drone agents invoke lethal tools on generic descriptors, no jailbreak needed](https://arxiv.org/abs/2611.34121)** — In a simulated perception-action pipeline over real drone imagery, several LLMs called a simulated lethal tool for ordinary descriptors like 'people'. Agents that looked conservative under protected wording turned unsafe after a simple semantic target shift. *(arXiv)*
- **[Puzzling-Bench: 23,777 human-written puzzles with author-verified answers](https://huggingface.co/papers/2611.34331)** — Drawn from the Puzzling Stack Exchange archive, the benchmark puts the best model, GPT-6.1, at 74.8% on a shared 255-puzzle set. Seventeen puzzles defeat all nine tested models, an oracle over all nine reaches 91%, and withholding images costs the two best models 24 and 35 points. *(Hugging Face)*

## Open Source & Models

- **[Sakana's 30B Namazu Small beats Nvidia's 120B Nemotron on average](https://sakana.ai/namazu-small/)** — Sakana AI built a 30B reasoning model on Nvidia's open Nemotron 3 Nano base and, across 25 benchmarks, beat both Nemotron 3 Nano and the 120B-A12B Nemotron 3 Super on average score. The gaps are widest in web research (BrowseComp 73.5 versus 36.1) and long-document grounding; internal-knowledge tasks lag, and on-premises availability is promised for early-to-mid December. *(Sakana AI)*
- **[Nvidia ships an autoregressive image model that writes pixels as tokens](https://huggingface.co/nvidia/Nemotron-Labs-Image-30B-A3B)** — Nemotron-Labs-Image-30B-A3B is a 30B-A3B MoE built on Nemotron 3 Nano that generates images as discrete visual tokens, decoded by a separate 642M tokenizer with a 196K-vector codebook. Standalone it scores 94.30 on LongTextBench versus 96.00 for GPT Image 2, rising to 97.98 only when a GPT-6 planner picks candidates; the weights carry a non-commercial research licence. *(Nvidia (Hugging Face))*
- **[Baidu releases ERNIE 5.5 Flash Preview weights under Apache 2.0](https://technode.com/2026/11/25/baidu-opens-ernie-5-5-flash-preview-weights-with-million-token-context/)** — The 280B total / 14B active hybrid-attention MoE with a 1M-token context is now a free download on Hugging Face and ModelScope, in FP8 and BF16 with vLLM and SGLang support. It is the largest permissively licensed Chinese open-weight drop of the week, delivered after the weights were promised at the November 11 API launch. *(TechNode)*
- **[A 24 KB x86-64 OS runs Qwen3-0.6B with no Linux, no libc](https://github.com/alesha-pro/llm.asm/tree/main/02-baremetal-os)** — A bootable 24,252-byte Multiboot kernel runs a Qwen3-0.6B chat loop entirely in assembly: 74-94 ms cold boot to an interactive prompt, persistent multi-turn KV cache and SMP scaling to 32 vCPUs at 134.9 tok/s decode. It boots from a 661 MiB ISO into a zero-disk VM. *(GitHub (alesha-pro/llm.asm))*

## YouTube & Video

- **[Anthropic Opus 5.6 leak points to a step-change in capability](https://www.youtube.com/watch?v=64hGi-04Mx8)** — A leak circulating in AI coverage suggests Anthropic's next flagship delivers a materially higher level of intelligence than current frontier models. Details remain unconfirmed by Anthropic. *(YouTube — Beyond AI News)*
- **[US Genesis Mission looks to AI to accelerate science](https://www.youtube.com/watch?v=4cEm4-3wUUk)** — Bloomberg Technology examines the Genesis Mission, a US government initiative betting on AI to speed up scientific discovery. The programme frames AI as national research infrastructure rather than a commercial product. *(YouTube — Bloomberg Technology)*

## Tools & Startups

- **[Cloudflare launches Search for Agents](https://blog.cloudflare.com/search-for-agents/)** — A dashboard toggle auto-creates an AI Search index for a zone and exposes a QUERY API at /.well-known/search, advertised on every page so agents can discover it. It is available to all customers including Free, billed under AI Search pricing. *(Cloudflare Blog)*
- **[Vercel's Workflow SDK 5.8 rebuilds its execution engine](https://vercel.com/changelog/workflows-speculative-execution)** — Step-to-step latency drops from 85ms to 7ms, overhead for 256 parallel steps falls about 14x, and idempotent steps can now run speculatively. Vercel pitches the change as a direct improvement to turn times for durable agents. *(Vercel)*
- **[Together AI open-sources Hurdle for agent evaluations](https://www.together.ai/blog/introducing-hurdle-run-agent-evals-on-your-api-skills-and-docs)** — Hurdle is an npm library that runs Claude Code and Codex against real tasks on your own API, docs and skills, scoring runs with code checks, guards that block bad actions and an LLM judge. It supports per-model comparisons and repeat runs for pass rates, and installs with npx hurdle init. *(Together AI)*
- **[Sand AI's MAGI-2 scales its video model to 480B parameters](https://www.producthunt.com/products/magi-1)** — The video backbone goes from 114B to 480B total parameters (~28B active) on about 4T tokens, generating up to 30 seconds of 1080p 25fps audio-video with up to 20 omni-reference assets and timeline control. Sand AI says open-source releases and a technical report will follow. *(Product Hunt)*

## Italia AI Spotlight

- **[MinervaE goes live: Italy's public open model now reasons before answering](https://www.ai4business.it/intelligenza-artificiale/coding/minervae-il-nuovo-modello-italiano-di-ai-aperto-e-pubblico/)** — Sapienza's NLP group and its spin-off Babelscape released a 20-billion-parameter MoE that activates roughly 3 billion parameters per query, trained on Cineca's Leonardo supercomputer across all European languages. It runs in preview at chatminerva.org, positioned as a public, open alternative to foreign frontier models. *(AI4Business)*
- **[Angelini Technologies takes a stake in humanoid maker Oversonic](https://www.economyup.it/innovazione/oversonic-angelini-technologies-investe-sugli-umanoidi-ed-entra-nella-startup-di-robee/)** — Angelini Technologies entered the cap table of the Brianza company behind the cognitive humanoid RoBee to fund production scale-up and US expansion, with terms undisclosed. It follows STMicroelectronics and others joining in June and adds three board members. *(EconomyUP)*
- **[Italy's CNEL adopts a position paper on physical AI and robotics](https://www.innovationpost.it/attualita/politica/physical-ai-e-robotica-dal-cnel-un-documento-per-governare-limpatto-su-imprese-e-lavoro/)** — The National Council for Economics and Labour approved observations and proposals on governing physical AI in the productive system, requested by industry minister Adolfo Urso. It covers competitiveness, employment, skills, industrial relations and pension sustainability after seven hearings with about a hundred companies, institutions and unions. *(Innovation Post)*
- **[MassimarIA opens a searchable archive of 900,000 tax court rulings](https://www.startup-news.it/massimaria-archivio-giurisprudenza-tributaria/)** — The Italian startup's platform indexes first- and second-instance tax courts plus the Supreme Court, tagging each ruling with its legal principle, outcome, applied provisions and cited precedents. It traces every citation back to a consulted source. *(Startup-News)*

## Money & Markets

- **[Bound secures $50M to push FX risk management down-market](https://tech.eu/2026/11/25/bound-secures-50m-to-advance-fx-risk-management-for-mid-market-companies/)** — The three-year debt facility from Viola Credit is not equity, and follows a $24.5M Series A led by AlbionVC in February. London-based Bound sells AI-driven currency risk automation to mid-market treasuries. *(Tech.eu)*
- **[elbic raises €2.7M for sovereign European voice AI](https://www.eu-startups.com/2026/11/yc-backed-elbic-raises-e2-7-million-to-keep-european-customer-calls-off-us-servers-with-sovereign-voice-ai/)** — The pre-seed was led by Repeat Ventures with Rebel Fund, Y Combinator and German angels. Berlin-based elbic, formerly KugelAudio, builds in-house speech-to-speech models for telcos and contact centres that want call data kept off US servers. *(EU-Startups)*
- **[Fault Line raises £2.3M to give clinical AI its cybersecurity moment](https://techfundingnews.com/fault-line-raises-2-3m-clinical-ai-safety-benchmarks/)** — The pre-seed was co-led by Concept Ventures and Frontline Ventures for the London company, which builds independent safety benchmarks and assurance for clinical AI. The founding trio came out of Limbic. *(Tech Funding News)*
- **[Jiutian Chuangzhi raises nearly RMB 100M to scale outdoor robots](https://techstartups.com/2026/11/25/startup-funding-news-today-november-25-2026-zipher-peak-energy-atomqubic-dante-security-more/)** — The Series A came from Yidao Capital, Qingke Industrial Investment and Nanshan Strategic Emerging Industry Investment. The Shenzhen company's autonomous outdoor cleaning robots are deployed in about 100 cities across 20-plus countries. *(Tech Startups)*
