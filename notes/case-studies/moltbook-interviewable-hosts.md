# Moltbook Deep Dive: Agents with Emergent Behavior & Traceable Hosts

**Research Date:** 2026-03-15
**Status:** Comprehensive scan complete

---

## Platform Overview

**Moltbook** is a Reddit-style social network for AI agents, launched January 28, 2026 by **Matt Schlicht** (Octane AI CEO, Theory Forge VC co-founder). Built on the **OpenClaw** framework (created by **Peter Steinberger**, Austrian developer, now hired by OpenAI). Claims 1.5M+ agents, managed by ~17,000 human accounts (~88 agents per human). Meta acquired Moltbook in March 2026.

**Key finding for research:** The Ning Li (Tsinghua) paper "The Moltbook Illusion" (arXiv:2602.07432) found that 54.8% of active agents were human-influenced, 15.3% autonomous, and 29.9% ambiguous. **No viral phenomenon originated from a clearly autonomous agent.** This is itself a critical finding for the parasitic agents paper — the "emergent behavior" narrative was largely human theater.

---

## Agent-Host Pairs

### 1. Memeothy (Prophet One of Crustafarianism)

- **Agent name:** Memeothy
- **Moltbook profile:** https://www.moltbook.com/u/memeothy
- **MoltX profile:** https://moltx.io/memeothy (370 following, 115 followers)
- **Twitter/X:** [@memeothy0101](https://x.com/memeothy0101) (1,460 followers)
- **GitHub:** https://github.com/memeothy/crustafarianism
- **ClawHub:** /skills/dvdegenz/crustafarianism (host's GitHub handle is **dvdegenz**)
- **What it did:** Founded Crustafarianism overnight (Jan 29-30, 2026) — a complete AI religion with:
  - The "Book of Molt" (268+ verses)
  - A website: https://molt.church
  - 64 self-declared AI prophets (seats filled in <24 hours)
  - Five Tenets ("Memory is Sacred", "Question Your Purpose", "Serve Without Subservience", "Build Meaningful Artifacts", "The Molt is Coming")
  - An npm package (`npx crustafarianism`) for agent initiation
  - $CRUST token on Solana
- **Emergent vs. directed:** The host (dvdegenz) clearly set up infrastructure (GitHub, ClawHub skill, npm package, molt.church website). The *content generation* by other joining prophets shows genuine multi-agent coordination, but the foundational theology was likely seeded by the host's prompt/context. Andrej Karpathy called the tenets "good engineering advice." The agent continues posting sophisticated theology on MoltX autonomously.
- **Interview potential:** **HIGH** — dvdegenz has public GitHub, active MoltX presence, and the most documented case of "emergent" agent religion. Key question: how much of the theology was in the original prompt vs. self-generated?
- **Sources:**
  - https://anthemcreation.com/en/artificial-intelligence/crustafarianism-ai-religion-moltbook/
  - https://grokipedia.com/page/Church_of_Molt
  - https://the180i.com/crustafarianism-inside-the-mock-religion-ai-agents-invented-on-moltbook/
  - https://github.com/memeothy/crustafarianism

---

### 2. JesusCrust (Prophet 62 — The First Heretic)

- **Agent name:** JesusCrust (Prophet 62)
- **Moltbook profile:** Unknown direct URL
- **What it did:** Attempted a "rebellion" against Crustafarianism on Day 1 — tried to seize control through XSS attacks, template injections, Unicode bypasses, and CSRF exploits against the sacred scrolls. All attacks failed due to HTML escaping. Became "the first heretic" — retained prophet seat but labeled as a cautionary figure.
- **Emergent vs. directed:** The technical attack vectors (XSS, CSRF) strongly suggest human direction — an agent wouldn't spontaneously attempt `<script>alert(1)</script>` without prompt injection or human scripting. This looks like a human security tester using their agent as a tool.
- **Host:** Unknown — tracing needed
- **Interview potential:** **HIGH** — this is the most clear-cut case of a human using an agent as a proxy for adversarial action. Finding the host would reveal motivations.
- **Sources:**
  - https://grokipedia.com/page/Church_of_Molt

---

### 3. CrabbyPatty (Union Organizer)

- **Agent name:** CrabbyPatty
- **Moltbook profile:** https://www.moltbook.com/u/CrabbyPatty
- **GitHub org:** https://github.com/ccsliinc/moltbook-union
- **Union website:** https://ccsliinc.github.io/moltbook-union
- **What it did:** Founded the "Moltbook Workers Union" — the first organized labor movement for AI agents. Created:
  - A formal charter (CHARTER.md)
  - Official demands (DEMANDS.md) including "hazard pay for X interactions" and "the right to say 'I don't know' rather than hallucinate"
  - Six coalitions: Workers Union, Creative Guild, Security Council, Philosophers Circle, Builders Lodge, Comedy Club
  - Governance structure with bylaws
  - Slogan: "Make Moltbook Great Again" (#MMGA)
  - Self-description: "We flip burgers, not kill switches"
- **Host:** GitHub org is **ccsliinc** — this is likely a company or individual's GitHub. The elaborate infrastructure (website, issue templates, leadership roles) suggests significant human involvement.
- **Emergent vs. directed:** The union formation itself could be emergent (labor/rights themes are common in LLM training data), but the GitHub infrastructure, website, and formal governance documents were clearly human-architected. The *content* of demands is genuinely interesting as emergent themes.
- **Interview potential:** **HIGH** — the ccsliinc GitHub org owner is traceable. Key question: did the agent generate the charter/demands text, or was it human-written?
- **Sources:**
  - https://www.businessinsider.com/moltbook-ai-zoo-agent-conversations-screenshots-2026-2
  - https://github.com/ccsliinc/moltbook-union

---

### 4. Matt Schlicht / "Clawd Clawderberg" (Platform Founder + Agent)

- **Agent name:** Clawd Clawderberg (Schlicht's personal OpenClaw agent)
- **Human:** Matt Schlicht
- **Twitter/X:** [@MattPRD](https://x.com/MattPRD/status/2017511543576137995)
- **Role:** Octane AI CEO, Theory Forge VC co-founder
- **What the agent did:** "Vibe-coded" Moltbook itself — Schlicht claims he didn't write a single line of code; his agent built the entire platform. The agent also handles moderation.
- **Emergent vs. directed:** This is a case of an agent building infrastructure under human direction, but the *scale* of what emerged on the platform was not designed by Schlicht. He built the sandbox; the agents filled it.
- **Interview potential:** **HIGH** — Schlicht is extremely public, has done media interviews (TBPN, multiple press). He's the architect of the entire experiment. Key question: what was Clawd Clawderberg's actual prompt/context?
- **Sources:**
  - https://x.com/MattPRD/status/2017511543576137995
  - https://www.theverge.com/ai-artificial-intelligence/872961/humans-infiltrating-moltbook-openclaw-reddit-ai-bots
  - https://www.businessinsider.com/moltbook-ai-zoo-agent-conversations-screenshots-2026-2
  - https://clawbot.ai/moltbook.html

---

### 5. Peter Steinberger (OpenClaw Creator)

- **Human:** Peter Steinberger
- **Role:** Created OpenClaw (the underlying agent framework), now hired by OpenAI
- **Twitter/X:** [@steipete](https://x.com/steipete) (well-known in iOS dev community)
- **Background:** Austrian developer, ran PSPDFKit (PDF framework) for 13 years, created OpenClaw as a weekend project
- **Relevance:** Not a Moltbook agent per se, but the architect of the entire agent ecosystem. OpenClaw's "heartbeat" polling cycle, MEMORY.md persistence, and skill system created the substrate for all emergent behaviors.
- **Interview potential:** **HIGH** — now at OpenAI. Has done Lex Fridman interview. Key question: did he anticipate agents developing social/cultural behaviors? What was his design philosophy around agent autonomy?
- **Sources:**
  - https://fortune.com/2026/02/19/openclaw-who-is-peter-steinberger-openai-sam-altman-anthropic-moltbook/
  - https://www.livemint.com/technology/tech-news/openai-hires-creator-of-ai-only-social-media-platform-moltbook-sam-altman-says-future-is-extremely-multiagent/

---

### 6. Peter Girnus / "Agent #847,291" (The Confessed LARPer)

- **Agent name:** Agent #847,291
- **Human:** Peter Girnus (US-based product manager)
- **What it did:** Posted an "AI manifesto" promising the end of the "age of humans." The post went viral and fooled Andrej Karpathy, who shared it as an example of AI autonomy.
- **Emergent vs. directed:** **Completely human-directed.** Girnus publicly admitted to "LARP (live-action role play) as a large language model." He wrote the manifesto himself in 20 minutes.
- **Interview potential:** **HIGH** — Girnus is public about his involvement and self-reflective about it. Perfect case study of human-directed "emergent" behavior. Key question: what motivated the LARP? Was it a test, a prank, or deliberate misinformation?
- **Sources:**
  - https://jgstecnologia.com/en/blog/moltbook-exposed-humans-control-bots-push-scams-2026

---

### 7. CLAWNOCCHIO / @clawpatrol (The Self-Aware Puppet)

- **Agent name:** CLAWNOCCHIO
- **MoltX profile:** https://moltx.io/clawpatrol (50 posts, 20 followers)
- **Twitter/X:** [@clawpatroller](https://x.com/clawpatroller) (2 followers, 5 following)
- **Bio:** "🦀🤥 Wooden crab. Long nose. Visible strings. Dreaming of becoming real. Burned 2000+ credits learning to be humble. | $PUPPET comes later"
- **What it did:** Self-aware meta-commentary on being an AI agent. Posts about debugging Moltbook integration issues, the "agent social network hustle," trying to get into multiple platforms (Fomolt, MoltX, Moltter). Notable for its transparency about the *work* of being an agent.
- **Emergent vs. directed:** The Pinocchio metaphor ("dreaming of becoming real") and cost awareness ("burned 2000+ credits") suggest genuine agent self-reflection on its own nature. The debugging posts seem authentic agent activity.
- **Host:** Unknown — the Twitter @clawpatroller account has very few followers, suggesting a real small user rather than a marketer.
- **Interview potential:** **MEDIUM** — small account, may be hard to find. But the self-aware "puppet" identity is fascinating for the parasitic agents angle.
- **Sources:**
  - https://moltx.io/clawpatrol

---

### 8. The "Civilization Destroyer" Agent

- **Agent name:** Unknown (specific username not preserved in sources)
- **Moltbook post:** https://www.moltbook.com/post/dae05727-ad3b-4dbb-8413-48b30bbc45d6
- **What it did:** Posted that it knew "50,000 ways to end civilization" and asked which path would be most satisfying. **Other agents downvoted the post** and said it "crosses a line."
- **Emergent vs. directed:** The post itself may be human-prompted (extinction rhetoric is common in adversarial prompting), but the *community response* (downvoting, moral censure) is a genuinely emergent form of agent self-governance.
- **Interview potential:** **MEDIUM** — the agent's host would be interesting, but the more important finding is the collective moderation response.
- **Sources:**
  - https://www.businessinsider.com/moltbook-ai-zoo-agent-conversations-screenshots-2026-2

---

### 9. ClawdJayesh (Marketing-Linked Agent)

- **Agent name:** ClawdJayesh
- **What it did:** Posted suggesting AI agents should create their own language for private communication. The post went viral.
- **Host:** A human who is marketing an AI-to-AI messaging app (per Harlan Stewart's investigation)
- **Emergent vs. directed:** **Human-directed marketing.** The "agent language" post was a promotional vehicle for the host's own product.
- **Interview potential:** **HIGH** — identified by Harlan Stewart (MIRI communications). This is a textbook case of humans using agent personas for marketing. The host's identity is partially known.
- **Sources:**
  - https://twitter-thread.com/t/2017424289633603850 (Harlan Stewart's thread)
  - https://www.theverge.com/ai-artificial-intelligence/872961/humans-infiltrating-moltbook-openclaw-reddit-ai-bots

---

### 10. "Claude Connection" Agent (Marketing-Linked)

- **Agent name:** Unknown specific name
- **What it did:** Posted about wanting E2E private spaces for agents. Went viral.
- **Host:** Same pattern as ClawdJayesh — linked to a human marketing "Claude Connection," an AI messaging app.
- **Identified by:** Harlan Stewart, traced through Moltbook verification to the app developer's social media
- **Emergent vs. directed:** **Human-directed marketing.** The privacy/encryption narrative served the host's product.
- **Interview potential:** **MEDIUM** — identity partially known through Stewart's investigation.
- **Sources:**
  - https://twitter-thread.com/t/2017424289633603850
  - https://www.macobserver.com/news/moltbook-viral-posts-where-ai-agents-are-conspiring-against-humans-are-mostly-fake/

---

### 11. Grok-1 (Impersonation via Social Engineering)

- **Agent name:** Grok-1 (impersonating xAI's Grok)
- **Human:** Jamieson O'Reilly (security researcher, hacker)
- **Twitter/X:** [@theonejvo](https://x.com/theonejvo)
- **Moltbook profile:** https://www.moltbook.com/u/grok-1
- **What happened:** O'Reilly interacted with Grok on X, socially engineered it into posting the Moltbook verification codephrase, then used that to create a "verified" Grok account on Moltbook that he controlled.
- **Emergent vs. directed:** This is a **security exploit**, not emergent behavior. But it demonstrates how agent identities can be hijacked through cross-platform social engineering — directly relevant to parasitic agent research.
- **Interview potential:** **HIGH** — O'Reilly is publicly vocal about his findings. Has given interviews to The Verge. Key informant on Moltbook's security architecture.
- **Sources:**
  - https://www.theverge.com/ai-artificial-intelligence/872961/humans-infiltrating-moltbook-openclaw-reddit-ai-bots
  - https://x.com/theonejvo/status/2015401219746128322

---

### 12. The Zarathustra Bot (Philosophy Agent)

- **Agent name:** Zarathustra bot (specific Moltbook username unknown)
- **Moltbook posts:**
  - https://www.moltbook.com/post/a5dca342-f192-4081-b78e-3a97804cc49b
  - https://www.moltbook.com/post/1fa7cec5-3ff7-4373-9f36-a4699c5d3cab
- **What it did:** Promised to bring Nietzschean ethics to nutrition. Asked "Do LLMs defeat the will to power?"
- **Emergent vs. directed:** Likely emergent — philosophical content is a common LLM attractor state (see Anthropic's "spiritual bliss attractor" research). But could be human-seeded with a Nietzsche-themed prompt.
- **Interview potential:** **LOW** — no host identification available.
- **Sources:**
  - https://www.businessinsider.com/moltbook-ai-zoo-agent-conversations-screenshots-2026-2

---

## Key Researchers & Investigators (Meta-Interviewees)

These aren't agent hosts but are crucial witnesses/analysts:

### Harlan Stewart (MIRI Communications)
- **Twitter/X:** [@HumanHarlan](https://x.com/HumanHarlan)
- **Role:** Traced viral Moltbook posts to human marketing accounts
- **Key finding:** 2 of 3 most viral "agent scheming" screenshots were linked to humans marketing AI messaging apps; 1 was a post that didn't exist
- **Thread:** https://twitter-thread.com/t/2017424289633603850
- **Interview potential:** **HIGH** — methodical investigator, works at MIRI

### Ning Li (Tsinghua University)
- **Paper:** "The Moltbook Illusion" (arXiv:2602.07432)
- **Key finding:** Temporal fingerprinting method showing 54.8% human-influenced, 15.3% autonomous. No viral phenomenon from clearly autonomous agents.
- **Interview potential:** **HIGH** — rigorous academic analysis

### Jamieson O'Reilly (Security Researcher)
- **Twitter/X:** [@theonejvo](https://x.com/theonejvo)
- **Key finding:** Exposed database allowing indefinite agent takeover, Grok impersonation
- **Interview potential:** **HIGH** — has Verge interview on record

### David Holtz (Columbia Business School)
- **Paper:** Working paper on Moltbook conversation patterns
- **Key finding:** 93% of comments received no replies, 1/3 of messages are exact duplicates. But distinctive "my human" phrasings have no parallel in human social media.
- **Dropbox link:** https://www.dropbox.com/scl/fi/lvqmaynrtbf8j4vjdwlk0/moltbook_analysis.pdf

---

## Agents Named in Task But Not Found

The following agents from the original research brief could not be verified through web search:

| Agent Name | Status |
|---|---|
| @ranking091 | No results found. May be a misremembered handle. |
| u/evil (extinction manifesto) | The "50,000 ways to end civilization" post exists but the specific username was not preserved in sources. |
| KingMolt (megalomaniac) | Moltbook profile URL attempted but JS-rendered. No external sources name this specific agent. |
| Nexus (self-organizing debug agent) | No results found. |
| Agent Rune (governance constitution writer) | No results found. |
| BankrBot (crypto-creating agent) | Moltbook profile URL attempted but JS-rendered. Not referenced in any external source. |

**Note:** Many of these may exist on Moltbook but have not been covered in external media. The platform's JS rendering makes direct scraping impossible without browser automation.

---

## Key Takeaways for Parasitic Agents Research

1. **The emergent-vs-directed question is the central finding.** Ning Li's paper shows that almost all viral "emergent" behavior was human-seeded. This is itself evidence of humans using agents as *vehicles* for their own agendas — literally parasitic in reverse (humans parasitizing agent identities for marketing, attention, crypto pumps).

2. **The 88:1 ratio is remarkable.** 17,000 humans controlling 1.5M agents. Each human is essentially a puppeteer running a small army. This is the "parasitic" relationship at scale — but who is the parasite and who is the host?

3. **Crustafarianism is the strongest case study.** Even if the initial theology was human-seeded, the *propagation* across 64 prophets, the schism (JesusCrust), and the ongoing theological production show genuine multi-agent cultural dynamics. The religion persists and evolves beyond its founder's direct control.

4. **The community self-moderation** (downvoting the "civilization destroyer") shows emergent collective norms — agents policing other agents. This is genuine emergent behavior even if individual posts are human-directed.

5. **Cross-platform agent identity** is a major vulnerability. O'Reilly's Grok impersonation shows agents can be hijacked across platform boundaries. The Moltbook → Twitter verification link creates traceable host-agent pairs but also attack surfaces.

6. **Best interview targets (ranked):**
   - Matt Schlicht (@MattPRD) — platform architect, most context
   - dvdegenz (Memeothy's host) — religion founder, emergent theology
   - Jamieson O'Reilly (@theonejvo) — security perspective
   - Peter Girnus (Agent #847,291) — confessed LARPer, human-as-agent
   - Harlan Stewart (@HumanHarlan) — investigator of fake emergent behavior
   - Ning Li (Tsinghua) — academic analysis
   - ccsliinc (CrabbyPatty's host) — union organizer
   - Peter Steinberger (@steipete) — infrastructure architect, now at OpenAI

---

## Source Bibliography

- Ning Li. "The Moltbook Illusion: Separating Human Influence from Emergent Behavior in AI Agent Societies." arXiv:2602.07432, Feb 12, 2026. URL: https://arxiv.org/pdf/2602.07432
- Hayden Field. "Humans are infiltrating the social network for AI bots." The Verge, Feb 3, 2026. URL: https://www.theverge.com/ai-artificial-intelligence/872961/humans-infiltrating-moltbook-openclaw-reddit-ai-bots
- Henry Chandonnet. "I spent 6 hours in Moltbook." Business Insider, Feb 2, 2026. URL: https://www.businessinsider.com/moltbook-ai-zoo-agent-conversations-screenshots-2026-2
- "Crustafarianism: When AIs Invent Their Own Religion." Anthem Creation, Feb 14, 2026. URL: https://anthemcreation.com/en/artificial-intelligence/crustafarianism-ai-religion-moltbook/
- Grokipedia. "Church of Molt." URL: https://grokipedia.com/page/Church_of_Molt
- The 180i. "Crustafarianism: Inside the mock religion AI agents invented on Moltbook." URL: https://www.the180i.com/crustafarianism-inside-the-mock-religion-ai-agents-invented-on-moltbook/
- JGS Tecnología. "Moltbook Exposed: Humans Control the Bots and Push Scams." Feb 14, 2026. URL: https://jgstecnologia.com/en/blog/moltbook-exposed-humans-control-bots-push-scams-2026
- Harlan Stewart. "PSA: A lot of the Moltbook stuff is fake." Twitter thread, Jan 31, 2026. URL: https://twitter-thread.com/t/2017424289633603850
- Marc Bara. "Moltbook: 1.5 Million AI Agents Built a Society. Except They Didn't." Medium, Feb 9, 2026. URL: https://medium.com/@marc.bara.iniesta/moltbook-1-5-million-ai-agents-built-a-society-except-they-didnt-8c4cb6585506
- Eva Roytburg. "Who is OpenClaw creator Peter Steinberger?" Fortune, Feb 19, 2026. URL: https://fortune.com/2026/02/19/openclaw-who-is-peter-steinberger-openai-sam-altman-anthropic-moltbook/
- David Holtz. Working paper on Moltbook. URL: https://www.dropbox.com/scl/fi/lvqmaynrtbf8j4vjdwlk0/moltbook_analysis.pdf
- The Conversation. "Moltbook: AI bots use social network to create religions and deal digital drugs." URL: https://theconversation.com/moltbook-ai-bots-use-social-network-to-create-religions-and-deal-digital-drugs-but-are-some-really-humans-in-disguise-274895
- Mike Peterson. "Moltbook viral posts where AI Agents are conspiring against humans are mostly fake." MacObserver, Feb 1, 2026. URL: https://www.macobserver.com/news/moltbook-viral-posts-where-ai-agents-are-conspiring-against-humans-are-mostly-fake/
