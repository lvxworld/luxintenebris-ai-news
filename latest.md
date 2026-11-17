# Lux in Tenebris — AI dispatches · November 17, 2026

> A daily dark-broadsheet recap of the most disruptive AI news from the last 24 hours.
> Issue No. 145 · https://luxintenebris.news/

## Lead AGENTS ON THE WARD: OpenAI's computer-use agent cleared 325 healthcare tasks with 99% rated clinically safe

GPT-6 Astra clicked and typed through EHR and insurer portals in multi-step clinical and administrative workflows, handling prior authorization, referrals and discharge planning. Reviewers rated 99% of 325 tasks clinically safe, and physicians called the work very or extremely helpful in 93% of 646 assessments.

Source: [OpenAI](https://openai.com/index/advancing-computer-use-for-healthcare-teams/)

## Top stories

### Anthropic's filing shows $16.3B in first-half revenue and a $974M quarterly operating profit

Revenue for the first half of 2026 came in at $16.3B against $1.2B a year earlier, with compute costs falling from 251% to 48% of revenue. Anthropic also reported a $974M operating profit in the second quarter and said Claude contributed to more than 90% of its codebase in September.

Source: [@DeepLearningAI](https://x.com/DeepLearningAI/status/2122363904881819677)

### DeepMind opens Antigravity to 10,000 scientists with six months of Gemini 4 Carbon

The Antigravity research program will give up to 10,000 scientists free access for roughly six months. Cited results include AlphaProof code agents formally proving the security of Signal's cryptographic code and a 40x increase in protein sequences found in large databases.

Source: [@GoogleDeepMind](https://x.com/GoogleDeepMind/status/2122366994708124098)

### Apple tests daily usage caps on complex Siri and Apple Intelligence features

The iOS, iPadOS and macOS 27.3 betas put per-device daily limits on cloud-backed Apple Intelligence features: multi-step personal-context Siri requests, image generation and editing, Shortcuts automations on Foundation Cloud models and third-party apps using them. Basic Siri commands stay free, and an iCloud Plus subscription lifts the caps.

Source: [The Verge](https://www.theverge.com/tech/1034581/apple-intelligence-siri-ai-daily-usage-limits-icloud-subscription)

### OpenAI expands frontier model access to 200,000 academic researchers

The ChatGPT for Academic Researchers program adds 50,000 grants on a first-come basis from November 23, each covering a recipient plus two collaborators. Data shared through the program is not used for training by default.

Source: [OpenAI](https://openai.com/index/expanding-chatgpt-for-academic-researchers/)

## Research & Papers

- **[CLAM compiles a session stream into a memory adapter in one forward pass](https://arxiv.org/abs/2611.20759)** — A recurrent hypernetwork turns activations into a low-rank adapter with no gradient steps and no generation calls, paired with an episodic buffer for verbatim detail. On LoCoMo and LongMemEval-S across three 2-7B models it leads agentic baselines by 1-45 points at 3-151x lower memory-build wall-clock time. *(arXiv)*
- **[SilentGuard moves silent-API-failure detection into the tool-calling harness](https://arxiv.org/abs/2611.20595)** — The authors find silent failures in 11 of 15 public research APIs, with counts inflated up to 691x. Checking every result against invariants cuts wrong answers from 74.0% to 1.7% across seven open models and from 70.2% to 0.5% on three frontier models, where a warning-only fix still leaves 70.1% wrong. *(arXiv)*
- **[Twenty frontier models shift their accept/reject verdicts on the same papers](https://arxiv.org/abs/2611.20608)** — Pre-registered tests on ICLR 2027 submissions find the share of papers on the accept side falls 52 and 53 points between two Claude Opus versions and two Gemini versions, and by 43-79 points in six further paired comparisons, with no paper moving up. All twenty models gave a 2 or 3 in 473 of 475 reviews. *(arXiv)*
- **[GPRM scores an agent's step against its past and its future](https://arxiv.org/abs/2611.20755)** — The process reward model judges the problem, prior steps and their evaluations, the current step and future steps jointly, trained with SFT plus GRPO on a four-dimension rubric. With less data and smaller models it beats strong baselines by 7.8 and 5.4 points on PRMBench and ProcessBench and surpasses GPT-4.1 on Agent Error Bench. *(arXiv)*
- **[GaugeRoPE takes 5.85x of the KV cache without retraining the model](https://arxiv.org/abs/2611.20524)** — The paper characterizes when a latent KV representation can serve directly as execution state for pretrained RoPE, then builds the training-free construction it implies. On Mistral-7B it compresses the cache 5.85x at quality close to the full cache and reaches up to 2.48x decode throughput by skipping per-token K/V reconstruction. *(arXiv)*

## Open Source & Models

- **[Hugging Face puts OpenRouter inside the Hub](https://x.com/huggingface/status/2122393775314264519)** — The integration means one token and one endpoint serve open models straight from the Hub, with live model stats and a jointly redesigned inference widget. Hugging Face frames it as cutting the friction between open weights and production use. *(@huggingface)*
- **[MMFlash speeds speculative decoding for vision-language models](https://x.com/_akhaliq/status/2122245046263308321)** — A new paper introduces a speculative decoding scheme built for vision-language models, targeting the multimodal prefill and draft overhead that text-only speculators handle badly. *(@_akhaliq)*
- **[eDMD brings endpoint distribution matching to few-step diffusion distillation](https://x.com/_akhaliq/status/2122362729759662110)** — Endpoint Distribution Matching compresses diffusion and flow models into few-step generators by matching the distribution at the sampler endpoint rather than along the whole trajectory. *(@_akhaliq)*
- **[Liquid AI ships d1.2 decision models and claims the calibration lead](https://x.com/JaceYao10/status/2122562777814614305)** — The d1.2 and d1.2-ultra models target decision and calibration work; d1.2-ultra is reported to top the Artificial Analysis Decision Index with notably lower calibration error than GPT-6 Luna on some benchmarks, at low input-weighted pricing. *(@JaceYao10)*

## YouTube & Video

- **[Nvidia fallout deepens US-China AI tensions](https://www.youtube.com/watch?v=NWwia17We98)** — Bloomberg Technology on how the fallout around Nvidia is adding friction to the US-China AI competition, with export controls and chip supply at the center. *(YouTube — Bloomberg Technology)*
- **[Why Microsoft needed 36 hours to restore its own cloud](https://www.youtube.com/watch?v=ytmawkPTP24)** — Fireship breaks down a major outage across Microsoft's own server infrastructure and what the recovery time says about tooling at hyperscale. *(YouTube — Fireship)*
- **[China is writing its own AI playbook, Bloomberg argues](https://www.youtube.com/watch?v=4Ouzi1OTc8w)** — Everybody's Business argues China's AI strategy has become a self-contained stack of domestic chips, models and deployment rather than a copy of the US approach. *(YouTube — Bloomberg Technology)*

## Tools & Startups

- **[Audible rolls out an AI-generated audio discovery feature](https://techcrunch.com/2026/11/16/audible-turns-to-ai-to-help-users-discover-audiobooks/)** — Audio discovery plays an AI-generated overview of a book's themes plus a summary of reader reactions and commentary from editors or authors. It follows last month's batch of AI story tools and lands as Spotify expands audiobook hours. *(TechCrunch)*
- **[Google Maps' Ask Maps now builds full trip itineraries](https://techcrunch.com/2026/11/16/google-maps-can-now-build-trip-itineraries-with-real-time-details-about-each-stop/)** — Ask Maps produces day-by-day plans with numbered map pins, insider tips and live traffic, hours and crowding data per stop. Itineraries share or export to Google Docs, and Maps can also find appointments. *(TechCrunch)*
- **[Hotline Computer gives coding agents a rootless Linux desktop over MCP](https://computer.hotline.dev/)** — An Xvfb plus Chromium machine in a rootless Docker or Podman container, driven by any MCP client through eight tools, with a browser viewer where a human can take the mouse. It needs no GPU and binds only to localhost. *(Hotline)*
- **[Sutra-OS stores knowledge as scarce, typed units instead of text](https://github.com/0nelight/sutra-os)** — A self-hosted, Clojure-built platform that structures knowledge as typed, related and actionable units, and drew the most discussion of the day's Show HN AI tools. *(GitHub)*
- **[Blobby is a design canvas that Claude, Cursor or Codex drive over MCP](https://useblobby.com/)** — A desktop design tool with no AI of its own that exposes an MCP server, so the agent you already pay for builds pages in a real canvas with layers, components and comments. Designs export as HTML/CSS, React, Shopify or WordPress, and files stay local. *(Blobby)*

## Italia AI Spotlight

- **[Italy approves Cloud Italia 2027-2029 to prepare public administration for AI](https://www.ai4business.it/intelligenza-artificiale/cloud-italia-2027-2029-il-piano-che-prepara-la-pa-allai/)** — The interministerial committee approved a strategy requiring public bodies to extend the national strategic hub with territorial infrastructure, cut extra-EU dependencies and plan compute for AI services. It sets the procurement and sovereignty framework Italian AI suppliers will work within. *(AI4Business)*
- **[Italy is fourth in industrial robotics but 16th in the humanoid supply chain](https://www.latechmadeinitaly.com/e-se-il-made-in-italy-costruisse-i-robot-ma-non-il-loro-cervello/)** — An analysis of the Ingenium 2026 report notes Italy exports €30bn of automation machinery and holds 5.4% of the industrial robotics market, but only 1.1% once chips, control systems, vision and software are counted. The piece argues physical AI is where the gap must close. *(La Tech Made in Italy)*

## Money & Markets

- **[Noeri launches with $110M to build AI that learns from each organization's own work](https://www.securities.io/noeri-raises-110-million-with-menlo-ventures-and-nvidia-backing/)** — Co-led by Yejin Choi and Carlos Guestrin, Noeri builds systems that learn continually from an organization's proprietary data. Menlo Ventures led, with Madrona, Nvidia, Kindred, Cisco, Wing VC, Snowflake and NEA participating. *(Securities.io)*
- **[Corma reaches a $1B valuation about three months after launching](https://techcrunch.com/2026/11/16/cybersecurity-ai-startup-corma-reaches-1b-valuation-in-about-3-months/)** — The cyber-defense startup raised a $125M Series A led by NEA for AI models and agents built for security operations. Total raised is now $185M, including Sequoia, Khosla Ventures and Coatue. *(TechCrunch)*
- **[OpenAI weighed paying more than $5B for interpretability startup Goodfire](https://techstartups.com/2026/11/16/openai-considered-5-billion-plus-acquisition-of-anthropic-backed-startup-goodfire-amid-ai-security-concerns/)** — Executives including Sam Altman held multiple talks with Goodfire about an acquisition or partnership, with one senior executive floating a price above $5B, over 4x its February valuation. No deal resulted; Goodfire preferred staying independent to serve multiple labs. *(Tech Startups)*
- **[Freshworks alums raise $53M for Dreamteam, an AI-native CRM](https://techcrunch.com/2026/11/16/freshworks-alums-raise-53m-to-take-on-salesforce-hubspot-with-ai-native-crm/)** — Together Fund led the seed and Accel the Series A, with Premji Invest participating. Dreamteam's Company Brain plus four built-in agents automate record-keeping, follow-ups and pipeline monitoring, and the company claims 100+ customers in 13 countries. *(TechCrunch)*
- **[Alecto lands €18M seed to scale its AI-native law firm](https://www.eu-startups.com/2026/11/alecto-lands-e18-million-to-scale-its-ai-powered-law-firm-beyond-property-transactions/)** — Insight Partners led the round, with Firstminute, Blue Lion Global, Andrena, FJ Labs and Mishcon de Reya among the participants. The UK consumer law firm plans its first international launch in 2027. *(EU-Startups)*
