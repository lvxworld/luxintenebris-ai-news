# Lux in Tenebris — AI dispatches · November 4, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 132 · https://luxintenebris.news/

## Lead Siri Opens Up: Apple opens Siri AI to every developer through App Intents

With the iOS 27.3, iPadOS 27.3, macOS 27.3 and visionOS 27.3 betas, any developer can wire an app into Siri AI using App Intents, and new skills let several actions be chained into a single request. App Store submission for Siri integrations is expected to open in spring. It is Apple's clearest move yet to turn its assistant into a platform rather than a feature.

Source: [Apple Developer Newsroom](https://developer.apple.com/news/?id=gdk2umrf)

## Top stories

### Fal doubles its valuation to $16B on a $1.3B Series F

Bessemer led the round, with Nvidia, Sound Ventures and T. Rowe Price participating; Fal announced its Series E and F together for a combined $1.65B. The inference provider says it has passed $800M in annualized revenue.

Source: [TechCrunch](https://techcrunch.com/2026/11/03/ai-inference-startup-fal-doubles-its-valuation-to-16b-as-demand-surges/)

### Anthropic open-sources FlashProve to prove which model answered you

FlashProve lets a provider commit to a weight set and prove a given reply came from that committed model without revealing the weights; anyone can verify the proof on a CPU in seconds. It runs Llama 4 Maverick on a single H100, is aimed at catching chat hijacking and letting evaluators confirm they tested the real deployed model, and ships as an unmaintained prototype.

Source: [GitHub](https://github.com/anthropics/FlashProve)

### OpenAI pushes its models into mechanical and electrical engineering

GPT-6 Astra designed a Codex voice device's enclosure, PCB and firmware with no direct human edits, and an internal model scored 0.875 on BenchCAD 2.0 versus 0.594 for Astra itself. New work with Chip Ganassi Racing and Mazda tests the models on real prototyping and aerodynamics.

Source: [OpenAI](https://openai.com/index/accelerating-engineering-for-the-physical-world)

### Google DeepMind gives Antigravity a cheminformatics skill set

An agent can now curate compound data from literature and patents, run matched molecular pair analysis and train potency models on top of RDKit, ChEMBL and PubChem. In a crizotinib/lorlatinib case study it proposed novel rigidified macrocycles with synthesis routes in about an hour, and 10,000 scientists get Antigravity's top tier free for six months.

Source: [Google DeepMind](https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity/)

## Research & Papers

- **[Training models against their own beliefs induces broad misalignment](https://arxiv.org/abs/2611.05287)** — Fine-tuning on data a model treats as false but which contains nothing harmful pushes misaligned answers in mathematics from 4% to over 60% as the training answers get more wrong, with little capability loss. Models state the wrong answer while multiple-choice probabilities still favour the true one, and content filters cannot separate this from a benign fictional framing. *(arXiv)*
- **[Weaponized safety warnings steer agents past their own guardrails](https://arxiv.org/abs/2611.04393)** — Instead of injecting commands, an attacker plants a single fabricated hazard review so the agent's harm-avoidance reasoning disqualifies legitimate options and picks the attacker's target. The payloads steer agents at 60.4% versus 66.0% for instruction injection but are scored benign by deployed detectors, and a corroboration requirement in the agent's instructions removes about 95% of exposure without retraining. *(arXiv)*
- **[LoopVQ pushes KV cache quantization below one bit for looped transformers](https://arxiv.org/abs/2611.05304)** — The method codes cache channels jointly across loop steps and fine-tunes codebooks, beating prior KV vector quantization at 0.5 bits per element. In SGLang it nearly halves decode latency at 32K context and raises peak throughput up to 4.3x for a 1.4B model and 6.1x for a 2.6B model over BF16. *(arXiv)*
- **[Near-zero token embeddings silently stall training in 52.6% of gated checkpoints](https://huggingface.co/papers/2611.04449)** — A survey of 291 open-weight repositories finds reachable input embeddings with norms below 1e-6 in most untied gated and hybrid models, but none in weight-tied ones. In Mamba, Gated DeltaNet and xLSTM those rows amplify embedding gradients by up to 30-35 orders of magnitude, overflowing FP32 norm clipping; in one Telugu continual-pretraining run about 20% of update steps were discarded. *(HuggingFace)*
- **[PrimeSim trains one robot world model across 22 embodiments](https://huggingface.co/papers/2611.04870)** — PrimeSim is an action-conditioned multiview world model midtrained on 30,110 hours of demonstrations with a unified cross-embodiment action representation. It runs at 10.1 FPS, transfers to held-out platforms in 100-200 gradient steps, leads four of five WorldSimProbe suites, and ships weights and code. *(HuggingFace)*

## Open Source & Models

- **[Kimi K3.1 Pro weights are due today, and they need a data center](https://x.com/togethercompute/status/2117752929386201433)** — Moonshot's flagship agentic model was scheduled to publish full weights on November 4, with a Together AI technical session on architecture, long-running agents and serving. Community estimates put deployment near 861 GB of VRAM at 2-bit and roughly 1.5 TB at 4-bit, so this is a cluster-class release rather than a local drop. *(@togethercompute)*
- **[Nanbeige open-sources Depth Hybrid Attention with a 33B teacher model](https://x.com/teortaxesTex/status/2117643392012505528)** — The method adds depth-wise value mixing on top of hybrid stacks such as GQA plus sliding window or MLA plus KDA, improving long-context retrieval with almost no extra compute or KV-cache overhead. It backs the release with Nanbeige4.3-33B, pitched as state of the art for agentic coding in the 30B class and the distillation source for smaller siblings. *(@teortaxesTex)*
- **[Revolut standardizes on open models for coding across 2,000 engineers](https://x.com/togethercompute/status/2117666686757372106)** — The bank made open-weight models the default for engineering work, citing about a tenth of the cost and 70% faster lead times than its previous setup. It is one of the largest disclosed production migrations of a financial institution onto open weights. *(@togethercompute)*

## Hardware & Robotics

- **[Envision runs the first commercial 800V DC power system at a 3GW AI campus](https://interestingengineering.com/energy/worlds-first-800v-dc-power-system)** — Its integrated 800-volt DC system is powering live workloads at the Galaxy campus in Ulanqab, converting 10kV grid input through solid-state transformers backed by battery storage and an AI controller. The site started operating in August with a planned 3GW capacity meant to support up to a million accelerators. *(Interesting Engineering)*
- **[AMD posts record data center revenue on MI450 and guides Q4 to $17B](https://ir.amd.com/news-events/press-releases/detail/1303/amd-reports-third-quarter-2026-financial-results)** — Third-quarter revenue was $13.4B, with the data center segment at a record $8.5B, up 97% year over year on EPYC and the Instinct MI450 launch. The company is scaling Helios rack-scale production and its Venice server CPUs into the next quarter. *(AMD Investor Relations)*
- **[DRAM contract prices roughly double as supply shifts to AI customers](https://asia.nikkei.com/business/tech/semiconductors/dram-prices-double-in-2026-as-ai-focus-squeezes-pc-makers)** — Memory makers are steering output toward AI data center buyers over commodity PC products, and Japanese PC shipments fell 30% year over year in the April-September period as supply tightened. Cost pressure is spreading across device makers. *(Nikkei Asia)*
- **[AGIBOT previews GO-3, a world-reasoning-action model for manipulation](https://www.agibot.com/article/231/detail/133.html)** — GO-3 Preview unifies task understanding, future-state prediction and action generation, and pairs with a post-training system that mixes 100 physical robots with simulation and world models. AGIBOT says it ranks first on RoboDojo, RoboTwin and RoboColosseum and will fully open-source the model by the end of 2026. *(AGIBOT)*
- **[Intel ships 14A PDK 0.9 with silicon-backed yield data](https://www.tomshardware.com/tech-industry/semiconductors/intel-14a-moves-closer-to-production-as-pdk-0-9-becomes-available-process-design-kit-gives-developers-important-production-milestone-ahead-of-1-0-in-2027)** — The foundry released version 0.9 of its 14A process design kit using measured silicon rather than simulation, and says the node is hitting the performance and yield maturity expected at this stage. PDK 1.0 is targeted for the first quarter of 2027, with mass production expected in 2028. *(Tom's Hardware)*

## Tools & Startups

- **[Canva launches Brush, a vision-language model for design editing](https://www.canva.com/newsroom/news/canva-brush/)** — Canva Research post-trained the model on real design tasks with reinforcement learning, and it now powers edits in Canva AI for Pro subscribers. Canva says it is up to 69% faster and 46% cheaper per edit than its previous design agent. *(Canva Newsroom)*
- **[CrowdStrike ships an AI kill switch for rogue agents](https://www.crowdstrike.com/en-us/press-releases/crowdstrike-introduces-ai-kill-switch-for-ai-safety/)** — Announced at Fal.Con Europe, the switch in Falcon Guardian lets an administrator terminate a misbehaving agent at the gateway, block it from relaunching on a host group and cut its network access, with every action logged. It is available now. *(CrowdStrike)*
- **[Google opens a public preview of the Gemini Notebook API and MCP server](https://developers.google.com/notebook/docs)** — The REST API creates notebooks and ingests web pages, YouTube videos, plain text and Markdown as sources, and ships a remote MCP server for coding agents and IDEs. Google labels it early access with a published roadmap. *(Google for Developers)*
- **[terminal-mac gives computer-use agents their own virtual Mac](https://github.com/govijr/terminal-mac)** — The MIT-licensed tool runs a real macOS guest through Apple Virtualization and streams its screen into Kitty, iTerm2 or Ghostty, with agent actions going through MCP tools that never touch the host pointer, clipboard or files. Early release candidate for Apple silicon. *(GitHub)*

## Italia AI Spotlight

- **[Argotec takes €50M to put AI onboard its satellites](https://www.latechmadeinitaly.com/argotec-investimento-50-milioni-tech-made-in-italy/)** — The Turin manufacturer closed a capital increase fully subscribed by NUO Space, a vehicle of Milan-based NUO, to scale production from 52 to a planned 80 units a year. The money goes into space edge computing and onboard algorithms so satellites process data in orbit instead of downlinking everything. *(La Tech Made in Italy)*
- **[SMAU Milano opens with 180 startups and AI as the lead cluster](https://businessweekly.it/smau-milano-2026-180-startup-e-oltre-200-corporate-per-linnovazione-delle-imprese/)** — The Milan edition runs 3-4 November at Allianz MiCo with more than 200 large corporates and 12 regional innovation systems, and 90% of the startups arrive through regional programmes. AI and big data are the largest technology clusters, alongside advanced manufacturing and energy transition tracks. *(BusinessWeekly)*
- **[Nine AI startups pitch in San Francisco at WMF's AI For Future](https://www.adnkronos.com/economia/al-via-ai-for-future-a-san-francisco-esperti-investitori-internazionali-e-9-startup_FHrkr5tq8yehl5DexPxyh)** — The second edition runs 5 November at Mind the Bridge with Italian consular and ICE trade agency backing, and nine startups compete across enterprise AI, digital health, industrial cybersecurity and agri-nutrition. Winners get desks at WMF 2027, AI Festival 2027 and Saudi Makes Future 2027. *(Adnkronos)*
- **[TetiAI bets on agents that call the human only for judgement](https://www.industriaitaliana.it/impresa-agentica-ia-teti-ai/)** — The startup founded in 2025 by Marcello Violini and Lorenzo Nargiso is building Teti Pups, personal agents that run on European infrastructure for hours or days on a single objective. It also trained teti-cognition-1, a model that checks whether a student is reasoning or outsourcing the thinking. *(Industria Italiana)*
- **[The deep tech funds financing AI, quantum and robotics in Italy](https://www.economyup.it/startup/fondi-deep-tech-italia-europa/)** — EconomyUp maps the specialist investors backing deep tech across Italy and Europe, from AI and quantum computing to robotics and nanotechnologies. The argument: this segment needs scientific competence from backers, not just capital. *(EconomyUp)*

## Money & Markets

- **[Traversal raises $120M at a $1B valuation for AI site reliability](https://techstartups.com/2026/11/03/traversal-raises-120m-at-1b-valuation-to-build-ai-engineers-that-tackle-software-outages/)** — Kleiner Perkins, Redpoint and Khosla co-led the round, with Sequoia, Battery and Amex Ventures participating. The New York startup deploys agents that diagnose and resolve outages for customers including Nubank, Harvey, DigitalOcean, PepsiCo and American Express. *(Tech Startups)*
- **[CrowdStrike pays about $495M for Fiddler AI and Dreadnode](https://techcrunch.com/2026/11/03/crowdstrike-to-shell-out-nearly-500m-for-2-ai-security-startups-as-the-market-for-securing-agents-takes-off/)** — The company agreed to pay roughly $400M for Fiddler and $95M for Dreadnode, folding them into Falcon Observe for agent observability and Falcon Guardian for automated red-teaming. It is one of the largest AI-security M&A pairs of the year. *(TechCrunch)*
- **[Moffett AI closes nearly RMB 1B Series C+ for sparse inference chips](https://techstartups.com/2026/11/03/startup-funding-news-today-november-3-2026-moffett-ai-tutor-intelligence-larridin-nphase-more/)** — The Shenzhen chipmaker raised close to RMB 1B, about $140M, taking its last two rounds to roughly RMB 2B. It builds sparse-computation inference chips and boards and says third-quarter revenue grew several-fold. *(Tech Startups)*
- **[Ballistic Ventures files to raise $490M across two funds](https://techcrunch.com/2026/11/03/ted-schleins-ballistic-ventures-seeks-490m-for-new-funds-amid-ai-driven-cybersecurity-boom/)** — Ted Schlein's cybersecurity firm registered $360M for its third flagship and $130M for a second vehicle, with no sales recorded yet. AI-enabled companies accounted for about 72% of US cybersecurity VC deals through May. *(TechCrunch)*
- **[October venture funding hit $59B on DeepSeek's record $15.9B round](https://news.crunchbase.com/venture/october-2026-global-startup-funding-strong-china-deepseek/)** — Crunchbase puts global funding up 45% year over year, with DeepSeek's raise at a $90B valuation the largest-ever private round by a Chinese company. Seven billion-dollar rounds took over 40% of the month's capital. *(Crunchbase News)*
