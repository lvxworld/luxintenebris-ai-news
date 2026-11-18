# Lux in Tenebris — AI dispatches · November 18, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 146 · https://luxintenebris.news/

## Lead Frontier Release: OpenAI ships GPT-6.2 in two flavours, Astra and Sol

OpenAI released GPT-6.2 Astra, a frontier model for its hardest professional, scientific, visual and engineering work, alongside GPT-6.2 Sol, a cheaper model tuned for everyday use and multistep agentic workflows. Both are live in ChatGPT Work, Codex and the API, and OpenAI says they reach better results while emitting fewer output tokens.

Source: [OpenAI](https://openai.com/index/introducing-gpt-6-2-astra-sol/)

## Top stories

### Nvidia names CFO Colette Kress interim CEO and reaffirms its open-model strategy

Nvidia's board installed finance chief Colette Kress as interim chief executive after Jensen Huang's departure. On her first earnings call in the role, Kress said the company remains committed to a vibrant open-model ecosystem and that the $12.9 billion Hugging Face acquisition agreed in September is still on track, citing 35x year-over-year growth in weekly OpenRouter token volume.

Source: [TechCrunch](https://techcrunch.com/2026/11/17/nvidia-says-its-open-source-ai-strategy-remains-intact-after-jensen-huangs-exit/)

### Isomorphic Labs raises $5B Series C to push AI-designed drugs into trials

The Alphabet-linked drug discovery company closed a $5 billion Series C co-led by Sequoia Capital and Greenoaks, with Andreessen Horowitz, Thrive Capital, Alphabet, GV, CapitalG and Temasek participating. The round lands six months after a $2.1 billion Series B and funds scaling of its IsoDDE design engine and the move of therapeutic candidates into clinical trials.

Source: [Tech.eu](https://tech.eu/2026/11/17/sequoia-and-greenoaks-lead-massive-5bn-series-c-funding-round-in-isomorphic-labs/)

### Google renames its Spark agent to Tasks and gives it away free

Google renamed the Spark agent inside the Gemini app to Tasks and opened it to free users in the US, Canada, Japan, Korea, Australia and India, dropping the AI Pro and Ultra requirement. Running on Gemini 4 Hydrogen, it can call businesses to compare prices, buy with Google Pay and take work by email inside a per-account isolated VM.

Source: [The Verge](https://www.theverge.com/tech/1035756/google-spark-ai-tasks-free)

## Research & Papers

- **[K2-Horizon: a frontier fleet of open source language models](https://huggingface.co/papers/2611.21003)** — Six fully open models from 0.9B dense up to a 375B-A23B MoE, leading or matching open models of their size on agentic and coding benchmarks. The work introduces Mixture-of-Value Attention and softplus attention gating, where a 36B-A4B model nearly matches a 32B dense model at one-seventh the active parameters, plus lossless diffusion adapters that speed decoding up to 2.2x without a draft model. *(Hugging Face)*
- **[ScaleVLA scales vision-language-action models to 552B parameters](https://huggingface.co/papers/2611.21607)** — Connects a 552B DeepSeek-V4.1-Flash backbone to a trainable action DiT and compares VLMs from 2B to 552B under one training setup. Ten demonstrations beat a 2B backbone trained on 50 (87.8% vs 85.6%), LIBERO-PRO success reaches 45.1% against at most 31.3% for smaller backbones, and real-world charger insertion improves from 4/10 to 9/10. *(Hugging Face)*
- **[Higher-scoring coding models did not get more work done](https://arxiv.org/abs/2611.23216)** — Uses the 19-day suspension of Claude Fable 5 as a natural experiment across 297 of its users, with 8,908 developers who stayed on Opus 4.8 as controls. Access to the stronger model raised the 7-day PR merge rate by only 1.4 points, not statistically significant, and five model upgrades in 2026 produced a weighted mean of -0.9 points. *(arXiv)*
- **[What RL on expert-built tasks teaches Nemotron 3.5 Super](https://arxiv.org/abs/2611.22161)** — Post-trains Nemotron 3.5 Super, at 120B total and 12B active parameters, with rank-32 LoRA adapters using CISPO on five expert-built task datasets one at a time, with no supervised stage. Gains run from +4.5 points on IFBench to +13.8 on GDP_pdf, SWE-bench Pro V2 rises from 86.9% to 92.1% and AutomationBench from 14.8% to 27.5%. *(arXiv)*
- **[RSI-Prime: training models to train models](https://arxiv.org/abs/2611.23138)** — Builds 350 complete experimental trajectories across seven task categories to improve LLM model-training capability, with decision-level annotation and loss masking. On PostTrainBench, training GLM-5.3 on RSI-Prime yields a 31.95% relative improvement in overall performance over the original model. *(arXiv)*

## Open Source & Models

- **[OVHcloud releases Olala mini 7A1B, its first in-house model family](https://corporate.ovhcloud.com/en/newsroom/news/ovh-olala-mini/)** — Trained from scratch on three European public supercomputers, Jupiter, MeluXina and Jean Zay, on roughly EUR 7 million of compute. The 7B model runs 1B active parameters across 256 experts per layer and hits 160 tokens per second on an RTX A4500, with Apache 2.0 weights, a technical report and AI Act compliance documents shipping alongside. *(OVHcloud)*
- **[vLLM v0.34.0 removes Model Runner V1 and sizes the KV cache from free memory](https://github.com/vllm-project/vllm)** — The release lands 1,061 commits from 412 contributors and sizes the KV cache from memory actually free after warmup, so most models get a larger cache by default. Model Runner V2 becomes the path forward and ten new architectures are supported, including Mistral Large 4 and Nemotron-3.5-Transcribe. *(GitHub)*
- **[NVIDIA ships SkillEvaluator v1.0.1 as the repo climbs GitHub trending](https://github.com/NVIDIA/SkillEvaluator)** — NVIDIA's framework for grading agent skills moved to v1.0.1 a day after v1.0.0 while gaining about 950 stars in a day. It bundles quality gates, semantic overlap detection, synthetic evaluation set generation and live evaluation of how a skill changes agent behaviour, plus token and cost budgets. *(GitHub)*

## Tools & Startups

- **[OpenAI launches ChatGPT for Sales with more than 30 new partner plugins](https://openai.com/index/introducing-chatgpt-for-sales/)** — A Sales plugin for ChatGPT aimed at prospect research, pitch preparation and CRM updates, launched alongside a wider batch of partner plugins. OpenAI says the experience is designed to shorten the cycle from finding accounts to following through on commitments. *(OpenAI)*
- **[Perplexity Computer adds Multiagent with up to 16 cross-checking agents](https://www.marktechpost.com/2026/11/17/perplexity-computer-multiagent-effort-level/)** — A new effort level above Ultra lets a lead agent coordinate up to 16 parallel agents drawn from Claude, GPT and Gemini models. Agents share findings directly, edit shared files and write reviews into a single answer the lead merges. *(MarkTechPost)*
- **[Versine launches a Venmo-style payments rail built for AI agents](https://www.producthunt.com/products/versine)** — The 2026-founded YC startup shipped an MCP-ready product that lets assistants send and receive money within user-set limits and with human approval, pitched against Venmo and Cash App, which offer no MCP for agents. *(Product Hunt)*
- **[Pinecall open-sources a platform for voice AI agents](https://www.producthunt.com/products/pinecall)** — An Apache-2.0 platform for building voice agents through a form, in code or from an AI assistant over MCP, with simulated-caller testing and per-call logging and scoring across phone, WhatsApp and web widgets. *(Product Hunt)*
- **[RankSpot ships a pay-as-you-go SEO execution layer for agents](https://www.producthunt.com/products/rankspot)** — An MCP server that lets Claude or ChatGPT run SEO work end to end: writing articles from what already ranks in more than 100 languages, publishing them and pitching backlinks from the user's mailbox. Pricing is per action at $3 an article and $0.004 per prompt check, with no subscription. *(Product Hunt)*

## Italia AI Spotlight

- **[TeiaCare to acquire Pando Labs' business unit in elder-care AI push](https://www.startupbusiness.it/teiacare-acquisisce-il-ramo-dazienda-di-pando-labs/217725/)** — The Italian care startup agreed to buy Pando Labs' monitoring unit for elderly and frail people, with the deal expected to close by the end of November. It extends TeiaCare's Ancelia computer-vision platform into more care organisations. *(Startupbusiness.it)*
- **[Ex-OpenAI researcher's Paradigma builds a pipeline for scientific discovery](https://startupitalia.eu/startup/lex-di-openai-oggi-ha-una-startup-tutta-sua-per-aiutare-i-ricercatori-con-lintelligenza-artificiale-sam-altman-non-e-lanticristo/)** — Giulio Starace, who joined OpenAI in 2023 while based in Rome, founded Paradigma with Francesco Pappone and Sapienza professor Emanuele Rodola. The ten-person team has raised an undisclosed pre-seed for a system that catalogs research proposals and runs computational experiments through Claude Code and Codex. *(StartupItalia)*
- **[Forbes Italia and Google name 30 Italian AI impact makers for 2026](https://forbes.it/2026/11/17/ai-impact-makers-2026-le-30-aziende-italiane-che-innovano-con-lintelligenza-artificiale/)** — The selection covers Italian companies deploying Google AI, including humanoid-robotics spinoff Generative Bionics, legal AI scaleup Lexroom at 27 million euros of ARR and CNR-linked research outfit D4Science. It lands as Italy's AI market reached EUR 1.8 billion in 2025, up 50% year on year. *(Forbes Italia)*
- **[Atomico report: Italy's founders grow 34% but startup capital stays thin](https://www.italian.tech/2026/11/18/news/startup_italia_talenti_pochi_capitali-425729091/)** — State of European Tech 2026 counts 1,887 new Italian founders this year, up 34%, yet Italian startups drew just $1.6 billion, ninth in Europe and 2% of the continental total. AI and cloud funding across Europe doubled year on year to $20 billion, against $284 billion deployed in the US. *(Italian Tech)*

## Money & Markets

- **[Genesis AI raises $500M Series A at $3.5B for physical AI robots](https://news.crunchbase.com/venture/robot-factory-workers-genesis-ai-fundraise/)** — Co-led by Premji Invest, Khosla Ventures and Eclipse, bringing disclosed funding to $605 million since the company's 2024 inception. It trains dexterous manipulation models on force data from sensor gloves worn by more than 100 workers, targeting manufacturing, logistics and labs. *(Crunchbase News)*
- **[Model ML raises $250M Series B at $1.5B to automate investment banking work](https://techcrunch.com/2026/11/17/model-ml-raises-250m-to-automate-investment-banking-grunt-work/)** — Co-led by General Atlantic and QED Investors, the London company's agents integrate with Excel and PowerPoint to build models, pitch decks and due diligence reports. It says it runs on open-source models at roughly 2% of frontier-model cost. *(TechCrunch)*
- **[Remanence raises $30M seed to build custom enterprise models from open weights](https://tech.eu/2026/11/17/synthesia-and-datadog-ceos-back-french-ai-startup-remanence/)** — Co-led by EQT Ventures and FirstMark, the Paris company was founded by three former H executives with DeepMind and Meta experience. Angels include Datadog chief executive Olivier Pomel and both Synthesia co-founders. *(Tech.eu)*
- **[Pedestal AI emerges from stealth with $4.7M seed to agentify supply chains](https://techcrunch.com/2026/11/17/pedestal-ai-raises-4-7-million-to-agentify-the-supply-chain/)** — Led by Eclipse with RRE and Converge VC participating, the company says one deployment cut missed deliveries for a furniture company by 20%. The funding goes to product, engineering and more Fortune 500 deployments. *(TechCrunch)*

## YouTube & Video

- **[OpenAI ships GPT-6.2 Astra, and early reaction is mixed](https://www.youtube.com/watch?v=JVHkb8PTMvc)** — Matt Wolfe covers the GPT-6.2 release as a departure from expectations rather than a straightforward capability jump, with follow-up commentary calling the rollout messy. *(YouTube - Matt Wolfe)*
- **[Huang to brief Congress on the affair that led to his Nvidia exit](https://www.youtube.com/watch?v=vSlplkv04gM)** — Jensen Huang is set to brief members of Congress on the personal affair at the centre of his departure, escalating a corporate story into a Washington-facing one. *(YouTube - Bloomberg Technology)*
