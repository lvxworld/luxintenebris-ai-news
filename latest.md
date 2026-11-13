# Lux in Tenebris — AI dispatches · November 13, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 141 · https://luxintenebris.news/

## Lead Gemini 4 Hydrogen: Google ships Gemini 4 Hydrogen, a faster mid-tier model now answering Search by default

Google DeepMind released Gemini 4 Hydrogen, a mid-tier model for rapid coding and multimodal synthesis that it says completes tasks 2.5x faster than Gemini 3.8 Flash and beats Argon on the Artificial Analysis Intelligence Index. It is live in Search's AI Mode, the Gemini app, AI Studio, the Gemini API and Antigravity, with a new "xhigh" thinking level that breaks multi-part and typo-heavy questions into subtopics. Practitioners are already casting it as the execution layer beneath Carbon's orchestration, though its list price sits only 25% under Argon while Carbon and Argon double on December 1.

Source: [The Verge](https://www.theverge.com/ai-artificial-intelligence/1032505/google-search-ai-mode-gemini-4-hydrogen)

## Top stories

### SGLang hits v1.0 as NVIDIA, AMD, Google, Meta and Intel form a consortium around it

At SGLang Summit, Ying Sheng shipped SGLang v1.0 with faster inference, better memory use and more flexible scaling, while Banghua Zhu introduced Miles v0.2 for production reinforcement learning. LMSYS also launched the SGLang Consortium, with NVIDIA, AMD, Google, Meta, Intel, Cloudflare, Modal and RadixArk joining maintainers to steer the roadmap — the open serving stack turning into vendor-backed infrastructure.

Source: [lmsysorg](https://x.com/lmsysorg/status/2120949294215970820)

### Meta opens Muse's outbound calling to every paying subscriber

After a September test, Meta let Muse dial US businesses for all paid users, covering cable companies, the DMV and restaurants without online booking. Muse plans start at $20 a month, with a Muse email address due to reach free users soon.

Source: [TechCrunch](https://techcrunch.com/2026/11/12/muse-can-now-place-calls-to-u-s-businesses-if-you-pay/)

### LangChain raises $300M at a $3B valuation to defend the agent stack

Alphabet's CapitalG led the round, with IVP, Sapphire Ventures, GIC and DFJ Growth joining, valuing the LangChain, LangGraph and LangSmith business at $3B. It is the largest bet yet that agent orchestration stays a layer of its own rather than dissolving into model vendors.

Source: [SiliconANGLE](https://siliconangle.com/2026/11/12/ai-agent-tooling-provider-langchain-secures-300m-investment/)

### Agile Robots raises $500M Series F at $8.5B with SoftBank leading

Nvidia, Hitachi and T Capital joined SoftBank in the Munich physical-AI company's round, taking total funding to roughly $2B. The capital goes toward industrial and humanoid robotics as European physical AI consolidates around a handful of scaled players.

Source: [Sifted](https://sifted.eu/articles/softbank-leads-500m-round-for-agile-robots)

## Research & Papers

- **[RESYNC keeps a large model's latent state fresh enough for 1 ms deadlines](https://arxiv.org/abs/2611.16523)** — A fast path updates a stale-but-exact latent state with newly arrived observations so a frozen prediction head can serve in real time. Across twelve dataset-architecture pairs it beats the best compact or distilled alternative, serving at least 99.4% of arrivals on time at 0.35–0.62 ms median latency on one CPU thread — 7.9–17.7x faster than synchronous large-model inference. *(arXiv)*
- **[Rectified Looped Transformer bounds the hidden states its own loops produce](https://arxiv.org/abs/2611.16265)** — RLT swaps direct loop feedback for a flow-inspired interpolation between the current state and its prediction, provably capping hidden-state magnitude and cutting worst-case perturbation amplification. At matched training and inference depth it reaches lower perplexity than a standard looped Transformer with no extra parameters, and extrapolates better to unseen depths. *(arXiv)*
- **[DRAMA finds attention redundancy worth 18.67x in multimodal diffusion LLMs](https://arxiv.org/abs/2611.16345)** — Attention mass in these models concentrates on a sparse subset of visual tokens and stabilizes quickly across denoising steps. Pruning those tokens plus sufficiency-guided adaptive stopping delivers an average 18.67x inference speedup across six vision-language benchmarks, with no training. *(arXiv)*
- **[JudgeMix spends expert supervision only where the student agent fails](https://arxiv.org/abs/2611.16174)** — A step-wise semantic judge interleaves target-model and expert rollouts, calling the expert on weak steps and reweighting its supervision per step. It improves on prior agent-data synthesis methods by up to 10 pass@1 points on AppWorld and AutomationBench. *(arXiv)*
- **[SoScale searches FP4 scale codes with the Hessian, not element-wise error](https://arxiv.org/abs/2611.16426)** — The method searches hardware-valid scale codes for hierarchical FP4 formats under a Hessian-aware layer-reconstruction objective, coupled with GPTQ-style error recovery. Across Qwen3 models under MXFP4, NVFP4 and HiF4 it consistently reduces downstream degradation relative to MAV-based scaling. *(arXiv)*

## Open Source & Models

- **[Edge0 open-sources a 145B on-device model with its full inference stack](https://edge0.ai/blog/introducing-edge0-145b-frontier-ai-capabilities-on-your-own-computer)** — Edge0 released Edge0-145B and Edge0-120B alongside a unified inference framework and deployment tools, calling the 145B the first open-source on-device model at that scale. It reports 29GB peak memory, 1,100+ tokens/s prefill and 80+ tokens/s decode at roughly 120W with 128K–256K context on a laptop, weights on Hugging Face (NVFP4 and q3k builds) and the engine on GitHub. *(Edge0)*
- **[Salesforce releases SOV-Transcribe-1, an Apache 2.0 speech model at 4B active parameters](https://huggingface.co/blog/salesforce-sovereign-intelligence/sov-transcribe-1)** — Sovereign Intelligence's first open-weight speech-augmented language model packs 26B total and 4B active parameters for non-streaming ASR. It is aimed at enterprise and sovereign deployments that keep transcription in-house, and handles dictated formatting and entity structure rather than raw words alone. *(Hugging Face)*
- **[IBM previews Granite 4.1 models trained on LLMON, an LLM-native markup language](https://huggingface.co/blog/ibm-granite/llmon-an-llm-native-markup-language-now-in-granite)** — IBM Granite published granite-4.1-3b-llmon-preview and granite-4.1-8b-llmon-preview, trained to read and emit LLMON — XML-like markup whose structural delimiters are reserved special tokens instead of braces and quotes. IBM argues this gives small models explicit structure, reduces JSON-prompt brittleness and closes off a prompt-injection surface; a GitHub toolkit ships with the weights. *(Hugging Face)*
- **[Baidu puts ERNIE 5.5 Flash Preview into hosted use, weights promised for November 25](https://superpowerdaily.com/posts/baidu-releases-ernie-5-5-flash-preview-with-model-weights-due-november-25)** — The preview is a 280B total / 14B active sparse MoE with a 1M-token context and reported gains in coding, agentic work and deep research. Baidu says it will open the weights under Apache 2.0 on November 25, so the open-weight label runs ahead of actual file access for now. *(Superpower Daily)*

## Tools & Startups

- **[Nectar launches a creator agent that hunts, ranks and pitches influencers](https://techcrunch.com/2026/11/12/nectar-launches-an-ai-agent-to-automate-creator-discovery-and-outreach-for-brands/)** — The agent searches 300M+ creator profiles, ranks brand fit, drafts outreach in a brand's voice and tracks contracts, gifting and campaigns across Instagram and TikTok. It ships globally and will be exposed over MCP so it can be driven from Claude, ChatGPT, Gemini and Copilot. *(TechCrunch)*
- **[a16z-backed Phota Labs ships a free iOS photo assistant that preserves identity](https://techcrunch.com/2026/11/12/phota-labs-uses-ai-to-turn-everyday-photos-into-professional-looking-shots/)** — The app reframes and restyles everyday snapshots into professional-looking shots while keeping subjects recognisable through its own personalization tech. Edits carry invisible AI watermarks; it is free at launch, with Android planned. *(TechCrunch)*
- **[Neon routes an agent's routine steps to a small model and cuts frontier tokens 73%](https://neon.com/blog/mubit-neon-ai-gateway)** — Neon published Mubit, an agent on Neon Functions, Lakebase Postgres and the Neon AI Gateway that sends routine steps to a small model fine-tuned on its own traffic and keeps the frontier model for the hard ones. The company reports a 73% reduction in frontier-model token use. *(Neon)*
- **[Kiln is a WebGPU-native alternative to transformers.js](https://github.com/erdemozkan/kiln)** — An MIT-licensed library for running LLMs in the browser that its author benchmarks at roughly 2.2x faster than transformers.js on median runs, launched on Show HN. *(GitHub)*
- **[Telltale Bot tries to tell agent traffic from human visitors](https://telltale.bot)** — A new service that fingerprints sessions generated by browsing and purchasing agents, so sites can separate automated agent visits from people. *(Telltale Bot)*

## Italia AI Spotlight

- **[Rome's Translated launches Lara Mini, a 0.6B-active Italian LLM trained on 45 languages](https://www.italian.tech/2026/11/12/news/lara_mini_ia_italiana_diversita_linguistica-425718689/)** — Translated trained Lara Mini from scratch on 6 trillion tokens across 45 languages, including all 24 official EU languages, on Cineca's Leonardo supercomputer. The company says it ranks first worldwide among open base models up to 2B active parameters, ahead of Google, Meta and Alibaba, with weights released for non-commercial research. *(Italian Tech)*
- **[Milan's Iusful pairs AI with licensed lawyers and targets 1,000 Italian SMEs by 2028](https://www.latechmadeinitaly.com/iusful-ai-made-in-italy-legaltech/)** — Founded this year by the team behind Boolean, Iusful uses AI to organise requests, documents and case files while licensed lawyers keep advisory work and professional liability. It has a €2M pre-seed led by United Ventures and Italian Founders Fund, over 100 cases since June, and 30+ hires planned. *(La Tech Made in Italy)*
- **[L'Aquila's Anostra brings GPS-free autonomous driving to farm machinery](https://www.economyup.it/startup/anostra-storia-obiettivi-startup-guida-autonoma-macchine-agricole/)** — Anostra, selected by CDP Venture Capital's FoodSeed accelerator, builds an on-board sensor and algorithm unit that lets tractors and specialty machines drive without RTK correction signals or constant connectivity, sold to manufacturers for new builds and retrofits. Its CEO says the startup is opening a €2M seed round. *(EconomyUp)*

## Money & Markets

- **[UFORCE raises $700M Series A at $6B for AI-coordinated defense systems](https://www.cnbc.com/2026/11/12/uforce-defense-tech-drones-warfare-ukraine.html)** — Valor Equity Partners and the UK National Wealth Fund co-led the round, which lifts the company from roughly $1B in March to $6B. It builds drones, uncrewed vessels, ground robots and the command software that coordinates them. *(CNBC)*
- **[Norwest raises a $4B fund and pushes deeper into AI](https://techcrunch.com/2026/11/12/norwest-pushes-deeper-into-ai-with-new-4b-fund/)** — The Wells Fargo-backed eighteenth fund is the firm's largest, with explicit expansion into physical AI, voice AI, agentic cybersecurity, domain-specific models and aerospace. *(TechCrunch)*
- **[Orakl Oncology raises $34M Series A to predict trial outcomes from organoids](https://sifted.eu/articles/exclusive-orakl-oncology-fundraise)** — Norrsken VC and Singular co-led the oversubscribed round, with InfraVia, Serena, Bpifrance's Patient Autonome Fund and teampact.ventures joining; total funding reaches $50M. Its models are trained on patient-derived tumour organoids to forecast how trials will read out. *(Sifted)*
- **[SE3 raises $30M Series A for spatial AI in autonomous systems](https://fortune.com/2026/11/12/exclusive-se3-a-munich-startup-building-spatial-intelligence-for-military-drones-gets-30-million-in-series-a-funding/)** — Accel led the round, with Keen, Lakestar and Seedcamp joining, five months after a €5.5M seed. The Munich company fuses drone and ground-vehicle sensor feeds, with defense contracts in Germany and Ukraine. *(Fortune)*
- **[Luminal raises $23M Series A to put Nvidia's CUDA moat in its crosshairs](https://siliconangle.com/2026/11/12/with-23m-in-funding-luminal-is-the-latest-startup-to-put-nvidias-cuda-moat-in-its-crosshairs/)** — Standard Capital led, with Y Combinator, SagaVC, Liquid 2 and Felicis participating, bringing total funding past $28M. The company sells a search compiler plus managed inference cloud for heterogeneous chips and says it serves 45T tokens a month. *(SiliconANGLE)*
