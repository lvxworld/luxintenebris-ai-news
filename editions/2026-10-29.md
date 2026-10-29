# Lux in Tenebris — AI dispatches · October 29, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 126 · https://luxintenebris.news/

## Lead Frontier launch: Google DeepMind launches Gemini 4 Carbon, its new frontier flagship

Google DeepMind announced Gemini 4 Carbon, described as its strongest model yet with state-of-the-art cybersecurity and long-horizon capabilities, including reliable multi-day coding tasks. Access is initially limited to a group of cyber defenders while safety guardrails are iterated.

Source: [Google DeepMind](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/)

## Top stories

### Upwind raises $400M after walking away from a Datadog acquisition offer

The cloud and AI security platform closed a $400M Series C at a $3.8B valuation led by Bessemer Venture Partners, with revenue quadrupling in 2026. The round funds product development and go-to-market expansion.

Source: [TechCrunch](https://techcrunch.com/2026/10/28/upwind-raises-400m-after-walking-away-from-datadog-acquisition-offer/)

### Study: roughly 24% of crawlable web pages now contain AI-generated text

An analysis of over 5 million pages between 2019 and 2026 estimates about 24% carried AI-generated or AI-edited text by August 2026, with growth accelerating. The rise concentrates on low-authority 'edge' pages, while .gov/.edu domains remain far cleaner.

Source: [X — study authors](https://x.com/i/status/2115497580746719303)

### Tencent open-sources Hy-Nomas, a free-form interactive world generation model

Tencent's Hunyuan team open-sourced Hy-Nomas, an interactive world generation model positioned as comparable to DeepMind's Genie 4. It ships with a Hugging Face paper, a Space demo, and a public playable demo with no waitlist.

Source: [@_akhaliq](https://x.com/_akhaliq/status/2115563792180588875)

### Amazon unveils EMMA, a self-improving multi-agent framework

EMMA treats routing memory, agent prompts and skills as episodic memory, with a reflector assigning scoped fixes after failures. It reportedly outperforms ACE, GEPA, EvoMAS and ADAS by up to 32.5% while using 17–38% fewer training executions.

Source: [omarsar0](https://x.com/omarsar0/status/2115438189901181296)

## Research & Papers

- **[A scaling law for tool-use agents, from 849 models trained in synthetic environments](https://arxiv.org/abs/2610.37648)** — SynthAPI is a pipeline for synthetically generating tool-use environments, and the paper derives scaling laws showing how data composition in these environments drives multi-step tool-use agent performance. *(arXiv)*
- **[Timestral: four time-series foundation models sweep forecasting benchmarks](https://huggingface.co/papers/2610.37585)** — A family of four forecasting models (5M–209M parameters) sets a new state of the art on GIFT-Eval, TIME and fev-bench, with the 209M and 123M variants taking the top two spots on every metric. *(HuggingFace)*
- **[Metacognitive decoding makes diffusion language agents cheaper to run](https://arxiv.org/abs/2610.37642)** — A metacognitive controller for diffusion language models adaptively allocates computation and controls generation length, improving the efficiency of parallel-token agent inference. *(arXiv)*
- **[Label-free RLVR improves reasoning, then collapses](https://arxiv.org/abs/2610.37553)** — The paper shows self-reinforcing RLVR initially improves reasoning but eventually collapses: self-assessed reward saturates while accuracy falls, often degenerating to a single answer across all questions. *(arXiv)*
- **[MuonGS: relaxed weight-norm control improves LLM pretraining](https://arxiv.org/abs/2610.37647)** — An analysis of weight-norm control in the Muon optimizer across the full training trajectory yields relaxed norm-constraint schemes that improve pretraining performance. *(arXiv)*

## Hardware & Robotics

- **[Altera launches Agilex 27, first FPGA family in its new Agilex 2X portfolio](https://www.servethehome.com/altera-agilex-27-800gbe-1-6tbe-hyperflow/)** — The Agilex 27 pairs hardened 800GbE and 1.6TbE Ethernet with PCIe 6.0 and 7.0 support and configurable transceivers up to 256 Gbps for bandwidth-intensive datapath, beamforming and RF workloads. *(ServeTheHome)*
- **[CXMT to start HBM3E mass production by end of 2026](https://www.techpowerup.com/354226/cxmt-to-start-hbm3e-mass-production-by-the-end-of-2026)** — The Chinese memory maker said it will begin mass production of HBM3E by the end of 2026, a notable step for the domestic AI chip supply chain as it also enters LPDDR6 risk production with 12.8 Gbps chips. *(TechPowerUp)*
- **[NVIDIA GeForce RTX 5080 reaches nearly $2,000 across U.S. retailers](https://www.techpowerup.com/354216/nvidia-geforce-rtx-5080-reaches-nearly-usd-2-000-across-u-s-retailers)** — The card is now listed at close to $2,000 at Best Buy, Micro Center, Amazon, Newegg and B&H — well above MSRP — reflecting persistent pricing pressure amid AI-driven demand. *(TechPowerUp)*

## Tools & Startups

- **[Local Code: run DeepSeek 4.1 Flash coding models fully locally on Macs](https://github.com/drawthingsai/local-code-community)** — Draw Things released Local Code, an open-source community project to run DeepSeek 4.1 Flash coding models entirely on Apple Silicon. *(GitHub)*
- **[A full Python 3.15 implemented in 25,000 lines of C11](https://news.ycombinator.com/item?id=50281226)** — A Show HN project presents a complete Python 3.15 interpreter written from scratch in roughly 25,000 lines of C11, an unusually compact independent implementation. *(Hacker News)*
- **[Enframe wraps any OpenAPI spec into an MCP server](https://github.com/erwinkramer/enframe)** — Enframe is a drop-in sidecar that turns any existing OpenAPI specification into a Model Context Protocol server, making legacy APIs agent-ready. *(GitHub)*
- **[Fengarde: OCSF-native open-source SIEM with local AI triage](https://supermhel.github.io/fengarde/)** — An Apache-2.0 licensed, OCSF-native open-source SIEM that performs alert triage with locally running AI models. *(GitHub Pages)*
- **[Tilde: an open-source registry for discovering and sharing AI agents](https://github.com/trytilde/tilde)** — Tilde (~) is a new open-source registry for AI agents, launched as a Show HN project. *(GitHub)*
