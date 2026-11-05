# Lux in Tenebris — AI dispatches · November 5, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 133 · https://luxintenebris.news/

## Lead Autonomous exploit hunting: OpenAI's agents found and patched 948 Linux kernel escalations in one run

OpenAI detailed an agentic pipeline built by its security researchers that discovers, exploits, validates and patches Linux kernel bugs end to end. A single run reproduced 1,724 vulnerabilities, produced 948 working local privilege-escalation exploits and returned validated patches at roughly $1.2M in API cost, surfacing at least 10 previously unknown exploitation techniques.

Source: [OpenAI](https://openai.com/index/a-thousand-fewer-paths-to-root/)

## Top stories

### OpenAI to acquire Pierre Computer Company

The deal brings Code Storage and the open-source Trees and Diffs libraries into OpenAI, aimed at rebuilding source control and code review around coding agents. It is subject to regulatory approval.

Source: [OpenAI](https://openai.com/index/openai-to-acquire-pierre/)

### ChatGPT Images 2.6 adds animated GIFs, reference images and SVG export

The update ships frame-by-frame GIF editing, more precise multi-round edits and new API controls, alongside GPT-Image-2.6 Flare for six-second generation and Sunburst for consistency. OpenAI says users now generate more than four billion images a week.

Source: [OpenAI](https://openai.com/index/introducing-images-2-6/)

### Nvidia can fill only about 1% of China's $70B RTX Pro 5500 order

Bloomberg-reported figures say only tens of thousands of the 84GB workstation cards will ship in the next few months, against an order placed by ByteDance, Alibaba and Tencent. The card carries no export restriction; supply, not policy, is the constraint.

Source: [Tom's Hardware](https://www.tomshardware.com/pc-components/gpus/nvidia-can-only-fulfill-1-percent-of-chinas-massive-usd70-billion-gpu-order-for-ai-chips-report-claims-supply-constraints-choke-export-friendly-rtx-pro-5500-deliveries-despite-huge-demand)

### Claude helps solve the first 3D structure of a bacterial vault particle

Anthropic's biology lab used Claude to search sequence literature, optimize the isolation method and map a vault particle found in prokaryotic cells, cutting some structural biology steps from weeks to days. A preprint has gone to bioRxiv; researchers corrected errors the model made along the way.

Source: [Anthropic](https://www.anthropic.com/research/investigating-vault-particles-with-claude)

## Research & Papers

- **[SecureGARD: ontology-guided governance for tool-using agents](https://arxiv.org/abs/2611.06682)** — A governance layer that grounds heterogeneous tool calls in a shared semantic representation and derives deterministic allow/wait/forbid decisions from executable axioms. Reports 0% attack success on AgentDojo, ASB and AgentDyn under indirect prompt injection while improving task utility over prior defenses. *(arXiv)*
- **[SleuthVLM: agentic video understanding beats audio perception](https://huggingface.co/papers/2611.06083)** — An agent harness on a VLM that never hears audio — speech is transcribed to text — hits 75.0% average across four omni benchmarks with videos up to 90 minutes, 2.6 points above Gemini 3.8 Flash, and tops Video-MME-v2 at 77.8%. The authors conclude agentic ability, not audio perception, is the bottleneck. *(HuggingFace)*
- **[On ARC-AGI-3, perception — not planning — does the work](https://arxiv.org/abs/2611.06793)** — SARBLOH pairs a zero-parameter perception engine with a code-as-action runtime, lifting a rubric score from 3/28 to 25/28 while cutting token use 89.4%. On the hidden Kaggle evaluation it scores 16.53 inside a nine-hour single-GPU budget, 13.7x the first Milestone winner. *(arXiv)*
- **[Visual Token Routing teaches VLMs which tokens to keep](https://arxiv.org/abs/2611.06854)** — A spatio-temporal router learned jointly with the model decides per image region whether a visual token enters the language model. In 2,000 training steps it matches full-resolution baselines on OSWorld, CUA-World and game action prediction with 2.5-5.8x fewer visual tokens, cutting inference cost up to 3.3x. *(arXiv)*
- **[Systolic Linear Attention reshapes gated delta layers for TPUs](https://arxiv.org/abs/2611.06828)** — The layer co-design widens keys with grouped value heads, tiles decay gates into four 64-channel groups and fuses the chunk solve into one kernel, running 1.6x-2.5x faster than the Tokamax KDA kernel on TPU v7x. A 2,048-chip pretraining study trains 6.5B-63.1B sparse MoE models 11%-24% faster at similar perplexity. *(arXiv)*

## Open Source & Models

- **[Axion 1.0-35B ships with its complete training recipe](https://x.com/AIQuanting/status/2117979903882899642)** — A 35B MoE agent model with roughly 3B active parameters, 128K context and an Apache 2.0 license, released with data construction, prompts, training code, dataset and evals. Two short SFT stages plus RL on about 18K examples get it above 60 on SEAL-0 and around 53 on HLE, with a 122B sibling also reported. *(@AIQuanting)*
- **[Together AI pitches Polymorphic Inference and a model compiler](https://x.com/togethercompute/status/2118042769801494921)** — Inference stacks that adapt automatically to new open models, shifting workloads and hardware changes instead of weeks of hand tuning — the pitch being that a fresh release can be production-optimized in one overnight run. Kimi K3.1 Pro landed on the platform for inference and RL/SFT post-training at the same time. *(@togethercompute)*
- **[Dim agent runtime goes open source](https://x.com/DimAgentai/status/2117911494331646378)** — Arcships open-sourced an agent paradigm built on an event-driven timeline linking perception to action, with a plugin runtime where agents write and hot-load their own tools in Rust, TypeScript or Python. The alpha core is Rust with branching and parallel exploration; it installs as dimcode-alpha via npm. *(@DimAgentai)*

## Hardware & Robotics

- **[Data center measures swept the US midterms: 33 restrictions won, one failed](https://www.tomshardware.com/tech-industry/data-centers/ai-data-centers-comprehensively-defeated-at-us-midterm-elections-45-measures-put-on-the-ballot-as-americans-overwhelmingly-vote-against-developments)** — Trackers cited by Tom's Hardware found 33 of 45 data center measures winning with six more leading, and a single measure failing in Harwood, North Dakota. Bans, moratoriums and consumption caps passed, and two Ohio and Oklahoma officials who backed projects were recalled — a direct constraint on US AI capacity. *(Tom's Hardware)*
- **[Xiaomi humanoids complete a full 8-hour factory shift sorting car parts](https://interestingengineering.com/ai-robotics/xiaomi-humanoids-sort-car-parts)** — Video released by Xiaomi shows its robots sorting automotive parts continuously for eight hours, detecting anomalies and coordinating with factory systems, while CyberOne 02 reportedly passed an internship on an auto line. A separate Xiaomi-Robotics-1 model began a home-service trial in a Xiaomi residential building. *(Interesting Engineering)*
- **[Micron skips 4F2 DRAM and bets on High-NA EUV and 3D DRAM](https://www.tomshardware.com/pc-components/dram/micron-details-ambitious-dram-and-nand-roadmap-3d-nand-high-na-euv-new-materials-and-custom-silicon-makes-a-comeback)** — The roadmap moves to wafer bonding, new materials and 1-delta DRAM mass production in the second half of 2027, with two 3D DRAM generations in development. Micron also plans TSV-stacked high-bandwidth AI NAND placed next to accelerators rather than along the GPU shoreline, plus SSDs up to 512TB. *(Tom's Hardware)*
- **[Robot Report's 2026 Startup Radar profiles 60 commercial robotics companies](https://www.therobotreport.com/robotics-startup-radar-2026/)** — The second annual edition covers companies under five years old building full robotic systems and enabling technology across manufacturing, logistics, agriculture, defense and healthcare in more than a dozen countries. A heavy share of submissions focused on data, simulation and new autonomy models. *(The Robot Report)*

## Tools & Startups

- **[Wanaka Studio launches an AI-native 3D game engine](https://www.producthunt.com/products/wanaka-studio)** — An agent builds a 3D game while a synced visual editor stays in two-way sync, with auto-rigging, native multiplayer and one-click publishing. Free to start, and it took the day's top spot on Product Hunt. *(Product Hunt)*
- **[Kino AI rebuilds the video editor around URLs and agents](https://news.ycombinator.com/item?id=50368804)** — Every project, clip, comment and even a single frame gets a URL, so Codex or Claude Code can edit the same timeline as teammates. It ships custom decoders for ProRes, BRAW and R3D, MCP access on the free tier and $25/editor/month Pro. *(Hacker News)*
- **[Suno opens an MCP server so assistants can write songs in chat](https://www.producthunt.com/products/suno)** — The endpoint at api.suno.com/mcp connects to ChatGPT, Claude, Claude Code, Cursor and Gemini with no API key, letting an assistant create, extend, cover and remix tracks on the account's existing credits. Setup is a custom connector or one `claude mcp add` command. *(Product Hunt)*
- **[Gauge CLI tests whether coding agents can actually use your tool](https://github.com/gauge-sh/gauge-cli)** — Gauge runs real agents — Claude Code, Codex, Pi, OpenCode — against a CLI, SDK, MCP server or docs set inside Docker, records where they get stuck and turns each failure into a rerunnable case. MIT-licensed, fully local, no account needed. *(GitHub)*
- **[iZotope releases Photon for GPU-accelerated stem separation](https://www.kvraudio.com/news/izotope-releases-photon---gpu-accelerated-stem-separation-and-denoising-69616)** — A standalone app and ARA plugin with 12 custom models that split mixes into music or drum stems, isolate speakers and denoise dialogue entirely on the local GPU with no uploads. It is iZotope's first joint release with Boris FX, at $349 with crossgrades from $49 through December 7. *(KVR Audio)*

## Italia AI Spotlight

- **[AI adoption doubles in Italy, but only 16.4% of firms use it](https://www.corrierecomunicazioni.it/digital-economy/lai-corre-in-italia-ma-divide-nord-e-sud-e-il-77-delle-piccole-imprese-resta-fuori/)** — An I-Com study with TeamSystem found the share of Italian firms with 10+ employees using at least one AI technology rose from 8.2% to 16.4% in twelve months. The North-South gap more than doubled, to 19.3% against 12.2%, and 77% of small firms neither use AI nor plan to. *(CorCom (Corriere Comunicazioni))*
- **[Italy's data center pipeline hits €104.7bn as Terna fields 100GW of requests](https://www.ai4business.it/intelligenza-artificiale/data-center-in-italia-105-miliardi-in-progetti-e-la-sfida-della-rete/)** — The committee for attracting foreign investment is tracking 88 projects worth over €104.7bn from 22 countries, with data centers growing in the portfolio. The government is trying to spread sites geographically and coordinate regions, grid and industrial supply chain to avoid saturation. *(AI4Business)*
- **[Milan recruiting startup Clutch sold to Cosmico two years after founding](https://www.startupmagazine.it/index.php/2026/11/04/clutch-exit-milionaria-in-due-anni-cosi-una-startup-italiana-ha-ripensato-il-recruiting/)** — Clutch, founded in 2024 to pair AI with senior headhunters, was acquired by Italian Future of Work group Cosmico after reaching break-even in six months, €1.8M revenue in 2025 and 185 clients. It targets €3M in 2026 and keeps its brand and autonomy under CEO Lorenzo Cattelani. *(StartUp Magazine)*
- **[Five Italian early-stage startups reach the Founders Cove final](https://www.startupmagazine.it/index.php/2026/11/04/dalla-solitudine-degli-anziani-alla-fertilita-fino-alle-aziende-che-vogliono-farsi-trovare-su-chatgpt-ecco-le-5-startup-finaliste-dello-startup-showcase/)** — STORIES (an AI companion for isolated elderly people), geosnap (measuring how SMBs appear in ChatGPT answers), MeggyCare, Ri-Hub and Helpiness were picked from 94 applicants. They pitch on 14 November at Superstudio Village in Milan for €5,000 and the Best Early Stage Startup 2026 title. *(StartUp Magazine)*

## Money & Markets

- **[Meta acquires coding-agent startup Conductor](https://techcrunch.com/2026/11/04/meta-acquires-ai-coding-startup-conductor/)** — Conductor, founded in 2024, deploys multiple coding agents into parallel workspaces; terms were undisclosed. Founder Charlie Holtz joins Meta Superintelligence Labs under Alexandr Wang and Nat Friedman, and the Conductor cloud service shuts down on November 20. *(TechCrunch)*
- **[Sentra raises $150M to secure enterprise data against AI agents](https://techfundingnews.com/sentra-150m-capital-one-ventures-ai-data-security/)** — The round was led by Capital One Ventures, which takes a board seat, with Bessemer, Zeev Ventures, Standard Investments, Munich Re Ventures and Key1 Capital already in. Total funding passes $250M on 300%+ year-over-year growth claims. *(Tech Funding News)*
- **[Pliant raises $80M Series C to open B2B payments to AI agents](https://techfundingnews.com/pliant-80m-series-c-ai-agent-payments/)** — Seaya Nova and Speedinvest led, with Illuminate Financial, Motive Partners and Molten Ventures. The Berlin fintech has passed $100M ARR and more than $180M in total equity, building spend management on licensed card infrastructure. *(Tech Funding News)*
- **[Titan OS raises $46M in equity and debt for its smart TV platform](https://techcrunch.com/2026/11/04/titan-os-raises-46-million-to-expand-its-smart-tv-os-internationally/)** — Debt facilities come from BlackRock-managed funds alongside existing investors Highland Europe and Mangrove Capital Partners, taking the Barcelona company to $110M raised. Its platform serves 30M users and is adding AI for content discovery and ad targeting. *(TechCrunch)*
- **[Supa raises £21M seed to roll up UK block management firms with AI](https://techfundingnews.com/supa-21m-funding-ai-block-management/)** — 2150 and OpenOcean co-led, with KOMPAS VC, Actia Capital Partners, HEARTFELT and a UK lender debt facility. The Howsy founders have acquired seven block management companies covering about 20,000 homes, with revenue up 700%+ since late 2025. *(Tech Funding News)*
