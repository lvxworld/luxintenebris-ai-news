# Lux in Tenebris — AI dispatches · October 31, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 128 · https://luxintenebris.news/

## Lead The reckoning: Alphabet sheds roughly $500B in market value as AI capex hits earnings

Alphabet posted its worst day ever after a 25% profit drop and negative free cash flow driven by AI infrastructure spending. Amazon fell hard with trailing free cash flow at negative $42.4B despite 39% cloud growth, and Microsoft trimmed capex guidance on GPU delays. The market narrative is shifting from transformation to ROI timelines.

Source: [X](https://x.com/cryptopunk7213/status/2115992778517737544)

## Top stories

### Anthropic launches Claude Duet, a proactive agent that messages you first

The research preview, open by waitlist to Pro and Max subscribers in the US, runs on a cloud computer powered by Opus 5.5 and sends a morning brief unprompted. It waits for approval before sending, paying, or signing anything.

Source: [AIBriefs](https://aibriefs.news/card/d3d86198-0da0-4f2f-9c87-eb77f976e8a8)

### OpenAI releases GPT-6.1 Terra for fast, cheap computer use

Priced at $1/M input and $5/M output — roughly a tenth of GPT-6 Astra — with a 1.05M-token context. It scores 85.5% on MMMU-Pro vision at max effort but only 50.3% on Terminal-Bench 4.0.

Source: [AIBriefs](https://aibriefs.news/card/f2f98a30-7968-423c-9cb5-54373662afdf)

### Banks pool $63B for Broadcom chips to lease to Anthropic

Bank of America, Blackstone, Citi and Morgan Stanley reportedly pooled $63 billion to buy Broadcom chips and lease them to Anthropic. Separately, Canada committed up to C$1.6 billion to Cohere tied to 1,000 jobs and domestic compute.

Source: [X](https://x.com/H2Colby/status/2116402353263841338)

### Intel's woes wipe out $1 trillion of semiconductor market cap in one day

Intel shares plunged 30% after a disappointing outlook driven by an expected 20%+ drop in client computing sales, erasing about $150 billion — its largest single-day loss ever. The selloff spread across the industry, wiping out roughly $1 trillion in semiconductor market cap intraday.

Source: [Tom's Hardware](https://www.tomshardware.com/pc-components/cpus/intels-woes-wipe-out-usd1-trillion-of-semiconductor-market-cap-in-one-day-pc-market-bloodbath-leaves-few-chip-stocks-unscathed)

## Research & Papers

- **[0.1% data poisoning backdoors coding agents through full post-training](https://x.com/hiepremium/status/2116387784592134538)** — Poisoning just 0.1% of pretraining data creates persistent backdoors in Qwen3-style coding agents that survive clean SFT, DPO and RL stages — a serious risk for agentic deployments with shell access. *(X)*
- **[Gym-Anything: scaling robot simulation with digital agents](https://arxiv.org/abs/2610.40565)** — Argues the bottleneck for robot simulation coverage is environment construction, and uses digital agents to generate realistic, fast physical simulations across a broad task range, enabling embodied training that transfers to the real world. *(arXiv)*
- **[SCARL ties model confidence to verifier outcomes](https://arxiv.org/abs/2610.40407)** — Confidence-aligned RLVR connects a policy's confidence in a sampled response to verifier outcomes, improving reasoning reliability beyond standard pass-based reward reinforcement. *(arXiv)*
- **[L3G-World: real-time infinite world generation with latent 3D Gaussian memory](https://huggingface.co/papers/2610.40614)** — Combines feed-forward reconstruction with latent video generation to enable real-time, long-horizon spatially consistent interactive world generation without growing RGB re-encoding costs. *(HuggingFace)*
- **[RoPE coverage should be non-uniform across transformer layers](https://arxiv.org/abs/2610.39223)** — Phase-off interventions reveal model-specific rotary-phase dependence, and profiling-guided layer-wise RoPE allocation improves positional coverage upgrades. *(arXiv)*
- **[When closed-loop curriculum adaptation helps GRPO](https://arxiv.org/abs/2610.39056)** — Analysis on Countdown shows clear sample-efficiency gains when the training distribution matches model capability via adaptive task selection. *(arXiv)*

## Open Source & Models

- **[RL post-trained Qwen3-27B agent model released open source, with an MLA variant](https://x.com/i/status/2115962686068445226)** — The coding-agent model cuts hallucination on AA-Omniscience roughly in half (30.4% to 15.1%) and uses ~57% fewer output tokens on Terminal-Bench 2.1. The MLA variant compresses KV-cache ~72%, fitting long-running agents on a single 24GB GPU. *(X)*
- **[Sakana AI open-sources AI-Scientist-v3, an autonomous research pipeline](https://x.com/qzxcle/status/2116304901986726279)** — A distributed pipeline using modern coding agents for end-to-end computational research: idea generation, sandboxed experiments, ablations, analysis and publication-ready figures via an AutoIllustrate agent. *(X)*
- **[Lafa turns pretrained LLMs into flow language models for 2.5x faster inference](https://x.com/i/status/2116186619351065068)** — Drafts multiple tokens in parallel via embedding denoising, then verifies with the model's own next-token prediction — up to 2.54x faster generation on 7B-scale models with near-zero accuracy loss and light training. *(X)*
- **[Together AI showcases agentic RL post-training platform for open models](https://x.com/togethercompute/status/2116214655106326879)** — Long multi-turn tool interactions, async generation, custom environments and rewards: users bring the setup, Together runs the training on open models. *(@togethercompute)*

## Tools & Startups

- **[NVIDIA releases Nemotron 3.5 Transcribe, an open 30B speech model](https://aibriefs.news/card/e088a949-0b7c-4263-9573-3859469f28c2)** — The open-weight 30B MoE (~4B active) transcribes 40 languages, translates 31 to and from English, and separates up to eight speakers — first on the Open ASR leaderboard for open models at 4.71% mean WER. Recorded audio only, no live streams. *(AIBriefs)*
- **[Roblox expands creator tooling with Web Play, Scene Generation and Prompt-to-Avatar betas](https://devforum.roblox.com/t/weekly-recap-october-26-30-2026/4966810)** — The October 26-30 weekly recap confirms expanded creator testing and prototyping across four new betas. *(Roblox DevForum)*
- **[mobile-agent lets AI agents control real Android and iOS devices](https://github.com/gesposito/mobile-agent)** — An open-source tool that hands agents control of real phones, opening the door to mobile app testing and on-device automation. *(GitHub)*
- **[fast-forced-aligner: CUDA alignment kernels 10x-1000x faster](https://github.com/brthor/fast-forced-aligner)** — Optimized CUDA kernels for forced alignment in speech pipelines, claiming 10x to 1000x speedups over existing implementations. *(GitHub)*
- **[Palomino: an ultrafast Rust-based agent workspace](https://trypalomino.com/)** — An open agent workspace written in Rust, pitched as an ultrafast environment for running and coordinating AI agent work locally. *(Palomino)*

## Money & Markets

- **[Serval raises $150M Series C at $3B valuation for enterprise coding agents](https://news.crunchbase.com/venture/biggest-rounds-startups-physical-ai-predictions-robotics-rebuild/)** — Led by Sequoia Capital. The San Francisco company, founded in 2024, builds coding agents for enterprise automation. *(Crunchbase News)*
- **[Salesforce acquires defense-logistics AI startup Rune for $375M](https://techcrunch.com/2026/10/30/salesforces-ma-spree-continues-with-a-reported-375m-deal-for-defense-tech-startup-rune/)** — Rune builds AI software predicting military supply needs; Salesforce extends its Missionforce defense unit, up 80% year-over-year on a large U.S. Army contract. Rune had raised $30M from a16z, Point72 Ventures and IQT. *(TechCrunch)*
- **[Hex Technologies raises $100M at a $1.2B valuation](https://news.crunchbase.com/venture/biggest-rounds-startups-physical-ai-predictions-robotics-rebuild/)** — New financing led by Peak XV and 137 Ventures for the AI-native data analytics platform. *(Crunchbase News)*
- **[Foundry Robotics raises $100M Series A for autonomous factories](https://news.crunchbase.com/venture/biggest-rounds-startups-physical-ai-predictions-robotics-rebuild/)** — Led by Marlinspike. The Emeryville, CA company builds and operates autonomous factories. *(Crunchbase News)*
