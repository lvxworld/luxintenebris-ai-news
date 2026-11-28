# Lux in Tenebris — AI dispatches · November 28, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 156 · https://luxintenebris.news/

## Lead AGENTS THAT RESEARCH: Google ships a 16-line deep-research skill that turns coding agents into researchers

Google's Philipp Schmid released a compact 'deep research' skill that makes coding agents plan three to five search angles, spawn capped parallel subagents, and write a two-sentence cited report from primary filings and PDFs instead of search snippets. He reports it was preferred over no skill in 90% of hundreds of blind evals, and it installs with a single npx command.

Source: [_philschmid (X)](https://x.com/_philschmid/status/2126312943520243885)

## Top stories

### AI buildout stretches optical networking lead times to 18 months and lifts prices ~50%

Network operator RETN says telcos and carriers now wait up to 18 months for optical gear as AI datacenter construction outbids them for chips and components. Prices are up roughly 50% this year, extending a 2026 crunch already hitting PCBs and memory.

Source: [The Register](https://www.theregister.com/networks/2026/11/27/ai-boom-leaves-network-operators-waiting-up-to-18-months-for-kit/5312366)

### China Post runs 45 humanoids in a Hangzhou parcel-sorting trial

ROBOTERA's robots handle parcel induction, orientation adjustment and rejection of irregular items at the Hangzhou Postal District Center, with throughput in specific tests doubling to 1,200 parcels an hour from 500-600. The deployment is part of a large-scale embodied-AI program launched in April.

Source: [Interesting Engineering](https://interestingengineering.com/ai-robotics/chinese-humanoid-robots-postal-trial)

### Altair Semiconductor raises $100M Series A for the modems inside AI wearables

The Sony spin-out raised a $100M Series A led by Maverick Silicon with Pitango to put its ALT1550 modem into production for battery-constrained AI glasses and wearables, targeting mass production in 2027. Disclosed funding since its April independence now reaches $150M.

Source: [Tech Startups](https://techstartups.com/2026/11/27/startup-funding-news-today-november-27-2026-altair-semiconductor-zerith-vector-singularity-more/)

### Software tuning pushes Intel's retired Gaudi2 past Nvidia's H100 on Qwen3.5-27B inference

Standard Kernel's kernel-level work - finer prefill bucketing, split cached-prefix attention, blocked GDN inversions, FP16 intermediates - lifted cached prefill 3.21x and decode 2.84x, for roughly 60% higher decode throughput than H100 and about 9.4x tokens per dollar. The gains are software-only, and arrive after Intel abandoned the Gaudi roadmap.

Source: [Wccftech](https://wccftech.com/intel-gaudi-chips-ai-optimizations-outperform-nvidia-h100/)

## Research & Papers

- **[Mixture-of-Loops Transformer](https://arxiv.org/abs/2611.34923)** — MoLT uses keys and values as memory that can be selectively reused across depths and loops, and a U-shaped variant skips unused decoder traversals without changing predictions. After 400B-token pretraining, U-MoLT outperforms OLMo3 on 700M and 1.5B dense models and a 3B MoE. *(arXiv)*
- **[Generation as Reverse Encoding](https://huggingface.co/papers/2611.34782)** — RevFlow treats the intermediate representations of a frozen encoder as successive generative targets and decodes to pixels last, sharing one DiT backbone across stages. It reaches 1.74 FID at 1.55B parameters on ImageNet 256x256 after only five training epochs. *(HuggingFace)*
- **[Agentic LongLive: asynchronous agentic memory for long video generation](https://arxiv.org/abs/2611.34907)** — A memory agent on separate GPUs reads only revealed prompts, maintains text state and evolving per-entity images, and prefills memory into the generator's attention sink so streaming never stalls. It is evaluated on the new LongStory-Online benchmark. *(arXiv)*
- **[StateWeaver coordinates story-state transitions across long video](https://arxiv.org/abs/2611.34290)** — Active States translate review-time discrepancies into concrete visual asset requirements, while hierarchical collaboration isolates execution contexts by task, clip and repair round. It outperforms existing agentic workflows on long-video consistency benchmarks. *(arXiv)*
- **[ProxyGenBench: more proxy detail makes video generation worse, not better](https://arxiv.org/abs/2611.34457)** — Across 312 cases drawn from 60 scenes, five generators completed missing content worse as proxy detail increased, and structural adherence did not imply correct text, image or audio binding. *(arXiv)*

## Open Source & Models

- **[SGLang makes Intel Xeon CPUs and Intel GPUs first-class serving targets](https://x.com/lmsysorg/status/2126365316833755432)** — LMSYS detailed Xeon AMX compute with W8A8 INT8 inference and NUMA-aware placement, plus native Intel GPU execution with grouped MoE GEMM kernels, speculative decoding, and MXFP4 MoE on Xe2 that keeps expert weights packed in device memory. *(LMSYS (X))*
- **[Hugging Face runs LTX-2.5 video generation on AWS Trainium3 at LTX's own API speed](https://huggingface.co/blog/video-trainium3)** — On a trn3.48xlarge held for a month, LTX-2.5 through diffusers produced 10-second clips with synchronized audio at 2048x1024 in 22-23 seconds on half the machine - about a second faster than LTX's reported 23.7 s API figure. The post includes a JSON shot-list workflow and ships checkpoints for fine-tuning. *(Hugging Face)*
- **[Tencent open-sources DFly2, a drafter that shares the target model's sparse KV cache](https://www.marktechpost.com/2026/11/26/tencent-dfly2-speculative-decoding-sparse-models/)** — The 0.85B, 5-layer draft model keeps no KV cache of its own: it reads the paired target layer's latent cache and attends only to positions the target's indexer already selected. Tencent reports 2.97x end-to-end on DeepSeek-V4.1-Flash, 2.36x on GLM-5.3-Flash and up to 81% more serving throughput at SWE 64K. *(MarkTechPost)*

## Hardware & Robotics

- **[Yandex to pilot package delivery with humanoids by the end of 2026](https://meduza.io/en/news/2026/11/27/russia-s-yandex-to-launch-delivery-using-humanoid-robots-kommersant-reports)** — The pilot pairs existing delivery rovers with humanoid robots: the rover carries an order to a building entrance, the humanoid brings it inside, solving stairs and thresholds. Analysts quoted by Kommersant call the humanoid stage a technology and branding exercise rather than a commercial venture. *(Meduza)*
- **[Chinese chipmakers clear Day-0 support for SenseTime's SenseNova Loop-9B](https://www.globaltimes.cn/page/202611/1375203.shtml)** — Accelerators from Biren, Cambricon, Hygon, Kunlunxin, Moore Threads, MetaX and Huawei's Ascend ran the model on launch day, pulling hardware-software co-adaptation earlier into the model development cycle. CAICT still flags closed architectures and heterogeneous-chip compatibility as the main obstacles. *(Global Times)*
- **[Intel Razor Lake-AX splits into on-package and on-motherboard lines, up to 52 cores and 192 GB](https://wccftech.com/intel-razor-lake-ax-2028-launch-mop-96-gb-mob-192-gb-memory-up-to-52-cores/)** — Leaked details show an MoP variant with up to 96 GB LPDDR5X on package at an 8+16+4 core layout, and an MoB variant with memory on the motherboard scaling to 52 cores and 192 GB. The parts target an early 2028 launch. *(Wccftech)*

## Tools & Startups

- **[Sentinel watches coding agents and grades them against their own git diffs](https://github.com/run-llama/sentinel)** — LlamaIndex's macOS tool monitors Claude, Codex, aider, Gemini CLI, opencode and Cursor sessions across terminal windows, compares each agent's claimed work to the real diff, and flags loops, off-track edits and sabotage using Gemini 4 Hydrogen. *(Hacker News)*
- **[LLM.OS runs Qwen3.5-2B fully in a browser tab on a 52 KB WebAssembly engine](https://tesseracted.com/experiments-llm-os/)** — Tesseracted Labs runs Qwen3.5-2B and Qwen3-0.6B entirely client-side on a Zig-compiled wasm32 engine of roughly 52 KB, hitting about 39 tok/s for the 2B model on an M3 Max. Weights download once and no inference API or GPU is involved. *(Hacker News)*
- **[Wizstar R1 launches AI digital ambassadors that replace on-camera product videos](https://www.producthunt.com/products/wizstar)** — The tool generates presenters that gesture naturally and keep lip sync through head turns and object occlusion, aimed at product updates and localized marketing videos. It topped Product Hunt's November 27 leaderboard with 273 points. *(Product Hunt)*
- **[Pushary routes coding-agent permission prompts to your phone](https://www.producthunt.com/products/pushary)** — Pushary forwards permission prompts and clarifying questions to the right person's phone or Mac and keeps an audit record of approvals, supporting Claude Code, Codex, Cursor, Gemini CLI and Hermes for single developers or whole teams. *(Product Hunt)*
- **[Depost AI scores past LinkedIn posts and plans the month for approval](https://www.producthunt.com/products/depost-ai)** — It benchmarks each published post against the account's own average, finds what performs in the user's niche, then drafts the month's posts and graphics before publishing through LinkedIn's official API. It also runs inside Claude and ChatGPT over MCP. *(Product Hunt)*

## Italia AI Spotlight

- **[indigo.ai launches self-improving agents and continuous fine-tuning for enterprise chatbots](https://www.startup-news.it/indigo-ai-agenti-modelli-ai-conversazionale/)** — Milan's indigo.ai announced self-improving agents that flag gaps after deployment, a Composer that lets operational teams change agents without developers, and continuous fine-tuning on each customer's own conversations. Changes still need team sign-off, a model it calls Human-in-the-Lead. *(Startup-News)*
- **[ReportAId turns medical reports into usable clinical data](https://www.economyup.it/startup/sanita-giuseppe-faraci-con-lai-possiamo-leggere-nei-referti-anche-la-domanda-di-cure-future/)** — Founded in 2024 by Giuseppe Faraci with Claudio Caletti and Luca Foresti, the startup extracts information already written in medical reports so it can drive follow-up scheduling, care continuity and clinical research. Faraci hit the problem inside the Santagostino clinic group. *(EconomyUp)*
- **[Politecnico di Milano team builds an organ-on-chip model of a head and neck tumour](https://www.latechmadeinitaly.com/organ-on-chip-deep-tech-made-in-italy/)** — Researchers led by Marco Rasponi combined patient tumour cells, fibroblasts, endothelial cells and sensory neurons in a hyaluronic-acid gel, published in PNAS with Swedish and US partners. It is a step toward patient-specific models for personalised therapy testing. *(La Tech Made in Italy)*
- **[Brainpull and Metamer put Salesforce Agentforce assistants on sales and customer care](https://forbes.it/2026/11/27/lintelligenza-artificiale-al-servizio-delle-imprese-brainpull-e-metamer-lanciano-the-human)** — The Puglia-based agency and the energy company integrated Electra for sales and Mia for customer care, and will present them at a closed-door workshop in Conversano on 3 December. Metamer is described as the only Italian company recognised at Dreamforce for its AI work. *(Forbes Italia)*

## Money & Markets

- **[Vector Singularity closes a Series A with Alibaba joining its neutral-atom quantum bet](https://techstartups.com/2026/11/27/startup-funding-news-today-november-27-2026-altair-semiconductor-zerith-vector-singularity-more/)** — The Beijing company, founded in May 2026, raised several hundred million yuan with Alibaba Group alongside the Beijing AI Industry Investment Fund and Zhongguancun Science City Fund - reported as Alibaba's first quantum computing investment. It is building rubidium- and ytterbium-based machines toward a first prototype in H1 2027. *(Tech Startups)*
- **[Profitable French startup Korben raises €10.2M for robots' brains](https://www.eu-startups.com/2026/11/profitable-french-startup-korben-raises-e10-2-million-to-give-europe-control-over-its-robots-brains/)** — Paris-based Korben raised €10.2M in seed at a €36.2M valuation, most of it from Tiresias Angels with Bpifrance adding €2M, for the software and AI platform that runs service robots. The company is already profitable. *(EU-Startups)*
- **[Zerith raises several hundred million yuan to commercialise robot manipulation](https://techstartups.com/2026/11/27/startup-funding-news-today-november-27-2026-altair-semiconductor-zerith-vector-singularity-more/)** — The Hefei startup, founded in January 2025, closed a round backed by Zero2IPO Capital, Xizhou International and local industrial funds for robotic picking and end effectors. It reports nearly 200 unattended retail installations and a Picking API due by year-end. *(Tech Startups)*
- **[Liying Biotechnology raises over RMB 100M Series A+ for AI protein design](https://techstartups.com/2026/11/27/startup-funding-news-today-november-27-2026-altair-semiconductor-zerith-vector-singularity-more/)** — Led by Haohe Capital with Guangming Science City and Nanjing Healthcare Fund, the Shenzhen company pairs computational protein design with automated cell-free production and physical testing. It claims validation throughput up from about 200 to 20,000 sequences per month. *(Tech Startups)*
