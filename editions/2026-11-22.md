# Lux in Tenebris — AI dispatches · November 22, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 150 · https://luxintenebris.news/

## Lead Amazon's world-model bet: Amazon nears a $7.5B deal to acquire world-model startup Decart

Amazon is in advanced talks to acquire Israeli startup Decart for about $7.5 billion, with an announcement possible as soon as next week, according to the Financial Times. The price roughly doubles the $4 billion mark Decart set in May and would hand Amazon a real-time world-model and optimization stack that runs across Nvidia GPUs, Google TPUs and its own Trainium chips.

Source: [Financial Times via Seeking Alpha](https://seekingalpha.com/news/4675396-amazon-nears-75b-deal-buy-ai-start-up-decart)

## Top stories

### Lean FRO and Mathlib issue a joint statement on the 17-million-line verification of a Riemann proof

The Lean FRO and the Mathlib Initiative published a joint statement on the Lean verification of a Riemann Hypothesis proof released on November 20 by Anthropic mathematician Levent Alpoge — a 17-million-line library built with Claude. A competing all-human draft released the same day by Stanford researchers was already being flagged for problems.

Source: [X — @dotey](https://x.com/dotey/status/2124282068284699051)

### NVIDIA's Rubin HPC GPU carries more than 50,000 CUDA cores, ships in 2028

Announced at SC26, Rubin HPC joins the Vera Rubin platform as a science-focused accelerator with more than 50,000 CUDA cores — nearly triple the RTX 5090's 21,760 — plus sparse-data acceleration and seventh-generation NVLink. Deployed systems are targeted for 2028, with no independent performance data yet.

Source: [TechRadar](https://www.techradar.com/pro/nvidia-finally-reveals-new-rubin-gpu-with-almost-3x-more-cuda-cores-than-the-nvidia-rtx-5090-but-you-will-have-to-wait-till-2028-to-grab-it)

### Rapidus has yet to show working 2nm SRAM, putting its 2027 mass production at risk

Bloomberg reports the Japanese government-backed foundry missed a milestone due this summer — working SRAM cells on its 2nm-class GAA node — while also fighting cleanroom contamination. Rapidus insists it remains on track for mass production in the second half of fiscal 2027.

Source: [Tom's Hardware](https://www.tomshardware.com/tech-industry/semiconductors/rapidus-reportedly-struggles-to-produce-working-sram-on-its-2nm-node-putting-2027-mass-production-at-risk-company-faces-significant-challenges-using-euv-to-develop-gaa-transistors)

### Trump threatens to bar or tax US companies that build AI data centers abroad

At a White House news conference Trump said he wants to stop US firms from building AI data centers overseas, or impose a "tremendous tax" on those that do, arguing China would otherwise capture the capacity. No rate, timeline or legal mechanism was given, and no executive order has been issued.

Source: [Tom's Hardware](https://www.tomshardware.com/tech-industry/data-centers/trump-wants-to-ban-us-companies-from-building-overseas-data-centers-as-bans-slow-development-also-considers-putting-a-tremendous-tax-in-lieu-of-prohibition)

## Research & Papers

- **[ForceHarness gives frozen API models a sense of touch, lifting zero-shot arm success from 3.3% to 90%](https://arxiv.org/abs/2611.21099)** — A harness lets API-only frozen multimodal models use contact force without demonstrations or fine-tuning, via self-terminating force primitives and a physics translation layer that converts force traces into physical quantities. On a real arm with no wrist force sensor it adds 17.5 points on ForceBench and 34.3 points on the new HiddenPhys benchmark. *(arXiv)*
- **[VideoNexus splits video perception across sub-agents that report evidence, not transcripts](https://arxiv.org/abs/2611.21392)** — A training-free framework separates detailed video perception into sub-agents with independent contexts that return compact temporally grounded evidence to a planner. With Gemini 3.8 Flash in both roles it reaches 88.6% on full LVBench at 44% of the cost of built-in agentic processing. *(arXiv)*
- **[TCP4D tracks and generates robot tool-center-point motion in one 4D representation](https://arxiv.org/abs/2611.23143)** — A single 4D scene representation both tracks observed tool-center-point motion in SE(3) and generates future trajectories, with a cross-embodiment pipeline that retargets RGB video into demonstrations. It hits 7.60mm trajectory error on DROID, adapts to a new embodiment from ten demos and reaches 69.19% mean success on RoboTwin. *(arXiv)*
- **[M3OPD-Reasoner: an open recipe for post-training multimodal reasoning](https://arxiv.org/abs/2611.23034)** — Comparing recipes from Qwen3.5-9B across 21 decontaminated benchmarks, multi-teacher on-policy distillation of GSPO teachers wins, matching each teacher in its own domain and beating mixed-training baselines. Stacking MixRL on the distilled student adds further gains without collapse, and all data, code and checkpoints are released. *(arXiv)*
- **[Do LLM agents still need to be told how to self-improve?](https://arxiv.org/abs/2611.23219)** — Give a frozen agent primitives, a compute budget and only a general goal, and sufficiently capable models design their own self-learning algorithm — converging on strategies that match classic self-regulated learning frameworks. The learned text artifacts transfer across game horizons, mechanics and 3D navigation. *(arXiv)*

## Hardware & Robotics

- **[SoftBank's Son explored a $1 trillion buyout of SK hynix, then dropped it](https://asianomist.com/article/softbank-chief-approached-lenders-sk-hynix-acquisition-before-dropping-plan)** — Son approached Wall Street institutions about financing an acquisition of the South Korean HBM supplier at roughly $1 trillion, according to The Information. SoftBank says the proposal is no longer under active consideration and SK hynix says it received no formal approach. *(Asianomist)*
- **[Medtronic's Hugo surgical robot cleared by the FDA for general surgery](https://www.therobotreport.com/medtronics-hugo-surgical-robot-ready-for-bigger-operation/)** — The FDA cleared Medtronic's modular, cart-based Hugo system for upper and lower abdominal procedures including cholecystectomy, gastric bypass, hernia repair and appendectomy — indications covering roughly 3.5 million US surgeries a year. Medtronic paired European clinical data from its 2022 CE mark with a US trial to win the broader clearance. *(The Robot Report)*
- **[Phison previews an enterprise SSD that runs AI frameworks on its own NPU](https://www.techpowerup.com/355089/phison-previews-an-ssd-that-runs-ai-frameworks-on-its-own-npu)** — Shown at SC26, the computational-storage design pairs an NPU with 64GB of onboard memory at 130GB/s and supports PyTorch, vLLM, OpenVINO and llama.cpp. Phison claims it can cut data transfers 10-100x by processing datasets in parallel on the drive, though controller, interface and form factor remain undisclosed. *(TechPowerUp)*
- **[Inference now drives two-thirds of AI workloads, and the chip mix is following](https://siliconangle.com/2026/11/21/inference-two-thirds-ai-workloads-chip-deployment-positron-sc26/)** — Positron AI's Cameron McCaskill told theCUBE at SC26 that the training/inference split has flipped from roughly 85/15 toward training in 2023 to about one-third training today. The inference chipmaker builds around commodity memory instead of scarce HBM, with a single server drawing about 4,500W and a full rack under 40kW. *(SiliconANGLE)*
- **[Bot Auto launches a freight network with 200 million miles of driverless commitments](https://roboticsandautomationnews.com/2026/11/21/bot-auto-launches-capacity-grid-with-agreements-for-200-million-miles-of-driverless-trucking/107423/)** — The Houston-based company unveiled a Capacity Grid that lets shippers and brokers reserve autonomous trucking by the mile at agreed routes, schedules and prices, including 50 million miles from FreightVana. Bot Auto owns and operates its own driverless fleet rather than selling driving systems. *(Robotics & Automation News)*

## Tools & Startups

- **[Exa ships Websets V2: web datasets 4x faster and about half the price](https://www.producthunt.com/products/exa-ai)** — Websets V2 builds large structured datasets from plain-English queries with 4x faster jobs, roughly half the cost per result and about 20% better matching accuracy and recall. Exa also drops subscription tiers for pay-as-you-go credits and opens API access to everyone. *(Product Hunt)*
- **[Zero C# compiles C# into tiny native binaries with no runtime and no GC](https://news.ycombinator.com/item?id=50590279)** — An MIT-licensed fork of bflat compiles C# straight into small native executables with no runtime and no garbage collector, aimed at developers willing to manage memory by hand. The Show HN post drew about 150 points and more than 100 comments. *(Hacker News)*
- **[Stitch Loop: a Google Labs agent that ships its own fixes and checks the metrics](https://www.producthunt.com/products/stitch-loop)** — Stitch Loop connects to a GitHub repo and live product metrics, proposes changes, opens pull requests and then checks whether the numbers actually moved. Access is waitlist-only. *(Product Hunt)*
- **[gitroots gives coding agents path-level permissions on GitHub](https://www.producthunt.com/products/gitroots)** — gitroots scopes each developer or agent to only the repo paths it needs, with separate read and write rules, approval routing for out-of-scope changes and an audit trail that covers reads as well as writes. *(Product Hunt)*
- **[KeepPlain carries session memory across Claude Code, Codex and Cursor](https://github.com/keepplain/keepplain-plugin)** — An open plugin keeps coding-agent session history so agents can resume work across tools, mines recurring corrections into rules and runs `keepplain blame` to attribute a line of code to the session that wrote it. It reads sessions from Copilot CLI, Gemini CLI, OpenCode, Cline and Goose, free for personal use. *(GitHub)*

## Italia AI Spotlight

- **[Venice spin-off Rara Factory wins Startup Marathon 2026 with AI-discovered rare-earth alternatives](https://www.ilnordest.it/economia/imprese/nuovi-materiali-per-sostituire-le-terre-rare-rara-factory-vince-startup-marathon-2026-jys9yro3)** — RARA Factory, a deep-tech spin-off of Ca' Foscari University of Venice, took first place at the seventh Startup Marathon run by Area Science Park, UniCredit Start Lab and Fondazione Comunica in Milan. Its platform pairs physics-guided AI with experimental synthesis to find materials that replace rare earths, earning pre-selection for Italy's mission to CES in Las Vegas. *(il Nord Est)*
- **[A new human-centric AI trade fair heads for Pompeii in April 2027](https://cronachesalerno.it/nasce-la-fiera-dellintelligenza-artificiale-governata-dalluomo/)** — Organisers opened the road to the third Human Driven AI Summit, scheduled for 16-17 April 2027 in Pompeii with an exhibition area for Made in Italy AI companies. The first stop at the University of Salerno also brought a Campania regional bill creating an AI observatory (ORIAC). *(Le Cronache)*
- **[Only 13.84% of Italy's innovative startups are women-led, and AI lags further behind](https://www.robadadonne.it/249124/donne-startup-deeptech-italia/)** — Women lead about 1,684 Italian innovative startups, 13.84% of the national total — a share essentially unchanged for years — with AI and deep tech lower still. Only 14% of Italian venture capital general partners are women, despite EU funding such as Women TechEU and FoundHer. *(Roba da Donne)*
