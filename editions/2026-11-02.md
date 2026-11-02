# Lux in Tenebris — AI dispatches · November 2, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 130 · https://luxintenebris.news/

## Lead Humanoid Robotics: Meta built a humanoid prototype called Max with Fourier Intelligence in three months

The Information reports Meta worked with Shanghai-based Fourier to assemble a roughly 1.5 m, 48 kg humanoid codenamed Max in about three months, running on NVIDIA Jetson Thor compute with five-fingered hands and an expressive face display. Work on a Max 2 is already underway, and Meta says the effort is internal research with no plans to sell the units.

Source: [Humanoids Daily / The Information](https://www.humanoidsdaily.com/news/meta-fourier-max-humanoid-prototype)

## Top stories

### LeCun's Llama-4 postmortem: rushed timelines, lost team, and the case for world models

Yann LeCun published a detailed retrospective on the Llama lineage, saying he championed open-sourcing Llama-2 but attributes Llama-4's weak reception to rushed product pressure and the dispersal of the original FAIR Paris team. In a companion thread he contrasts LLM declarative knowledge with JEPA-style world models that need far less data.

Source: [@ylecun](https://x.com/ylecun/status/2116957849255342094)

### A 109M-parameter JEPA-style trainer rivals 72B LLMs on representation alignment

A new paper by Randall Balestriero and Yann LeCun, promoted by LeCun himself, proves a version of the Platonic Representation Hypothesis: with anti-collapse regularizers, the similarity structure of training data determines learned representations. A 109M text encoder trained this way aligns with DINOv2/CLIP better than every evaluated LM up to 72B, using about 42x fewer examples than next-token prediction.

Source: [arXiv](https://arxiv.org/abs/2610.39302)

## Research & Papers

- **[Training Foundation Models with a Single Algorithm](https://arxiv.org/abs/2610.40564)** — Shows the staged lifecycle (pretraining, midtraining, SFT, RL) is not algorithmically fundamental: RL objectives can be derived as maximum-likelihood fitting to model-generated target distributions, unifying all stages under one likelihood-based trainer while improving the accuracy-compute tradeoff. *(arXiv)*
- **[Apple trains UI navigation agents with online RL on live iOS apps](https://arxiv.org/abs/2610.39264)** — An 8B RL agent trained across hundreds of concurrent virtual iOS devices with a planning-plus-grounding setup improves out-of-distribution Android generalization nearly 7x over the SFT baseline and outperforms Gemini-3.5-Flash on real applications. *(arXiv)*
- **[AB-Attention accelerates video diffusion transformers without retraining](https://arxiv.org/abs/2610.39663)** — A training-free block-sparse attention method skips 89-92% of attention on Wan2.1 and HunyuanVideo while improving PSNR by up to 4.4 dB over the strongest baseline and delivering up to 2.23x end-to-end speedup. *(arXiv)*
- **[EditAgent rethinks agentic image editing](https://arxiv.org/abs/2610.39664)** — A study finds general-purpose agentic editors produce no usable result in over 40% of expert-annotated cases; EditAgent routes steps across general and specialized editors with per-candidate verification, preferred by experts in 78.5% of decided comparisons. *(arXiv)*
- **[Unlocking any-order generation in pretrained autoregressive image models](https://arxiv.org/abs/2610.39293)** — A recipe adapts raster-scan AR image models into any-order generators at 13-33% extra compute, beating MaskGIT on ImageNet inpainting (FID 6.21 vs 10.44) while keeping the standard AR inference stack intact. *(arXiv)*

## Tools & Startups

- **[HackerBooks: HackerTube, but for books mentioned on Hacker News](https://hackerbooks.org)** — A companion site to Karpathy's HackerTube indexes and surfaces books referenced across Hacker News discussions, hitting 651 points within hours of launch. *(HackerBooks)*
- **[OmniDiff: a content-aware Git difftool in Rust](https://github.com/ivankovic/omnidiff)** — An open-source, super-fast Git difftool that understands content structure rather than plain line diffs, trending on Hacker News. *(GitHub)*
- **[Memdoor: five Qwen3.8-27B models beat Fable 5 on LiveCodeBench Hard](https://github.com/guregodevo/memdoor/tree/main/examples/workflows/team-solve)** — An open-source multi-agent workflow shows five cooperating Qwen3.8-27B models outscoring a frontier model on LiveCodeBench Hard; it drew 409 points and 200 comments on Hacker News. *(GitHub)*
- **[Confetti: build hardware gadgets using plain English](https://www.producthunt.com/products/confetti-5)** — A new tool for designing and prototyping hardware gadgets described in natural language, bridging plain English and electronics prototyping. *(Product Hunt)*
