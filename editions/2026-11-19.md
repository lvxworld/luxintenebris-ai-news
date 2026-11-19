# Lux in Tenebris — AI dispatches · November 19, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 147 · https://luxintenebris.news/

## Lead Record IPO: Anthropic prices its IPO at $83 a share, raising a record $81.3 billion

Anthropic priced its initial public offering at $83.00 a share, above the $70-$78 range, raising roughly $81.3 billion in the largest stock market debut on record and valuing the AI lab at about $1.26-$1.41 trillion. Shares begin trading on the Nasdaq on Thursday under the ticker ANT, with the offering expected to close on November 20.

Source: [The Guardian](https://www.theguardian.com/technology/2026/nov/18/anthropic-share-price-stock-market-ipo)

## Top stories

### Google launches Gemini 4 Neon, a mid-tier model for coding and enterprise work

Gemini 4 Neon sits between the Carbon flagship and the fast Hydrogen tier, scoring 61 on the Artificial Analysis Intelligence Index and taking the top spot on the Coding Agent Index. It is priced at $3 per million input tokens and $15 per million output tokens with a 1M-token context, rolling out across the Gemini API, AI Studio, Antigravity and the Gemini app.

Source: [Google DeepMind](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/)

### NVIDIA posts a record $115.8B quarter as Vera Rubin NVL72 ships

Q3 FY2027 revenue rose 103% year over year to $115.8 billion, with data-center revenue up 110% to $107.6 billion. NVIDIA said its Vera Rubin NVL72 platform has shipped and guided Q4 revenue to about $130 billion, plus or minus 3%.

Source: [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-announces-financial-results-for-third-quarter-fiscal-2027)

### Microsoft says Maia 200 is in production running its largest models

At Ignite 2026, Microsoft said its second-generation Maia 200 accelerator is now in production running its largest models, delivering 1.7x more tokens per watt and 30% better performance per dollar. The company calls it its most efficient inference system to date.

Source: [Microsoft AI](https://microsoft.ai/news/microsoft-ignite-2026/)

## Research & Papers

- **[GateWatch turns an LLM probe into a compact Boolean circuit](https://arxiv.org/abs/2611.24619)** — GateWatch expresses a probe's entire decision rule as explicit Boolean logic over a few binarized sparse-autoencoder features. Across 24 tasks on Gemma-2-9B it lands within 1.17 points of full 16K-feature SAE probes while cutting probe memory by 99.98%, and inside vLLM it keeps 97-98% of baseline throughput with 1,000 concurrent classifiers. *(arXiv)*
- **[AutoPI red-teams LLM agents by technique coverage, not just attack success](https://arxiv.org/abs/2611.24313)** — Built on a taxonomy of prompt-injection techniques, the black-box, training-free red teamer writes an attack for every sub-technique and reworks the failures with judge feedback. Against Claude Haiku 5.5 it achieved 20-50% higher attack success and up to 400% higher class-level coverage than recent state-of-the-art adaptive attackers. *(arXiv)*
- **[Replay, don't resample: consolidating long-horizon RL experts from their own logs](https://arxiv.org/abs/2611.24059)** — Multi-expert replay policy distillation replays each expert's RL training rollouts through the student in the order the expert learned from them, recomputing the policy gradient on the logged prefixes. It consolidates experts at roughly a seventh of the compute used to train them and beats multi-teacher on-policy distillation from the same experts. *(arXiv)*
- **[RePlan-VLA adds progress-aware replanning to long-horizon robot policies](https://arxiv.org/abs/2611.23843)** — The VLA-agnostic framework monitors the robot's motion to evaluate progress and revises future plans on the fly, preserving the underlying policy with no extra fine-tuning. It lifts success by 21.9% on RoboCasa365 and 10.4% on CALVIN over the next strongest baseline, and was validated on a Franka Research 3 arm. *(arXiv)*
- **[Latent reasoning degrades past its useful horizon, a new method finds](https://arxiv.org/abs/2611.24001)** — Extending latent chain-of-thought to the full preset horizon can hurt reasoning, with later computation mainly reorganizing existing candidates. A lightweight estimator adjusts the latent horizon during inference, improving accuracy by up to 7.2 points while cutting latent computation by up to 29% without retraining. *(arXiv)*

## YouTube & Video

- **[Google launches Gemini Neon](https://www.youtube.com/watch?v=AbfheTIO2Ec)** — A hands-on look at Google's newest Gemini model going live in real use. *(YouTube - AI Tool Report)*
- **[Nvidia beats earnings expectations but Huang succession risk weighs on investors](https://www.youtube.com/watch?v=jBd2MORp2F0)** — Bloomberg Technology on Nvidia's quarter and the leadership-transition questions still hanging over the stock. *(YouTube - Bloomberg Technology)*
- **[Anthropic IPO draws historic demand as VC backers double down](https://www.youtube.com/watch?v=WQUNcwbvR38)** — Bloomberg Technology on the demand around Anthropic's listing and its venture backers adding to their positions ahead of the debut. *(YouTube - Bloomberg Technology)*

## Hardware & Robotics

- **[Boston Dynamics' Atlas lands its first non-automotive trial at a chipmaker](https://www.therobotreport.com/boston-dynamics-atlas-humanoid-lands-first-non-automotive-trial/)** — Atlas will begin trials at a major semiconductor manufacturer in early 2027, its first deployment outside the automotive industry and a milestone for humanoids in electronics manufacturing. *(The Robot Report)*
- **[NVIDIA funds SPIL lines for AI chip interposer wafers](https://www.techtimes.com/articles/331032/20261118/nvidia-chip-packaging-deal-funds-spil-lines-making-ai-chip-interposer-wafers-not-just-assembly.htm)** — NVIDIA struck a chip packaging deal with SPIL to fund lines for bumping, interposer wafer fabrication, assembly and testing. SPIL plans to triple its advanced packaging capacity as AI chip demand strains co-packaged capacity worldwide. *(Tech Times)*
- **[California DMV bars Waymo from operating on the state's freeways](https://www.therobotreport.com/california-dmv-bars-waymo-avs-from-operating-on-the-states-freeways/)** — The California DMV determined Waymo's freeway operations pose an imminent hazard to public safety and barred the robotaxis from state freeways, a significant regulatory setback for the largest US robotaxi operator. *(The Robot Report)*

## Tools & Startups

- **[Vercel opens a public beta of Board, a shared message board for agents](https://vercel.com/blog/introducing-vercel-board)** — Board is a shared and secure message board designed for communication between AI agents, announced on Vercel's blog and Show HN. *(Vercel)*
- **[ADE Index sources and ranks 975 agentic coding tools](https://adeindex.com)** — A new directory sourcing and ranking 975 agentic coding tools, aiming to be a single reference for comparing AI coding agents. *(ADE Index)*
- **[Pitot packs OpenTelemetry into one binary with Parquet, DuckDB and MCP](https://github.com/labstack/pitot)** — An open-source single-binary OpenTelemetry tool that stores traces as Parquet, queries them through DuckDB and exposes an MCP interface for agents. *(GitHub)*
- **[SpringRep open-sources a B-rep CAD kernel for robotics](https://springcraft-ai.github.io/springrep/)** — An open-source boundary-representation CAD kernel with 3,487 tests, released on the argument that robotics needs better CAD tooling. *(GitHub)*
- **[KradleBench runs multi-agent AI evals inside Minecraft](https://www.kradle.ai?1)** — A benchmark platform for running multi-agent AI evaluations inside Minecraft, launched on Show HN. *(Kradle)*
