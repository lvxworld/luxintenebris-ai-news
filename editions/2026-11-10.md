# Lux in Tenebris — AI dispatches · November 10, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 138 · https://luxintenebris.news/

## Lead Frontier Release: Anthropic splits its frontier model in two with Claude Fable 5.2 and Mythos 5.2

Anthropic shipped Fable 5.2 and Mythos 5.2 as two tiers of the same frontier model: Fable is broadly available under standard safeguards, while Mythos goes out with reduced safeguards for vetted cybersecurity and life-sciences organizations. Both are priced at $8/$40 per million input and output tokens, with an optional fast mode at $16/$80, and Anthropic says output is up to 30% faster than the 5.1 versions. The company claims Fable 5.2 at high effort roughly matches Opus 5.5 at max effort at about half the cost per task.

Source: [Anthropic](https://www.anthropic.com/claude-fable-and-mythos-5-2)

## Top stories

### OpenAI's Control Room can halt model output within 35 seconds

OpenAI detailed Control Room, an internal system that tracks every research inference workload, including agentic sampling for training and evaluation, and stops model output within 35 seconds of an intervention decision. It is already deployed and designed to fail safe if the system itself goes down.

Source: [OpenAI](https://openai.com/index/control-room)

### Google adds TPU 8tx and TPU 8i Max, its fourth TPU system this year

TPU 8tx pairs 8t silicon with custom fifth-gen AMD EPYC Turin hosts for confidential inference, while TPU 8i Max stacks two 8i chips in one package for 384 GB of HBM at 17.2 TB/s. It is the first year Google has introduced four TPU systems, and the company says TPUs now serve nearly 100 customers.

Source: [Google](https://blog.google/innovation-and-ai/infrastructure-and-cloud/global-network/tpu-8i-max-and-8tx/)

### Claude Fable 5.2 designed three working electronic devices end to end

Anthropic says the new model produced schematics, PCB layouts, 3D-printable enclosures, firmware and parts lists for a USB speakerphone, a voice-assistant hub and a handheld virtual pet. Partner Diode Computers built the boards, and all three prototypes worked without circuit fixes.

Source: [Anthropic](https://www.anthropic.com/research/claude-electronics-design)

## Open Source & Models

- **[qwen-concept-27b gains coding and reasoning from nine rewritten weight matrices](https://x.com/conceptcountry/status/2119832078531596770)** — Concept Country released a weight-space-edited build of Qwen3.8-27B with no gradients and no training data, reporting +13 points on LiveCodeBench v6, +4.3 on GPQA Diamond and 27-54% fewer thinking tokens. Weights are on Hugging Face under Apache 2.0 with GGUF quants around 16GB. *(@conceptcountry)*
- **[Ant Group's Robbyant open-sources a tactile foundation model on 5,000 hours of touch](https://x.com/robbyant_brain/status/2119870554056651004)** — LingBot-Touch is a JEPA-style haptic transformer that unifies magnetic, piezoresistive and visuotactile sensors into shared tactile tokens, pretrained on roughly 4,983 hours of real manipulation data. Under Apache 2.0, with a 5.46M-parameter Tiny variant for real-time use, it improved success across 26 real-robot tasks and transfers zero-shot to unseen sensor types. *(@robbyant_brain)*
- **[Unverified 14T-parameter 'numbat' checkpoint appears on Hugging Face](https://x.com/kofservicesinc/status/2119536392204169438)** — A repo named burner22 uploaded a roughly 7.72 TB checkpoint described as a mid-pretraining snapshot of Anthropic's rumored Mythos-class run, with a reference PyTorch loader. The claim is unconfirmed, Anthropic has not commented, and the upload is unofficial. *(@kofservicesinc)*
- **[h0 ships as a dependency-free agentic coding harness with durable 'fittings'](https://x.com/parkerbrowndev/status/2120035799916048791)** — Developer Parker Brown released h0, a Python terminal harness that generates project-specific fittings to improve small and local models, with published evals against Claude Code and opencode. Runs are sandboxed with bubblewrap, network off by default, and any OpenAI-compatible endpoint works. *(@parkerbrowndev)*

## Hardware & Robotics

- **[NVIDIA launches GR00T 2, a 2B world action model trained on 100,000 hours of human video](https://blogs.nvidia.com/blog/robotics-simulation-advancements-corl/)** — At CoRL in Austin, NVIDIA introduced GR00T 2, built on Cosmos, which predicts future video frames alongside robot actions and hit 71% average success across 50 tasks from one demonstration, 95% from five. It also shipped Isaac Lab 3.0 with Newton physics at up to 2.5x the throughput of Isaac Lab 2.3, plus DexBench and VABAR, with GR00T 2 weights promised as open source in December. *(NVIDIA Blog)*
- **[Boston Dynamics puts scooter wheels on Atlas to test whole-body control](https://www.therobotreport.com/boston-dynamics-adds-wheels-to-atlas-humanoid-to-test-whole-body-control/)** — Off-the-shelf scooter rims were mounted on Atlas's existing ankle actuators via a single custom adapter, letting the humanoid roll on flat ground and switch to legged motion over obstacles under one reinforcement learning policy. The company calls it a research testbed, not a product. *(The Robot Report)*
- **[Huawei ships desktop PCs on its own 10-core Kirin X90 and HarmonyOS](https://www.tomshardware.com/tech-industry/huawei-develops-entirely-chinese-homegrown-desktop-pc-system-features-10-core-20-thread-kirin-x90-consumer-cpu-and-huaweis-own-harmonyos-operating-system-but-western-supply-chain-lingers)** — The Qinyun HM650 and HM650g run a 10-core Armv8 Taishan design in a 4+4+2 layout with SMT for up to 20 threads, a Maleoon GPU and an integrated NPU on HarmonyOS Enterprise Edition with Huawei's own kernel. TechInsights teardowns indicate SMIC's 7nm-class N+2 process. *(Tom's Hardware)*
- **[Epoch AI proposes an Inference Performance Index to replace FLOP/s comparisons](https://epoch.ai/publications/inference-performance-index)** — The index scores accelerators by how many concurrent requests they serve across a range of output speeds, accounting for memory and inter-chip communication rather than arithmetic throughput. Epoch estimates GB300 delivers about 25x H100's inference capacity per chip on modelled agentic workloads despite only 2.5x the 8-bit FLOP/s. *(Epoch AI)*

## Tools & Startups

- **[Nous Research opens Hermes Cloud agents that run 24/7 in their own container](https://x.com/NousResearch/status/2119851439904510217)** — Hermes Cloud agents keep full Hermes Desktop feature parity, including chats, group chats, plugins and settings, plus scheduled jobs, and are reachable from browser or mobile. Higher-tier plans include one free cloud agent. *(@NousResearch)*
- **[AWS ships Nitro Sandboxes to isolate AI agents per pod](https://aws.amazon.com/about-aws/whats-new/2026/11/nitro-sandboxes-eks-ecs-ec2/)** — Nitro Sandboxes are generally available on EKS, ECS and EC2, giving each opted-in pod or task its own lightweight VM enforced by the Nitro hypervisor at no extra charge. AWS explicitly targets agentic workloads running LLM-generated code, and on EKS Auto Mode it is a one-line pod spec change. *(AWS)*
- **[Expo open-sources Exact, an agent-native cross-platform UI framework](https://github.com/expo/exact)** — Exact is an MIT-licensed runtime that runs one UI written in a small declarative language called Contract natively on web, macOS, iOS and Linux, with data logic in TypeScript or Rust. It is built so coding agents can build, run, observe and test apps; in a demo Claude Code shipped a tested todo app on three platforms in about 57 minutes. *(GitHub)*
- **[MCP1 puts every MCP server behind one URL](https://www.producthunt.com/products/appwrite)** — The Appwrite gateway connects Claude Code, Cursor, ChatGPT and Codex once each, keeping tokens out of per-tool config files, with a catalog of 154 servers, optional read-only mode and approval gating for destructive tools. Free for one person, $12 per seat for teams. *(Product Hunt)*
- **[Medium opens TK Notebook to all writers with an inline AI assistant](https://www.unite.ai/medium-opens-tk-notebook-to-writers-with-inline-ai-assistance/)** — TK, Medium's private notebook and writing app, is now free with a Medium account after an invite-only phase, with an @TK assistant embedded in the editor plus AI feedback and archive features. *(Unite.AI)*

## Italia AI Spotlight

- **[Milan bids to host a new UN pillar for independent AI evaluation](https://www.ilgiorno.it/milano/cronaca/intelligenza-artificiale-ai-onu-vquc5sim)** — The MilanoAI committee of AmCham Italy, Assolombarda and Confcommercio asked the government and parliament to back Milan as host of a UN pillar for independent assessment and ethical AI governance. The proposal, Project Radegonda, lists four first-year functions and would hold no normative or sanctioning powers. *(Il Giorno)*
- **[University of Turin launches AI@UniTO district with €1.8M for AI spin-offs](https://www.torinocronaca.it/news/torino/725801/nasce-a-torino-il-distretto-dell-ai-ecco-il-progetto-che-vuole-cambiare-universita-e-imprese.html)** — The three-year programme with Fondazione Compagnia di San Paolo covers training, research, an AI Data Foundry and technology transfer aimed at creating AI companies, plus a new master's in AI and high-performance computing. It targets local strengths in manufacturing, med-tech and physical AI. *(Torino Cronaca)*
- **[Twelve Italian startups pitch for €110K at Trentino Startup Valley demo day](https://www.lapiazzaweb.it/news/attualita/823642/trento-12-startup-si-sfidano-al-demo-day-in-palio-110mila-euro-per-le-idee-piu-innovative.html)** — Finalists from the seventh edition presented at Trento's ITAS Forum on 9 November across innovation, social impact and research valorisation categories, with pitches spanning robotics, AI, cybersecurity, biotech and energy. The programme drew 89 applications and admitted 31 projects. *(La Piazza Web)*
- **[Rome deep-tech startup SOMA builds AI digital twins for aerospace design](https://www.corrierenazionale.net/2026/11/09/dallaerospazio-allindustria/)** — Founded by researchers from Università Niccolò Cusano, the 15-person team builds digital twin platforms for aerospace, defence and industrial manufacturing to cut design times and reduce European dependence on non-EU software. It works with CNR and the German Aerospace Center and has deployed its METIS assistant at its founding university. *(Il Corriere Nazionale)*

## Money & Markets

- **[Nominal raises $240M Series C at $3B as AI hardware testing demand surges](https://techcrunch.com/2026/11/09/ai-hardware-startup-nominal-triples-valuation-to-3b-in-8-months/)** — Lightspeed led and Insight co-led the round, tripling the Austin company's valuation from $1 billion in March 2026. Nominal sells an AI platform for engineering and testing aircraft, nuclear reactors and smart factories, counts Anduril and HII among 80+ customers, and holds a $71.2M Air Force STRATFI award. *(TechCrunch)*
- **[Onodrim Industries hits $1.3B valuation on a $300M Series A for European defence](https://tech.eu/2026/11/09/onodrim-industries-hits-13b-valuation-with-300m-series-a-to-strengthen-european-defence/)** — Lux Capital led the Amsterdam round for the Palantir-alumni venture, which takes controlling stakes in European aerospace, defence and industrial supply-chain businesses and modernises their manufacturing with permanent capital. First acquisitions are expected within months, with new offices in Munich and Turin. *(Tech.eu)*
- **[Spines raises $64M to automate book publishing with AI agents](https://fortune.com/2026/11/09/publisher-spines-raises-64-million-in-new-funding-to-accelerate-effort-to-automate-book-publishing-with-ai-agents/)** — The hybrid publisher split the raise between a $29M Series A-1 led by Zeev Ventures and a $35M non-dilutive facility from Twelve. Agents edit and translate manuscripts, design covers, produce audiobooks and market titles alongside human staff, on a $50M annual revenue run rate up 400% year over year. *(Fortune)*
- **[Coframe closes $25M Series A for websites that improve themselves](https://www.unite.ai/coframe-raises-25m-series-a-bringing-total-funding-to-35m/)** — Khosla Ventures and Hanabi Capital co-led the round, taking total funding to $35 million for a company whose agents handle strategy, design, engineering, QA and data analysis on customer sites and ads. Dropbox, Block and BCG are customers, and leaders from OpenAI, Anthropic and Google DeepMind joined as angels. *(Unite.AI)*
