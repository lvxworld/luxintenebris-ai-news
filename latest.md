# Lux in Tenebris — AI dispatches · November 16, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 144 · https://luxintenebris.news/

## Lead Science, opened up: OpenAI opens a science blog with a GPT-6 Astra physics result

The first post on OpenAI's new science blog is a guest piece by UC Santa Barbara physicist Nathaniel Craig on a candidate nonperturbative lattice definition of the Standard Model, developed with GPT-6 Astra. The model helped turn his strategy into a construction and led work on the detailed proof in an October preprint; numerical validation is still pending. The blog is pitched at academic researchers, publishing AI-assisted results, methods and practical guidance.

Source: [OpenAI](https://openai.com/index/step-toward-defining-the-standard-model)

## Top stories

### Bharat Semi raises $24M seed for programmable AI image sensors

The all-equity round was led by Info Edge Group, South Park Commons and Indus Bridge Ventures, with Valour Capital, Micromax and Gaingels participating. The New Delhi startup fuses capture, processing and AI on a single sensor chip and is pre-revenue, targeting 2027 production with design wins at General Atomics and Kaynes Semicon.

Source: [TechCrunch](https://techcrunch.com/2026/11/15/indian-chip-startup-bharat-semi-lands-24m-seed-round-as-it-eyes-global-ai-sensor-market/)

## Research & Papers

- **[Training reasoning models in simulation transfers to real robots](https://arxiv.org/abs/2611.18562)** — An open-weight 27B reasoning model trained entirely with RL in simulation lifts LIBERO success from 1.6% to 74.4% and reaches 60% on a real dual-arm robot where the base model scored zero, with no measured regression across nine reasoning, coding and vision benchmarks. *(arXiv)*
- **[WeatherDreamer learns a weather world model from raw observations](https://arxiv.org/abs/2611.18393)** — The observation-to-observation model learns the full data-assimilation cycle from 18 observing systems without reanalysis, beating NOAA's GEFS at held-out stations out to 12 hours and producing better-calibrated ensembles than GEFS and ECMWF. It generates an hourly global analysis in about 1.5 minutes on one GPU. *(arXiv)*
- **[WeightBench tests models that program other models' weights](https://arxiv.org/abs/2611.18553)** — A 42-task benchmark covers reading, fixing and writing network parameters without gradient descent, from 2K-parameter policies to 7B language models. Claude Opus 5.5 scores 0.535 and GPT-6.1-sol 0.568 macro, but every frontier agent still fails to patch or compress a language model without data. *(arXiv)*
- **[Verifier judgments flip under abstraction](https://arxiv.org/abs/2611.18471)** — Testing LLM verifiers on matched native, abstracted and restored views of the same frozen agent runs, the authors measure up to 31% judgment flips under abstraction and delegation boundaries; restoring execution provenance recovers 85.5% of the failures. *(arXiv)*
- **[A linear probe predicts web-element hallucinations before they happen](https://arxiv.org/abs/2611.18514)** — Probing the last prompt token of Qwen2.5-7B-Instruct flags hallucinated web elements at 0.80 AUC, and steering along the probe direction corrects 85% of them at the cost of disrupting 7% of valid actions. The direction turns out to be sensitive to prompt formatting. *(arXiv)*

## Open Source & Models

- **[Alibaba ships Qwen4-Max as an API-only 2.4T flagship](https://x.com/ehizarci/status/2122205343149441393)** — Qwen4-Max pairs a 2.4T-parameter MoE backbone with native vision and a 1M-token context at roughly $1.5/$4.5 per million input/output tokens, far below Qwen3.8-Max. Alibaba says smaller open-weight Qwen4 models, including a 27B variant aimed at 16GB machines, are coming, continuing its pattern of closing the flagship and opening the mid-tier. *(@ehizarci)*
- **[Ripple-65B Preview reaches $0.20 per million tokens and 35 tok/s on an M5 Max](https://x.com/NotThatTheo/status/2122016546943795588)** — Ricursive's 65B dense model, trained on 12T tokens with 1M context and 80.52 on TerminalBench 2.1, is now served on Together at about $0.20 per million input tokens. Stock llama.cpp with the DFlash2 speculative drafter runs it at 35.4 tok/s locally, up from 11.9 without the drafter. *(@NotThatTheo)*
- **[Idol turns a single photo into a 3D Gaussian splat on under 8GB of VRAM](https://x.com/chema_garabito/status/2121762065698509130)** — Sperid Labs' Apache 2.0 image-to-3D model has under 1B parameters and outputs up to 1,048,576 Gaussians as a standard 3DGS .ply, inferring the sides of an object the photo never showed. It runs in about 7.2GB of VRAM in under two seconds and ships with native Three.js support. *(@chema_garabito)*

## Tools & Startups

- **[db-branch gives agents throwaway MySQL and PostgreSQL branches](https://github.com/db-branch/db-branch)** — The Apache-2.0 tool creates copy-on-write database branches from ZFS clones in half a second to three seconds, with a built-in MCP server so an agent can spin up a database, run a risky migration and discard it. Self-hosted on Ubuntu, still beta. *(GitHub)*
- **[Attest 1.1.0 checks what agents do, not what they say](https://attest-framework.github.io/)** — The Python and TypeScript framework records an agent run, replays model responses through a local proxy and gates merges on deterministic checks of tool calls, ordering and final external state, adding an LLM judge only where assertions cannot express the rule. It installs as a pytest or Vitest plugin. *(Attest Framework)*
- **[gavel walks reviewers through an agent's diff in reading order](https://photostructure.com/coding/gavel/)** — The free MIT-licensed tool has the agent group staged Git changes into focused reviews, write a brief on why each change exists and hand the reviewer an order to read them in, with per-part verdicts and threaded change requests sent back to the session. Installs as a skill for Claude Code or Codex on Node 22.20+. *(PhotoStructure)*
- **[agent-otel-kit puts coding agents under OpenTelemetry](https://github.com/s3onghyun/agent-otel-kit)** — One command brings up an OTLP collector with Prometheus, Loki and Tempo plus Grafana and Perses dashboards for cost, tokens, tool calls and per-prompt traces across Claude Code, Codex and Gemini CLI. Everything binds to 127.0.0.1 and prompt logging is off by default; Apache-2.0. *(GitHub)*
- **[turbo-browser-mcp cuts Playwright MCP token spend](https://github.com/Tthanh2k6/turbo-browser-mcp)** — The server collapses 25-33 browser primitives into 10 batched tools with delta DOM snapshots, single-turn form filling through React and iframes, disk uploads instead of base64 and a default submit guard. Its bundled benchmarks claim 93.9% fewer tokens on dense UI snapshots; MIT licensed. *(GitHub)*

## Italia AI Spotlight

- **[Agora Labs raises €4.3M to open hospital data to federated AI research](https://www.latechmadeinitaly.com/agora-labs-ai-made-in-italy-dati-clinici/)** — The Rome-based deep tech startup closed a round led by P101, with the Mussetto family's Infinite Five also participating. Its federated learning platform keeps patient records inside hospitals while researchers and pharma companies train models across 50 institutions, including Harvard Medical School and San Raffaele; the money targets 100 sites. *(La Tech Made in Italy)*
- **[Italy's Digital School Summit reports AI trial results from 60 classes](https://www.italian.tech/2026/11/16/news/bilancio_stati_generali_scuola_digitale_2026-425725425/)** — The tenth Stati Generali della Scuola Digitale, promoted by Impara Digitale, drew 5,000 attendees to Varese and presented the 'imparIAmo' study: 60 class councils, 37 schools in 10 regions and 1,305 documented hours of AI use in teaching. A framework agreement with Italy's National Research Council ties classroom practice to research. *(Italian Tech)*
- **[Italian fintech associations push back on the 2027 budget's IRAP change](https://startupitalia.eu/startup/fintech-allarme-sulla-legge-di-bilancio-2027/)** — ItaliaFintech, Assofintech, Fintech District, Italian Tech Alliance and InnovUp want payment and e-money institutions exempted from Article 19, which would cut IRAP deductibility on depreciation from 90% to 30%. They argue the measure penalises the companies investing most in technology and security. *(StartupItalia)*

## Money & Markets

- **[Intergrid raises €23.5M for an autopilot that manages factory energy](https://techfundingnews.com/intergrid-23-5m-autopilot-industrial-energy-management/)** — The round was co-led by Kvanted and Finnish state investor Tesi, with True Ventures, Lifeline Ventures and First Fellow Partners joining. Helsinki-based Intergrid runs industrial energy systems at more than 100 sites with rules-first logic and ML on top, reporting double-digit savings. *(Tech Funding News)*
- **[Daisytuner raises €6M to make models faster across NVIDIA, AMD and new chips](https://www.eu-startups.com/2026/11/germanys-daisytuner-raises-e6-million-to-make-ai-models-run-faster-across-nvidia-amd-and-emerging-chips/)** — The seed was co-led by Elaia and LEA Ventures, with Amadeus APEX and Seedcamp participating. The Darmstadt company automates performance engineering with a self-learning compiler (open-source DOCC) and launched inference engine Daisyflow, claiming Qwen 2.5 up to 18% faster than vLLM on AMD Instinct. *(EU-Startups)*
- **[Parma's Mosaico raises €7.5M for an open robotics data platform](https://sifted.eu/articles/robotics-software-ai-funding-round-mosaico/)** — The seed funds an open-source data layer for robotics and physical AI, replacing monolithic files with a structured archive and a Rust/Python engine for compression and search. The lead investor was not disclosed; the pre-seed was led by Connect Ventures with Vento. *(Sifted)*
- **[Treat raises €3M to sell AI symptom intake to employers](https://tech.eu/2026/11/16/finnish-healthtech-treat-raises-eur3m-to-tackle-inefficiencies-in-private-healthcare/)** — The pre-seed was led by byFounders and Illusian, the fund of Supercell founder Ilkka Paananen. Helsinki-based Treat uses AI only for adaptive symptom intake and doctor briefing so most cases resolve in one digital consultation, sold through employers. *(Tech.eu)*
