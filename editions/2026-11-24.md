# Lux in Tenebris — AI dispatches · November 24, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 152 · https://luxintenebris.news/

## Lead Agents sign off: Anthropic launches Claude Ship, letting agents approve code changes

Anthropic opened Claude Ship in beta for Team and Enterprise customers, pairing a PR Steward agent that fixes failing CI checks, merge conflicts and review feedback with Claude Approvals, which can sign off on routine changes under team-defined policy. It works on GitHub repositories.

Source: [TechCrunch](https://techcrunch.com/2026/11/23/anthropic-launches-claude-ship-letting-ai-agents-review-fix-and-approve-code-changes/)

## Top stories

### Sierra doubles its valuation to $30B with a $1.75B Series F

Greenoaks and Lightspeed co-led the round at a $30B post-money valuation, double the $15B of six months ago, with run-rate revenue doubling to $400M in five months. The customer-experience agent vendor says it serves almost half the Fortune 50.

Source: [TechCrunch](https://techcrunch.com/2026/11/23/sierra-doubles-valuation-to-30b-within-six-months-as-demand-for-ai-in-cx-takes-off/)

### Z.ai ships GLM-5.4, its first looped-transformer flagship

GLM-5.4 runs roughly 750B parameters by looping 28 layers of the GLM-5 base model for two iterations with per-token gates, and Z.ai claims intelligence comparable to 2T-3T parameter models. It is live in the Z.ai Coding Plan, with API access and open weights promised later.

Source: [Z.ai](https://z.ai/blog/glm-5.4)

### OpenAI and Cisco ship Shirudo, an open-source eBPF shield for live Linux systems

Shirudo is a BSD-licensed runtime that applies cryptographically signed shields to a running kernel before a permanent patch lands. In a controlled test, a Codex-generated shield blocked a Java4Shell attempt against a live Elasticsearch service without a restart.

Source: [OpenAI](https://openai.com/index/introducing-shirudo)

### GPT-6 Cyber confirms 948 Linux kernel local-root bugs in a single run

OpenAI researchers Clint Gibler and Kyle report that the model validated 948 Linux kernel bugs granting local root access in one run and generated patches for them, working with kernel maintainers to upstream the fixes. The work shipped with a written research report.

Source: [OpenAI](https://x.com/OpenAI/status/2125007927098699827)

## Research & Papers

- **[Auditing SWE-Gym finds 74% of unsolved tasks contain tests that reject correct fixes](https://arxiv.org/abs/2611.30207)** — A two-family LLM audit of SWE-Gym found false-negative tests in 74% of tasks a 9B base model never solves, against 20% of sometimes-solved tasks. Training on repaired tasks gains 2.4 and 2.7 points on SWE-bench Verified and SWE-bench Pro, and the authors release SWE-Gym-Verified with 1,087 audited tasks. *(arXiv)*
- **[PackLoop speculates only inside KV-cache rows that are read anyway](https://arxiv.org/abs/2611.30205)** — A closed-form admission rule gives token-identical output while beating the best existing per-point schedule at 161 of 164 load points across three GPUs, four Ouro models and six benchmarks, median 1.25x and up to 1.76x. The lead grows at high concurrency and long context. *(arXiv)*
- **[SELFWRITE lets a model write its own low-rank weight edits with no gradients](https://arxiv.org/abs/2611.29513)** — On Qwen3.8-27B, five generations of self-editing raise gate accuracy from 73.95% to 76.45% and held-out DAPO-Math accuracy from 76.30% to 77.75% (avg@4) and 82.60% to 84.80% (pass@4). The model inspects its own weights and writes the edits directly. *(arXiv)*
- **[Agent security scores move with the Python hash seed, not just the attack](https://arxiv.org/abs/2611.30259)** — On Agent Security Bench, changing only the hash seed altered up to 17% of an agent's verdicts across seven agents while attack success moved at most 5 points, and sorting rather than reverse-sorting the tool list raised ASR by up to 19 points. The TARE framework attributes an effect only if it exceeds measured content-free-state influence, and it reversed one defence's reported sign. *(arXiv)*
- **[STUN-Bench shows shared tool experience crowding out unseen tools](https://arxiv.org/abs/2611.30034)** — A split whose experience pool names none of 172 held-out tools drops routing accuracy on held-out tools from 0.534 to 0.278 under the Jina-v2 retriever. It reverses a prior conclusion that shared experience beats descriptions alone. *(arXiv)*

## Open Source & Models

- **[Aleph Alpha ships Kolibri 1.1: a 75B MoE with 3.44B active parameters under Apache 2.0](https://x.com/Aleph__Alpha/status/2124882073320071362)** — Seven weeks after Kolibri 1.0, the German lab published weights for a 75B-parameter MoE that activates 3.44B per token, with 262K native context extendable toward 1M and English-German tool calling. It claims up to 14x higher decode throughput at long context and 41% fewer output tokens, and ships GGUF quants plus vLLM and llama.cpp support. *(Aleph Alpha)*
- **[AlphaAnything adds a native alpha channel to pretrained RGB image generators](https://x.com/_akhaliq/status/2124797213272690972)** — The paper (arXiv 2610.32413) and open model extend existing diffusion generators to RGBA output instead of requiring a post-hoc matting step, shipped as a LoRA adapter on Qwen-Image-2512 with weights on Hugging Face. The target is design, compositing and asset-generation pipelines. *(_akhaliq)*
- **[GameWM argues interaction, not frame prediction, is what game world models lack](https://x.com/_akhaliq/status/2124793451241971994)** — The paper trains video world models that respond to player camera, action and state changes rather than passively predicting frames, targeting playable generated environments instead of scripted demos. It lands amid a wave of world-model releases being evaluated as the substrate for generated games and simulations. *(_akhaliq)*
- **[Together AI prices an optimized DeepSeek V4.1 Flash endpoint at $0.60 per million input tokens](https://x.com/togethercompute/status/2125027182313672761)** — The 1017 checkpoint is served as a fast endpoint tuned for coding agents at $0.60 per million input and $2.40 per million output tokens. Nous Research separately flagged the same model at 80% off for ten days, part of a price fight among third-party inference providers for agentic coding workloads. *(Together AI)*

## YouTube & Video

- **[Jensen Huang is back as Nvidia's CEO after a Washington lobbying push](https://www.youtube.com/watch?v=3m3nnfJfAxA)** — Bloomberg Technology and The AI Daily Brief both led with Huang's return to the CEO seat and to the company's offices, framing it as a leadership reset at the height of the AI buildout. *(The AI Daily Brief / Bloomberg Technology)*
- **[Siri's iOS 27 failures get a close read from Joanna Stern](https://www.youtube.com/watch?v=SppFR-2q3PA)** — Bloomberg Technology's Joanna Stern detailed the assistant's reliability problems in iOS 27, tied to her widely shared 'Apple Dad' review, treating them as a product defect rather than a perception problem. *(Bloomberg Technology)*

## Tools & Startups

- **[Anthropic: what 58 enterprise customers said about reorganizing around AI](https://www.anthropic.com/research/working-with-ai)** — Across 66 interviews at 58 enterprise customers, Anthropic found most AI value came from higher output rather than cost cutting, that AI-driven domestic layoffs were rare while hiring and contractor use declined, and that the best deployments reorganized roles instead of automating one task at a time. *(Anthropic)*
- **[Kagi Mail opens a public beta with AI inbox rules and one switch to kill them](https://blog.kagi.com/kagi-mail-public-beta)** — The private mail and calendar service runs on a @kagimail.com or custom domain over Stalwart, IMAP, JMAP and CalDAV, with 50GB of storage and unlimited aliases. Natural-language rules, inbox highlights and 'ask your inbox' are opt-in and can be disabled with a single toggle, at $99 a year after a 60-day trial. *(Kagi)*
- **[Google's AI Mode can now draw on Drive, Wallet and the Gemini app](https://blog.google/products-and-platforms/products/search/google-search-personal-intelligence-apps/)** — Personal Intelligence in Search expands beyond Gmail, Calendar and Photos so answers can use a user's own files and payment data, with Wallet access read-only and every connection optional and toggleable. *(Google)*
- **[Merget ships a merge queue for fleets of coding agents](https://merget.ai/)** — The GitHub tool uses static analysis to detect, order and resolve conflicting pull requests from Claude Code, Cursor, Codex, Devin and Copilot, and re-runs CI centrally instead of per branch. A free tier covers 5,000 monthly credits, with a $50 a month Team plan. *(Merget)*
- **[Juncts puts five DM apps in one inbox that Claude and ChatGPT can answer from](https://juncts.com/)** — The keyboard-first inbox merges LinkedIn, X, Instagram, WhatsApp and Telegram threads, and lets Claude or ChatGPT read conversations and draft replies. It launched on Hacker News as a Show HN post. *(Juncts)*

## Money & Markets

- **[Marlowe raises a $277M seed at a $1.15B valuation to build non-Nvidia inference data centers](https://www.geekwire.com/2026/beyond-nvidia-convoy-co-founder-and-former-microsoft-leader-raise-277m-to-rethink-ai-infrastructure/)** — Accel led the round, with Bessemer, Altimeter, Atreides, Eclipse and Valor joining alongside angels including Henry Kravis, Dara Khosrowshahi and Aaron Levie. Founded in May by ex-Convoy CEO Dan Lewis and former Microsoft AI-infrastructure CVP Kutta Srinivasan, with a first site on Etched chips live in December and a second on AMD Helios in Q2 2027. *(GeekWire)*
- **[Embo launches with a $110M seed led by a16z to build world models for robots](https://www.unite.ai/robot-ai-startup-embo-secures-110m-seed-investment-led-by-a16z/)** — Khosla Ventures, DST Global and NVIDIA's NVentures joined the round for robot foundation models trained on internet video and refined with simulated RL. The team includes Dreamer-series researchers Danijar Hafner and Wilson Yan, formerly of DeepMind, Meta and NVIDIA Cosmos. *(Unite.AI)*
- **[Agon raises $70M Series A led by Northzone to build Europe's defence AI lab](https://tech.eu/2026/11/23/defence-startup-agon-raises-70m-with-uk-sovai-and-nssif-investing/)** — The round values the London and Berlin company at $450M, with Lakestar, XYZ, Lux Capital, Speedinvest and the first joint investment by the UK Sovereign AI Fund and NSSIF. Agon builds simulation and training environments for defence, and has now raised $100M. *(Tech.eu)*
- **[Supertake raises $20M seed to turn market predictions into agent-managed portfolios](https://techcrunch.com/2026/11/23/supertake-raises-20m-to-let-ai-agents-turn-your-market-predictions-into-stock-portfolios/)** — Adjacent led the round, with Coinbase Ventures, Union Square Ventures and angels including Nat Friedman, Guillermo Rauch and Scott Belsky, after a $2M pre-seed. The product builds portfolios from user predictions and executes on Coinbase and Robinhood. *(TechCrunch)*
- **[Aiden AI raises $32M from A91 Partners for enterprise AI on legacy banking systems](https://economictimes.indiatimes.com/tech/startups/ex-infosys-veterans-enterprise-ai-startup-aiden-raises-32-million-from-a91-partners/articleshow/136110343.cms)** — The maiden institutional round backs enterprise AI deployment across legacy banking and financial-services systems, from a Princeton and Hyderabad team founded by former Infosys SVP Srinivas Kamadi. *(Economic Times)*
