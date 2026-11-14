# Lux in Tenebris — AI dispatches · November 14, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 142 · https://luxintenebris.news/

## Lead The Huang Vacancy: Nvidia's board courts Arm's Rene Haas as it hunts a permanent chief

Nvidia's board has approached Arm chief executive Rene Haas, a former Nvidia executive, as it searches for a permanent replacement for Jensen Huang, who resigned this week with CFO Collette Kress running the company as interim CEO and Harvey Jones installed as first board chair. The vacuum sits under the whole AI buildout: Nvidia's GPUs and its Isaac and GR00T stacks underpin most datacenter and humanoid robotics programs, and investors already expect Kress to be far more conservative with startup checks.

Source: [Tom's Hardware](https://www.tomshardware.com/pc-components/gpus/nvidia-board-reportedly-approached-arm-ceo-rene-haas-during-replacement-search-jensen-huangs-transgressions-leave-nvidia-scrambling-to-fill-a-massive-void)

## Top stories

### Mirendil raises a $1B Series A to build agents for scientific R&D

Kleiner Perkins and Clearlake Capital co-led the round, with Battery Ventures, Google, M13, Pear VC and S32 participating, taking the San Francisco frontier lab to roughly $1.2B raised including a $200M seed. It topped Crunchbase's ranking of the week's ten biggest US rounds.

Source: [Crunchbase News](https://news.crunchbase.com/venture/biggest-startup-funding-rounds-agentic-ai-infrastructure-mirendil-mercor/)

### inclusionAI ships Duo v1, an open full-duplex audiovisual world model

Duo pairs an autoregressive multimodal LLM that decides when to speak with a causal audiovisual diffusion transformer emitting synchronized video and audio in 0.71-second chunks. The release includes a four-step distilled variant and an FP8 build, with Apache-2.0 code and weights under the MiniMax H3 community license.

Source: [arXiv](https://arxiv.org/abs/2611.15131)

### ASUS unveils Gallop, a humanoid already packing parts on its own motherboard line

Co-CEO S.Y. Hsu showed a two-armed humanoid on a fixed base packing 15 motherboard accessories per board at an ASUS group EMS factory, targeting 99.5% success inside a 20-second cycle. It runs on a single NVIDIA Jetson AGX Thor with an in-house dexterous hand; pilots come in 2027 and availability in the second half of 2028.

Source: [ASUS Pressroom](https://press.asus.com/blog/factory-proven-physical-ai-asus-gallop-humanoid-robot/)

### llama.cpp and ggml hit v1.0.0 with a semantic-versioning promise

ggml-org tagged both libraries v1.0.0, committing to semver where a major bump means a breaking change to the public C API in ./include — a stability contract for the 150-plus supported architectures and every app linking libllama. Distribution now spans Docker, Debian, Homebrew, conda-forge, MacPorts, Winget and XCFramework, with CI scaled across NVIDIA, AMD, Qualcomm, Arm, IBM and Intel runners.

Source: [Hugging Face](https://huggingface.co/blog/ggml-org/llama-cpp-v1)

## Research & Papers

- **[Classical energies learn to reason 1,000x faster than looped models](https://arxiv.org/abs/2611.17309)** — A learned version of the 1980s Hopfield-Tank energy solves 99.996% of Sudoku-Extreme and 100% of Maze-Unique puzzles after 42 ms and 132 ms of training on one GPU, matching looped baselines at 282x fewer inference FLOPs. The authors warn that trivially solvable puzzles overstate what looped reasoning can scale to. *(arXiv)*
- **[FOAM halves SOAP's optimizer state and matches Muon-class wall-clock time](https://huggingface.co/papers/2611.16905)** — FOAM drops SOAP's output-side Kronecker factor and replaces the dense rotated second moment with a factored Adam-style estimator, using half the optimizer state. Across LLM pretraining from 124M to 760M parameters it matches SOAP and Muon on validation loss, with code released. *(Hugging Face)*
- **[UniSpark-9B pairs full and linear attention for multimodal understanding and generation](https://huggingface.co/papers/2611.16517)** — UniSpark-9B mixes full attention with GatedDeltaNet on a Mixture-of-Transformer-Experts backbone, training autoregressive text and visual flow matching together on 159.7M generation and 213.4M understanding samples. It scores 2470.3 on MME-S and 0.83 on GenEval while extending synthesis to 2K and supporting interleaved generation. *(Hugging Face)*
- **[Ropedia Xperience 2 captures environments and behaviors together for physical AI](https://huggingface.co/papers/2611.17060)** — The release adds 1,589 metric-scale 3D scans and 4,230 egocentric recordings of 74 tasks, 131 hours in total, with each capture converted into interactive simulation and human motion retargeted to whole-body robot trajectories. The team frames joint environment-plus-behavior capture as the data foundation for scaling laws in physical AI. *(Hugging Face)*

## Hardware & Robotics

- **[DeepX commits more than $100M to a Samsung 2nm AI chip aimed at robots](https://qz.com/deepx-samsung-ai-chip-robots-100-million-111326)** — The South Korean fabless startup handed its final DX-M2 blueprints to Samsung Foundry and expects first silicon by March 2027, with customer testing and mass production in 2028. The roughly 5-watt edge accelerator targets robotics, industrial machinery and AI PCs, betting inference moves onto devices. *(Quartz)*
- **[Model tracks more than 1.5 GW of export-banned Nvidia chips inside China](https://www.tomshardware.com/tech-industry/artificial-intelligence/mass-smuggling-of-nvidia-ai-gpus-could-be-the-underlying-cause-of-jensen-huangs-departure-analysts-claim-more-than-1-5-gigawatts-of-banned-chips-tracked-to-china-despite-export-controls)** — SemiAnalysis' Accelerator Model puts roughly 1.5 million restricted Nvidia GPUs — over 1.5 gigawatts of datacenter hardware — in China despite US export controls, covering Nvidia, AMD and custom ASIC vendors. Analysts tie the flow to the collapse of Jensen Huang's tenure. *(Tom's Hardware)*
- **[Daikin Applied designs 60 MW of cooling for Nvidia Vera Rubin factories](https://refindustry.com/news/daikin-applied-introduces-60-mw-cooling-architecture-for-ai-factories/)** — The D60-W architecture, built on Nvidia's DSX platform with Vera Rubin NVL72, carries a 60 MW IT load across six deployable units, with liquid cooling handling 92% of the heat. Oil-free magnetic bearing chillers up to 10 MW and dry coolers eliminate cooling-tower make-up water; the CDU and dry cooler ship in the second half of 2027. *(Refindustry)*
- **[Andy Rubin's Genki Robotics shows its humanoid to Japan's prime minister](https://www.humanoidsdaily.com/news/genki-robotics-humanoid-debut-takaichi-kantei)** — The Tokyo startup gave its full-size biped a first public appearance at Prime Minister Sanae Takaichi's physical AI meeting, with the unit assembled over a weekend and walking for the first time that Monday. Genki designs its own joint actuators and cameras, plans an Android-style open software platform and is talking to carriers about cellular connectivity. *(Humanoids Daily)*

## Tools & Startups

- **[Cognition launches Devin Apps, web tools built and hosted from Devin's cloud VM](https://devin.ai/blog/devin-apps)** — Describe an internal tool in a session and Devin builds it, then serves it at a stable URL with mandatory sign-in and access scoped to people, org or enterprise. Apps run on one machine that sleeps when idle and support any HTTP stack plus on-machine SQLite or Postgres — aimed at admin panels and dashboards, not high-traffic production. *(Devin Blog)*
- **[Brave Search API adds pay-per-query agent payments over x402](https://brave.com/blog/search-api-agentic-payments/)** — Brave made its Search API endpoints callable with on-demand USDC payments settled on Base, so agents can query search without an account or key. Unpaid requests return HTTP 402 with the price, and LLM Context or web search runs at $0.005 per request with a receipt attached. *(Brave)*
- **[Simular launches box, a cloud Linux desktop agents drive over MCP](https://box.simular.ai/)** — box gives ChatGPT, Claude, Claude Code, Codex, Cursor and others a persistent cloud Linux desktop through one hosted MCP server, so agents can open browsers, click, type, read the screen and run terminal commands. Setup is one npx command, the computer is free per account and sleeps between sessions, with model calls billed against daily credits. *(Simular)*
- **[FAA rolls out AI air traffic tool to every control center days before a national ground stop](https://nypost.com/2026/11/13/us-news/faa-launched-new-ai-smart-tool-to-all-air-route-traffic-control-centers-just-days-before-nationwide-ground-stop/)** — The agency deployed SMART, a system meant to move traffic management from reactive to predictive, to all air route traffic control centers. The rollout became a story when a rare nationwide ground stop halted flights on Friday; the FAA and the Transportation Secretary said SMART did not cause it. *(New York Post)*

## Italia AI Spotlight

- **[Le Village by CA Campania opens in Naples to connect AI startups and corporates](https://startupitalia.eu/startup/a-napoli-le-village-by-ca-campania/)** — Crédit Agricole Italia inaugurated its sixth Italian innovation accelerator, with six startups and six corporate partners already on board. The hub targets AI and foodtech ventures in a region with more than 1,600 innovative startups, second in Italy after Milan. *(StartupItalia)*
- **[University of Salerno team builds a digital twin of the Amalfi Coast](https://www.latechmadeinitaly.com/costiera-amalfitana-digital-twin-tech-made-in-italy/)** — The Medusa project combined satellite observations, environmental data and mathematical models to model coastal erosion and landslide risk on the Amalfi Coast, funded by the Italian Space Agency through PNRR resources. It is now being adopted by the local fishing consortium Gal Pesca Approdo di Ulisse. *(La Tech Made in Italy)*
- **[Milan's bid to host a UN AI assessment pillar advances under the Radegonda project](https://www.economyup.it/blog/il-pilastro-onu-sullai-a-milano-raccontato-da-chi-e-coinvolto-nel-progetto-radegonda/)** — The MilanoAI committee, backed by Assolombarda, Confcommercio, local institutions and every Milan university, is campaigning to host a UN technical pillar for independent evaluation and ethical governance of AI. Organisers cite Milan holding 68% of Italy's installed datacenter capacity as the infrastructure case. *(EconomyUp)*
- **[Confcommercio Milano publishes Italy's first AI code of conduct for businesses](https://www.ai4business.it/sicurezza/da-confcommercio-milano-il-primo-codice-di-condotta-sulluso-dellai/)** — The code, drafted by an Asseprim working group, turns EU AI Act and privacy rules into operational guidance for member companies on confidential data, accountability for AI decisions and business continuity if a tool stops working. *(AI4Business)*

## Money & Markets

- **[Q-CTRL raises $290M Series C led by Salesforce Ventures and crosses $1B valuation](https://techstartups.com/2026/11/13/startup-funding-news-today-november-13-2026-mirendil-langchain-luminal-kindo-q-ctrl-more/)** — Bullhound Capital, Affinity Partners, AMD Ventures, Lockheed Martin Ventures and In-Q-Tel joined the round for the Sydney quantum-infrastructure software company, which is valued above $1B. The money funds AI-driven quantum control software and GPS-free navigation. *(Tech Startups)*
- **[Nvidia's pause on startup checks threatens to blast a hole in AI funding](https://techcrunch.com/2026/11/13/jensen-huangs-departure-blasts-big-hole-in-ai-startup-funding-vcs-and-founders-say/)** — After Jensen Huang's resignation, investors expect interim CEO Colette Kress to be far more conservative with startup checks. Nvidia and NVentures joined 105 to 121 rounds in 2026, often as the largest investor, so a slowdown hits neoclouds, inference providers and open-weight labs hardest — especially in Europe. *(TechCrunch)*
- **[Drogue raises $20M to power floating AI data centers with ocean thermal energy](https://techcrunch.com/2026/11/13/this-young-startup-wants-to-power-floating-data-centers-with-the-oceans-heat-and-investors-are-already-on-board/)** — XYZ Venture Capital, Toyota Ventures, Tamarack Global, Boost VC and Slow Ventures are among the backers of the Washington DC startup, which uses ocean thermal energy conversion to run multi-megawatt datacenters on ships. A first prototype is targeted for early 2028. *(TechCrunch)*
- **[Czech startup ValkaAI extends pre-seed to €13M for real-time generative personas](https://www.eu-startups.com/2026/11/czech-startup-valkaai-extends-pre-seed-round-to-e13-million-to-bring-ai-personas-to-live-events-at-scale/)** — Look AI Ventures and ff Venture Capital backed the extension, adding to a €12M pre-seed led by Rockaway Ventures earlier in 2026. The Prague deeptech builds generative AI that lets digital personas react to live events, starting with sports broadcasting. *(EU-Startups)*
