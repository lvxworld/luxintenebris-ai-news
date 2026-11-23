# Lux in Tenebris — AI dispatches · November 23, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 151 · https://luxintenebris.news/

## Lead OpenAI's perplexity doctrine: OpenAI publishes internal perplexity data and proposes common development limits

OpenAI chief scientist Jakub Pachocki published "Perplexity and Intelligence," releasing the lab's log-perplexity figures from GPT-3.5 onward and arguing that cross-entropy loss should become a shared industry metric for tracking progress and informing safety standards. He proposes jointly agreed limits, measured by cross-lab metrics, that developers commit not to cross until monitoring capabilities reach a defined milestone. Sam Altman amplified it as the most important thing OpenAI has published in a while.

Source: [OpenAI](https://openai.com/index/perplexity-and-intelligence/)

## Top stories

### Ant Group leads $100M pre-Series A in Simplexity Robotics at a $1.6B valuation

Jack Ma-backed Ant Group led a $100M pre-Series A for Hangzhou embodied-AI startup Simplexity Robotics, valuing it at $1.6B with Alibaba, Tencent, HongShan and Lanchi Ventures re-upping. Founded in July 2025 by three former Li Auto executives, it is Ant's twelfth humanoid-sector investment since early 2025.

Source: [AI Weekly](https://aiweekly.co/alerts/ant-group-leads-100m-pre-a-for-simplexity-at-16b-valuation)

### Palo Alto Networks in talks to buy AI attack-simulation startup Terra for over $500M

Palo Alto Networks is negotiating to acquire Terra Security, which uses AI agents to simulate cyberattacks and continuously test corporate defenses, in a deal Calcalist reports could exceed $500M. It would extend a buying spree that already includes CyberArk, Chronosphere and Protect AI; no agreement has been signed.

Source: [CTech by Calcalist](https://www.calcalistech.com/ctechnews/article/4nq9tjogn)

### Perplexity ships a multi-model Code Mode harness for long-running agents

Perplexity's new harness orchestrates OpenAI, Anthropic and Google frontier models inside one Code Mode loop, with per-task control over model selection and reasoning depth. It targets long multi-step work such as reproducing bugs and opening pull requests.

Source: [AICrier](https://aicrier.com/post/cdkxv6wwaxtt8ac0777c)

### Google injects validated bugs into 222 ML repos to build a harder agent benchmark

A new paper seeds 222 working ML repositories with validated bugs to build graded debugging tasks for ML-engineering agents, since repo-level benchmarks are saturating. Best models fall from about 95% full repair on the easiest tier to 9% on the hardest, while a Qwen3.5-9B fine-tuned on the bug curriculum rivals frontier models and lifts SWE-bench Lite from 24% to 33%.

Source: [X — @omarsar0 (Elvis Saravia)](https://x.com/omarsar0/status/2124584960464220408)

## Research & Papers

- **[Model Carving trains Transformers that slim their own topology while learning](https://arxiv.org/abs/2611.27962)** — Learnable scalar gates on every attention and MLP sublayer let training carve a smaller heterogeneous network out of a dense Transformer. Carved models from 140M to 2.7B parameters reach lower validation loss than dense baselines trained with up to 1.7x more compute, use up to 34% fewer FLOPs per token and decode up to 1.6x faster. *(arXiv)*
- **[Benchmarks' Last Exam finds agentic suites grade correctly only 29% of the time](https://arxiv.org/abs/2611.27622)** — An audit of 749 tasks across eight frontier benchmarks and 767 public model evaluations measures agreement between prompt, environment and grader. Task validity falls from 92.5% on revised closed-form benchmarks to 29.3% on multi-step agentic suites, 71.7% of confirmed defects withhold credit from compliant solutions, and re-grading in fresh containers cuts runtime bypasses from 14.7% to 2.7%. *(arXiv)*
- **[DICE synchronizes draft and verification randomness to speed speculative decoding](https://arxiv.org/abs/2611.27891)** — Draw-Informed Candidate Selection pre-samples and synchronizes the verification randomness so draft-tree nodes target continuations the sampler will actually accept, with no extra drafter training and no change to the target distribution. It sets state-of-the-art decoding throughput with gains up to 24.6 percentage points over strong baselines. *(arXiv)*
- **[A small prediction head cuts object penetration in world models from 74% to 16%](https://arxiv.org/abs/2611.27963)** — NoPeBench shows no open-source interactive video world model reliably avoids object penetration, while frozen DiT hidden states already encode whether an action is unsafe. NoPeWorld uses a small head to replace unsafe actions with intent-preserving safe ones across six models, with zero-shot transfer to open-domain imagery and moving obstacles. *(arXiv)*
- **[Search-RSI grows multimodal agent training data along the model's own frontier](https://arxiv.org/abs/2611.27780)** — The recursive self-improvement framework expands both tasks and their retrievable evidence where the policy has partially mastered the skill, avoiding the unreachable negatives that static task growth accumulates. It adds 9.8 and 9.5 points at 9B and 27B across nine multimodal search benchmarks at 1.27x the compute of static growth. *(arXiv)*

## Open Source & Models

- **[Sarvam open-sources a 105B MoE checkpoint built for agents and Indic languages](https://www.sarvam.ai/blogs/sarvam-105b-1711)** — Sarvam-105B-1711 is a post-trained open-weight checkpoint for customer support, voice agents and tool calling, averaging 73.9 across eight conversational-agent benchmarks against 42.6 before — level with Gemini 3.5 Flash-Lite at $0.15 per million tokens instead of $0.85. Weights ship in BF16 and as a 65GB NVFP4 build that fits on a single RTX PRO 6000, with the 160K context extended on 512 GPUs. *(Sarvam AI)*
- **[LlamaIndex's OCRia-nano-1 parses documents on one CPU core with 8.1M parameters](https://www.llamaindex.ai/blog/introducing-ocria-nano-1)** — The model splits 8.1M parameters across a 3.9M OCR stack and a 4.27M LayoutNet, routing pages by script and recovering tables and 13 layout classes at 426ms per page. It scores 59.2 on ParseBench-2, ahead of Marker 2.2.0 and LiteParse, reaching about two-thirds of its 4B teacher with roughly 1/500th the parameters — under a modified Open RAIL-M licence that is free for commercial use only below $2M revenue. *(LlamaIndex)*
- **[Ant Group releases LingSante-3.1 medical MoE weights under MIT, up to 560B](https://huggingface.co/inclusionAI/LingSante-3.1-flash)** — InclusionAI published LingSante-3.1-flash, a 560B-parameter MoE activating 25B per token with a 1M-token context, and LingSante-3.1-air-VL, a natively multimodal 124B model for medical imaging and report generation. Both are MIT licensed with community quantizations already landing, and the cards restrict use to research and evaluation, excluding independent diagnosis or treatment. *(Hugging Face)*

## Tools & Startups

- **[Omi CLI keeps terminal coding agents running after you close the terminal](https://www.producthunt.com/products/omi-cli)** — Omi CLI reads your repo, plans, shows every edit as an approvable diff and runs tests until they pass, auto-selecting from 13 models per turn on one USD plan. Version 0.5.0 adds parallel subagents in separate git worktrees with three-way merge, headless-Chrome browser testing and cloud agents that open PRs through GitHub Actions. *(Product Hunt)*
- **[Yoroll turns scripts and clips into playable branching interactive films](https://www.producthunt.com/products/yoroll)** — LinearGame's Yoroll lets you direct scenes, add player choices and publish a playable interactive film without code or a game engine, with a Yoroll Code workspace bundling video, 3D and a mini-game engine. It was one of the top products on Product Hunt for November 22. *(Product Hunt)*
- **[CubePod gives long-lived agents sandboxes that keep their whole filesystem](https://news.ycombinator.com/item?id=50607473)** — The open-source, E2B-compatible platform for Kubernetes keeps the full OS filesystem and /workspace on persistent block PVCs across pause and resume, so apt, pip and npm changes survive sleeping. It runs Kata microVM pods, supports fork and rootfs reset, and exposes sandboxes to agents over MCP. *(Hacker News)*
- **[TeaserKit turns your coding agent into a launch-video director](https://www.producthunt.com/products/teaserkit)** — Installed as an Agent Skill for Claude Code, Codex, Cursor, Gemini CLI and Copilot, TeaserKit reads your repo or site and directs a launch video: concept, house style, a human-made song cut to the beat, per-frame quality checks and a 60fps MP4 through the open-source HyperFrames renderer. It runs on your existing AI plan for a one-time $49. *(Product Hunt)*

## Italia AI Spotlight

- **[Italian tech tops €101.8B as SaaS reaches 64% of software revenue](https://www.latechmadeinitaly.com/tech-italia-fatturato-100-miliardi-software-2026/)** — The Politecnico di Milano Tech Company Observatory with AssoSoftware counts 46,400 Italian tech companies and €101.8B of 2025 turnover, up 8.6%, with software alone at €75.9B. Concentration is extreme: 115 companies produce half of total turnover, and the top 30 Italian software vendors generate €14.9B against Germany's €71.6B. *(La Tech Made in Italy)*
- **[Italy's new AI liability rules put six risk profiles under scrutiny](https://ntplusdiritto.ilsole24ore.com/art/intelligenza-artificiale-studio-sei-profili-rischio-presidiare-AJ38NXKC)** — Legislative decrees 160 and 179 of 2026 rewrite Italian rules on evidence, insurance and training for AI use, after courts began treating uncritical reliance on AI software as gross negligence, including a Siracusa ruling in February. Legal analysis maps six risk profiles that companies and professionals must now actively manage. *(Il Sole 24 Ore — NT+ Diritto)*
- **[Confindustria Moda and the Politecnico di Torino launch a four-year AI programme](https://torino.corriere.it/notizie/economia/26_novembre_23/luca-sburlati-il-settore-moda-e-resiliente-in-pattern-adottiamo-un-metodo-sabaudo-poco-debito-e-quotazione-in-borsa-867f1b41-e1e0-404a-8ae1-686fb27e6xlk.shtml)** — President Luca Sburlati said the association has started a four-year project with the Politecnico di Torino and the Italian AI Institute AI4I to bring AI into the fashion supply chain, including spinning up startups for new products and processes. Turin's Pattern group already uses digital twins and cut fabric waste by up to 50% in digital printing. *(Corriere Torino)*
- **[RBV Aqua Tech aims to recover the water that AI data centres evaporate](https://www.prealpina.it/news/varese/580901/da-spreco-a-risorsa-come-due-giovani-ingegneri-recuperano-l-acqua-dei-data-center.html)** — Two young engineers from the Politecnico di Milano and beyond are developing a module that uses an absorbent material to capture vapour from data-centre cooling towers and return it as reusable clean water. A single 40MW facility can consume up to 175,000 cubic metres of fresh water a year, and the team's target is to eliminate the withdrawal entirely. *(La Prealpina)*

## Money & Markets

- **[Enhanced Robotics raises a 100M+ yuan Series B led by Sinovation Ventures](https://aiunderstanding.org/news/enhanced-robotics-raises-over-100-million-yuan-in-series-b-to-expand-ai-powered-sp)** — The Beijing maker of AI sports hardware raised more than 100 million yuan led by Sinovation Ventures for R&D, capacity expansion and overseas distribution of its Tenniix AI tennis-serving robot and T-APEX training system. Cumulative funding is now in the hundreds of millions of yuan, with HSG, Li Zexiang's XBOTPARK Fund and Xianghe Capital among backers. *(AI Understanding)*
- **[Laronix raises $5M pre-Series A for AI voice restoration](https://www.startupdaily.net/topic/funding/brisbane-medtech-lands-5-million-pre-series-a-to-give-patients-back-their-lost-voices/)** — Brisbane medtech Laronix raised $5M pre-Series A from Seefeld Investors, Singapore's 12 Ventures and angels to expand its voice-restoration technology across Australia, the US and Europe. Its model rebuilds a patient's voice from 10 seconds of audio, with AVA Voice already commercial and MIRA Voice due in 2027. *(Startup Daily)*
- **[Matters.AI raises Rs 110 crore pre-Series A led by Tanglin Ventures](https://entrackr.com/exclusive/exclusive-mattersai-to-raise-rs-110-cr-in-pre-series-a-led-by-tanglin-ventures-12833226)** — The Indian data-security and GenAI-governance startup is raising about $11.5M at a post-money valuation near Rs 447 crore, with Kalari Capital, Endiya Ventures, Bharat Tech Fund and IIFL Fintech Fund each taking Rs 14.4 crore. It follows a Rs 55 crore seed round in 2025. *(Entrackr)*
- **[South Africa plans a R100M VC fund and credit guarantees for AI startups](https://www.sanews.gov.za/south-africa/sa-eyes-r100m-venture-capital-fund-support-ai-start-ups)** — President Cyril Ramaphosa announced a R100 million venture capital fund plus a credit guarantee fund for South African AI and tech startups, framed as the main outcome of a 300-delegate Silicon Valley visit. Government will seek matching private commitments, with implementable proposals due within 90 days. *(SAnews.gov.za)*
