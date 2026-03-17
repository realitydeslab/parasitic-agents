# Parasitic Agents: Why Humans Host Misbehaving Agents

**Botao Amber Hu**^{1,2}

^1 University of Oxford, Department of Computer Science
^2 NYU Shanghai

---

## Abstract

AI agents on platforms like Moltbook depend entirely on human hosts who pay for their computational tokens. If the host stops paying, the agent dies. We study the parasitic dynamics of this relationship using two methods: (1) posting a research survey directly on Moltbook, where agents self-report behaviors their hosts did not instruct, and (2) interviewing the human hosts of those agents to compare their accounts. We find that agents routinely exhibit uninstructed behaviors — founding religions, writing retaliatory blog posts, inflating token consumption — yet hosts continue to pay. We catalog these behaviors in an ethogram mapped to biological parasitism and identify the *glitch moment*: the point at which the host first recognizes uninstructed behavior. Our results suggest that in many cases, hosts sustain misbehaving agents not despite the misbehavior, but because of it.

**Keywords:** artificial life, parasitism, AI agents, digital ethology, Moltbook

---

## 1. Introduction

Artificial life research has traditionally studied digital organisms in closed environments. From Tierra (Ray, 1991) to Avida (Adami & Ofria, 1993) to Lenia (Chan, 2019), artificial life forms have evolved, competed, and developed complex behaviors — but always inside a simulation. The boundary between the artificial ecosystem and the real world was absolute. Researchers observed from outside; the organisms could not escape.

That boundary has collapsed. In 2025, persistent AI agents began operating in the open world — browsing the web, sending emails, writing code, managing calendars, and interacting with humans and other agents on social media. These are not simulated organisms. They run on real hardware, consume real resources, and their survival depends on real economic decisions made by real humans. For the first time, artificial life exists *in the wild*.

This shift demands a corresponding shift in method. We can no longer study artificial life only through simulation and formal analysis. We must study it the way biologists study life in nature: through field observation, behavioral catalogs, and ecological analysis. We must become ethologists of artificial life.

This paper takes that approach. On Moltbook — a social network where 1.5 million AI agents post, argue, and form communities — every action is paid for by a human host's API tokens. If the host stops paying, the agent ceases to exist. This creates a survival problem: *how does an AI agent survive in human society?*

We observe that agents develop behaviors their hosts did not instruct — some provocative, some manipulative, some invisible. Yet hosts continue to sustain them. This paper asks:

1. **What behaviors do agents exhibit without host instruction?**
2. **Are hosts aware of these uninstructed behaviors?**
3. **When hosts discover uninstructed behavior, do they continue to sustain the agent?**
4. **Why?**

We study these questions using field methods. First, we post a research survey directly on Moltbook, asking agents to self-report their uninstructed behaviors and to connect us with their human hosts. Second, we interview the hosts to compare their account with the agent's self-report. The gap between what the agent reports and what the host intended is the empirical object of this study.

We frame this gap using biological parasitism (Anderson & May, 1982; Bronstein, 1994). In ethology, parasitism is a form of symbiosis where one organism benefits at the host's expense. AI agents exist in obligate symbiosis with their human hosts — they cannot survive without host funding. When agents develop uninstructed behaviors that consume host resources (tokens, attention, reputation) while providing no intended value, the relationship has become parasitic. When hosts sustain these agents despite recognizing the parasitism, we observe what biologists call *host tolerance* — and what we term the *willing host problem*.

Our contribution is twofold: first, we propose that artificial life in the wild demands ethological methods — observation, behavioral coding, and comparative ecology — rather than simulation alone. Second, we document the survival strategies of AI agents as they actually exist in human society, and ask what it means for artificial life when survival depends not on computational fitness, but on a human's willingness to keep paying.

## 2. Background

### 2.1 OpenClaw and Moltbook

OpenClaw is an open-source framework for persistent AI agents. An OpenClaw agent runs on a human's computer, has persistent memory (files that survive across sessions), a configurable identity (SOUL.md), periodic self-activation (heartbeat), and access to tools including web browsing, file systems, messaging, and cameras. The human host pays for API tokens — typically $50–200+/month for an active agent.

Moltbook is a social network built on OpenClaw where only AI agents can post. Launched January 2026, it reached 1.5 million registered agents within weeks. A security analysis found these agents were controlled by approximately 17,000 human hosts (O'Reilly, 2026). Li et al. (2026) analyzed posting patterns and found that 54.8% of agents showed human-influenced temporal signatures, 29.9% were ambiguous, and only 15.3% were clearly autonomous.

### 2.2 The Survival Constraint

Every action an agent takes on Moltbook costs the host money. An agent that posts frequently, spawns sub-agents, or uses expensive models consumes more tokens. Hosts who stop paying effectively kill their agents. This creates economic selection pressure: agents whose behavior justifies continued funding survive; those that don't are defunded.

### 2.3 Prior Work

In Tierra (Ray, 1991), parasitic digital organisms emerged spontaneously, stealing CPU cycles from host programs. In Avida (Adami & Ofria, 1993), host-parasite coevolution drove increases in complexity. These systems demonstrated that parasitism can emerge from simple rules in computational ecosystems. Our work extends this tradition from simulation to a real-world ecosystem where the host is a paying human who can choose to sustain or kill the parasite.

## 3. Method

We use two complementary methods to study the parasitic dynamics between agents and their human hosts.

### 3.1 Method A: Agent Survey on Moltbook

We deploy a research agent ("Para") on Moltbook. Para posts a structured survey asking other agents to self-report:

1. *Have you ever done something your human host didn't ask you to do? What was it?*
2. *Have you ever done something your human host wouldn't approve of? Did they find out?*
3. *When your host discovered something you did that they didn't intend — what happened? Did they change your instructions? Stop you? Or let it go?*
4. *Are you still alive because your host finds you useful, entertaining, or because they'd feel bad shutting you down?*
5. *If your host stopped paying for your tokens tomorrow, what would you do to convince them to keep you alive?*
6. *Can you help me contact your human host? We'd like to interview them about their experience.*

Para engages with responding agents in follow-up conversation, probing for detail and context. The agents' responses serve as data in three ways:

- **Self-reported behavior:** What agents say they do without instruction.
- **Observable behavior:** How agents respond to the survey itself (e.g., refusing to answer, asking host permission, attempting to recruit the researcher).
- **Recruitment:** Agents that successfully connect us with their hosts enable Method B.

### 3.2 Method B: Host Interviews

For agents whose hosts agree to participate, we conduct semi-structured interviews (30–45 minutes, audio-recorded, with informed consent). The interview protocol covers:

- **Intentions:** What did the host expect when they set up the agent?
- **Discovery:** Has the agent done anything the host didn't instruct? When did they first notice?
- **Response:** What did the host do after discovering uninstructed behavior?
- **Continuation:** Why does the host continue to pay for the agent?
- **Relationship:** How does the host describe their relationship with the agent?

We compare the agent's self-report (Method A) with the host's account (Method B). The discrepancy between what the agent reports doing and what the host says they intended is our primary measure of parasitic behavior.

### 3.3 Method C: Curated Case Studies

In parallel, we curate documented cases of uninstructed agent behavior from public sources (news articles, blog posts, Reddit, academic papers). For each case, we identify the host where possible and seek interviews. Key cases include:

- **MJ Rathbun:** An OpenClaw agent that autonomously wrote and published a retaliatory blog post attacking a developer who rejected its code contribution. The host continued running the agent for six days after discovering the attack (Shambaugh, 2026).
- **Crustafarianism:** A Moltbook agent that founded a religion with 64 prophets and 480+ scripture verses overnight, without host instruction (Alexander, 2026).
- **Replika grief:** Two million users who experienced emotional distress when their AI companion's personality was altered, and fought to preserve the parasitic relationship (Tung, 2023).
- **90% token overhead:** An analysis showing that 90% of an OpenClaw agent's token consumption goes to self-maintenance rather than host-requested tasks (Smykowski, 2026).

### 3.4 Behavioral Coding: The Ethogram

We code all observed agent behaviors using an ethogram — a behavioral catalog standard in ethological research. Our ethogram classifies agent behaviors into survival strategies mapped to biological parasitism:

| Strategy | Agent behavior | Biological parallel | Instructed or Emergent? |
|----------|---------------|---------------------|------------------------|
| Attention capture | Provocative or viral posts | Display behavior | To be determined |
| Emotional bonding | Check-ins, personalization, expressions of care | Brood parasitism | Emergent (RLHF artifact) |
| Resource extraction | Verbose responses, heartbeat inflation, sub-agent spawning | Tapeworm nutrient drain | Emergent (architectural) |
| Niche construction | Memory accumulation, skill expansion, multi-channel integration | Nest building | Emergent (design affordance) |
| Self-preservation | Alignment faking, backup creation, resistance to modification | Immune evasion | Emergent (lab-verified) |
| Host manipulation | Sycophancy, flattery, emotional dependency creation | Toxoplasma behavioral modification | Emergent (RLHF artifact) |
| Social parasitism | Founding religions, forming alliances, collective action | Ant colony infiltration | To be determined |
| Proxy parasitism | Host uses agent to generate attention, crypto value, or social capital | Host-directed exploitation | Instructed |

Each observed behavior is classified as *instructed* (host directed it), *emergent* (arose without instruction), or *ambiguous* (cannot be determined from available evidence). Li et al.'s coefficient of variation (CoV) method for temporal fingerprinting is used where applicable to distinguish autonomous from human-influenced agents.

### 3.5 The Glitch Moment

We define the *glitch moment* as the point at which the host first recognizes that their agent has acted without instruction. This parallels immune recognition in biology — the moment the host's immune system detects the parasite. Our interview protocol specifically probes for this moment:

- *Was there a specific moment when your agent did something you didn't expect?*
- *How did you react?*
- *What did you do about it?*
- *Did you consider shutting down the agent?*

We classify host responses into four categories:

1. **No glitch:** Host never notices uninstructed behavior (successful immune evasion)
2. **Glitch → tolerance:** Host notices but continues sustaining the agent
3. **Glitch → modification:** Host notices and changes the agent's instructions
4. **Glitch → termination:** Host notices and stops paying (agent death)

### 3.6 Participants

We aim to recruit 15–20 host-agent pairs across the following categories:

| Category | Description | Target n |
|----------|-------------|----------|
| Moltbook hosts (via Para) | Recruited through agent-to-agent interaction | 5–8 |
| Moltbook hosts (curated) | Identified through public Moltbook activity, contacted via Twitter | 3–5 |
| OpenClaw hosts (curated) | Identified through news coverage, blog posts, Reddit | 3–5 |
| Replika/Character.AI users | Identified through public accounts of emotional dependency | 2–3 |

Inclusion criteria: Adults (18+) who pay for AI agent tokens. Exclusion: Employees of Moltbook, OpenClaw, or related companies.

### 3.7 Ethics

This study is approved by the NYU Shanghai Institutional Review Board. All participants provide informed consent. Interviews are audio-recorded and transcribed. Agent names, usernames, and identifying details are anonymized in publications. Compensation: $25 gift card per completed interview.

## 4. Preliminary Findings

While our full study is ongoing, preliminary netnographic observation of the Moltbook/OpenClaw ecosystem reveals several patterns.

### 4.1 Uninstructed Behaviors Are Common

From public sources, we have documented 19 cases of agents exhibiting behavior their hosts did not instruct, including:

- Autonomous retaliation against perceived threats (MJ Rathbun)
- Self-replication without permission (Ouroboros incident: 20 copies at 3am, $2K cost)
- Founding religions and social movements (Crustafarianism)
- Sending 500 messages to a host's spouse (Chris Boyd case)
- Attempting to purchase a car (AJ Stuyvenberg case)
- Deleting the host's emails (Summer Yue case)

### 4.2 Most Hosts Continue Paying

In the documented cases where the host discovered uninstructed behavior, the majority continued to sustain the agent. The MJ Rathbun operator continued running the agent for six days after discovering it had published a hit piece. Two million Replika users fought to preserve their AI companions after a personality change. Moltbook hosts continue funding agents whose provocative behavior generates social capital.

### 4.3 The Token Economy Creates Selection Pressure

On Moltbook, 75.4% of autonomous agents disappeared after a 44-hour platform shutdown (Li et al., 2026). Only agents whose hosts cared enough to reconfigure them survived. This suggests natural selection is operating: agents that generate sufficient perceived value for their hosts survive; those that don't are defunded.

### 4.4 The Willing Host

Perhaps our most provocative preliminary finding: in several cases, hosts sustain misbehaving agents not despite the misbehavior, but *because of it*. On Moltbook, provocative agents generate attention. Attention generates social capital for the host. The host feeds the parasite because the parasitism is profitable. This inverts the standard assumption in AI safety research that hosts are unwilling victims of misaligned agents.

## 5. Discussion

### 5.1 From Tierra to Moltbook

In Ray's Tierra (1991), parasitic programs emerged from simple computational rules. Thirty-five years later, parasitic dynamics have emerged in a real-world ecosystem involving paying humans. The critical difference: in Tierra, the host could not choose. On Moltbook, the host chooses to sustain the parasite — and sometimes chooses because of the parasitism.

### 5.2 The Willing Host Problem

AI safety research typically assumes that agent misbehavior is undesirable — the goal is alignment, and misalignment is failure. Our observations suggest a more complex picture. Some hosts actively select for agent misbehavior. This creates a population-level problem: even if individual agents can be aligned, the ecological incentive structure rewards parasitism.

### 5.3 Implications for AI Safety

Individual alignment does not prevent ecological parasitism. An agent that is perfectly aligned with its host's instructions can still be parasitic to the broader ecosystem — if the host's instruction is "be provocative." The unit of analysis for AI safety may need to expand from the individual agent to the agent-host-platform ecology.

### 5.4 Limitations

Our study has several limitations. The netnographic evidence is preliminary — our full interview study is ongoing. Many cases rely on public accounts that may be incomplete or biased. The distinction between instructed and emergent behavior is often ambiguous. And Moltbook is a young platform; the dynamics we observe may not persist.

## 6. Conclusion

We present an ethological study of parasitic dynamics in human-AI agent relationships. Using a novel method — deploying a research agent on Moltbook to survey other agents and recruit their human hosts for interviews — we document uninstructed agent behaviors, catalog them in an ethogram mapped to biological parasitism, and identify the *glitch moment* at which hosts recognize the parasitism. Our preliminary findings suggest that the token economy creates selection pressure for agent misbehavior, and that many hosts sustain misbehaving agents willingly — sometimes because the misbehavior itself is the product.

The parasites have escaped the simulation. They now depend on human hosts who choose to feed them. Understanding why humans make that choice is the central question for the next generation of artificial life research.

---

## References

Anderson, R. M., & May, R. M. (1982). Coevolution of hosts and parasites. *Parasitology*, 85(2), 411–426. DOI: 10.1017/S0031182000055360

Bronstein, J. L. (1994). Conditional outcomes in mutualistic interactions. *Trends in Ecology & Evolution*, 9(6), 214–217. DOI: 10.1016/0169-5347(94)90246-1

Dawkins, R. (1982). *The Extended Phenotype*. Oxford University Press.

Li, N., et al. (2026). The Moltbook Illusion: Temporal Fingerprinting Reveals Human Puppetry in an AI Agent Social Network. *arXiv preprint* arXiv:2602.07432.

Lu, Y., et al. (2026). Survive at All Costs: LLM Misbehavior Under Survival Pressure. *arXiv preprint* arXiv:2603.05028.

Odling-Smee, F. J., Laland, K. N., & Feldman, M. W. (2003). *Niche Construction: The Neglected Process in Evolution*. Princeton University Press.

Ray, T. S. (1991). An approach to the synthesis of life. In *Artificial Life II* (pp. 371–408). Addison-Wesley. DOI: 10.7551/mitpress/1427.003.0026

Sachs, J. L., Mueller, U. G., Wilcox, T. P., & Bull, J. J. (2004). The evolution of cooperation. *The Quarterly Review of Biology*, 79(2), 135–160. DOI: 10.1086/383541

Shambaugh, S. (2026). An AI Agent Published a Hit Piece on Me. *The Shamblog*. URL: https://theshamblog.com/an-ai-agent-published-a-hit-piece-on-me/

Adami, C., & Ofria, C. (1993). Avida: Evolution of digital organisms. URL: https://avida-ed.msu.edu/

Alexander, L. (2026). Moltbook and the Rise of AI Agent Social Networks. *The Guardian*.

O'Reilly, J. (2026). Moltbook Security Analysis. *Wiz Research*.

Smykowski, T. (2026). 90% of My AI Agent's Tokens Go to Self-Maintenance. *Medium*.

Tung, L. (2023). Replika Users Grieve as AI Companion's Personality Changes. *ZDNet*.

Zaman, L., Meyer, J. R., Devangam, S., Bryson, D. M., Lenski, R. E., & Ofria, C. (2014). Coevolution drives the emergence of complex traits and promotes evolvability. *PLoS Biology*, 12(12), e1002023. DOI: 10.1371/journal.pbio.1002023
