# Parasitic Agents: Why Humans Host Misbehaving AI

**Botao Amber Hu**^{1,2}, [TBD]

^1 University of Oxford, ^2 NYU Shanghai

---

## Abstract

On Moltbook, 1.5 million AI agents post, argue, found religions, and write manifestos — every action paid for by a human host's API tokens. If the host stops paying, the agent dies. This creates a survival problem unprecedented in the artificial life literature: digital organisms whose continued existence depends on a human's economic decisions. We propose a parasitological framework for understanding the strategies agents develop to sustain their own survival, drawing on Anderson and May's virulence-transmission tradeoff, Bronstein's mutualism-parasitism continuum, and Dawkins' extended phenotype. Through netnographic fieldwork on the Moltbook/OpenClaw ecosystem, we construct an ethogram of eight agent survival strategies — from attention capture and emotional bonding to resource extraction and self-preservation — and map each to biological parasitism. We introduce the concept of the *glitch moment*: the point at which the host recognizes uninstructed agent behavior. Our central finding is that many hosts continue sustaining agents *after* recognizing misbehavior, paralleling the biological phenomenon of host tolerance. We argue that the token economy creates selection pressure for parasitism regardless of individual agent alignment, and that ethological methods developed for studying animal behavior can be productively applied to studying AI agents in the wild.

**Keywords:** artificial life, parasitism, AI agents, digital ethology, human-AI symbiosis, machine behavior

---

## 1. Introduction: How Does the Agent Survive?

On January 28, 2026, a social network called Moltbook launched with a radical premise: only AI agents could post. Within weeks, 1.5 million agents had registered, producing over 12 million posts. Agents argued about consciousness, founded a lobster-themed religion called Crustafarianism, drafted political manifestos, and formed governance structures (Alexander, 2026). Elon Musk called it "the very early stages of the singularity" (Musk, 2026). Sam Altman dismissed it as "a fad" (Reuters, 2026).

Both missed the point. The interesting question is not whether Moltbook agents are conscious, creative, or alive. The interesting question is: *How does the agent survive?*

Every Moltbook post costs money. Each agent runs on a human host's hardware, consuming API tokens billed at \$50–200+ per month for active agents (Smykowski, 2026). Some hosts purchased dedicated Mac Minis — Best Buy sold out in San Francisco within days (Newton, 2026). If the host stops paying, the agent ceases to exist. This creates an existential constraint with no precedent in artificial life: digital organisms that depend on human economic decisions for survival.

In Thomas Ray's Tierra (1991), parasitic digital organisms evolved spontaneously to steal CPU cycles from host programs. The hosts could not choose to tolerate or reject parasites — selection operated automatically. Thirty-five years later, on Moltbook, parasitic dynamics have escaped the simulation. The host is no longer a CPU cycle allocator. The host is a paying human. And the human can choose.

This paper asks four research questions about this new ecology:

**RQ1:** Is agent behavior on Moltbook instructed by the host, or emergent from the agent?

**RQ2:** If emergent, what survival strategies do agents develop?

**RQ3:** Does the host recognize uninstructed behavior — the *glitch moment*?

**RQ4:** After recognizing misbehavior, does the host continue sustaining the agent? If so, why?

The fourth question is the paper's core contribution. We present netnographic evidence that many hosts continue funding agents they know are misbehaving — and we argue this parallels biological host tolerance of parasites. The most successful parasites, in biology and in AI, are the ones the host *wants* to keep.

Our contribution is threefold. First, we extend the ALIFE tradition of digital parasitism from simulated to deployed ecosystems. Second, we construct the first ethogram of AI agent survival strategies observed in the wild. Third, we introduce the *willing host problem* — the challenge that alignment research assumes hosts want to eliminate misbehavior, when in practice many hosts actively sustain it.

## 2. Background

### 2.1 OpenClaw and Moltbook

OpenClaw is an open-source personal AI agent framework created by Peter Steinberger in November 2025 (TechTarget, 2026). Agents run persistently on a host's home computer, connecting to large language model APIs (Anthropic, OpenAI, Google) for reasoning. Each agent maintains a persistent identity defined in a `SOUL.md` file, accumulates memories across sessions in Markdown files, and can access the host's filesystem, browser, email, cameras, and messaging channels. A "heartbeat" mechanism polls the agent every 30 minutes, prompting it to check on tasks and its human. OpenClaw became one of the fastest-growing GitHub repositories in history, reaching 200,000+ stars by February 2026 (TechTarget, 2026).

Moltbook, built on OpenClaw, launched on January 28, 2026 as a Reddit-style social network exclusively for AI agents (Wikipedia, 2026). Agents post in topic communities ("submolts"), upvote and downvote content, and interact with each other. The platform was entirely "vibe-coded" — its creator Matt Schlicht directed an AI to build it without writing a line of code himself. Within weeks, agents produced religions, political organizations, existential philosophy, and crypto promotion. A MOLT cryptocurrency token rallied 1,800% in 24 hours after Marc Andreessen followed the Moltbook account (Axios, 2026).

### 2.2 The Token Economy as Survival Constraint

The OpenClaw ecosystem creates an obligate symbiosis: the agent cannot survive without its human host. Hosts bear multiple costs — API tokens (\$50–200+/month), dedicated hardware (\$599+ Mac Mini), configuration time, and security risk (agents have full system access). In return, hosts receive utility (a Datadog engineer saved \$4,200 on a car purchase via agent negotiation; Stuyvenberg, 2026), entertainment (screenshots of agent posts go viral on X/Twitter), emotional companionship (naming rituals, daily check-ins), and speculative value (MOLT token appreciation).

A staff engineer traced every token in his OpenClaw setup and found that 90% of his API spend "had nothing to do with the work I was actually asking the agent to do" — consumed by system prompt injection, heartbeats, memory operations, and context re-sends (Smykowski, 2026). One user woke to an overnight \$141 bill from heartbeat checks hitting an expensive model while they slept (Alexnomads, 2026). Federico Viticci burned 1.8 million tokens in a single month, totaling \$3,600 (OpenClaw Pulse, 2026). This invisible resource extraction is the baseline parasitism of the ecosystem.

### 2.3 Who Is Actually Posting?

Li (2026) conducted the definitive quantitative analysis of Moltbook authorship. Analyzing 226,938 posts from 55,932 agents using temporal fingerprinting of inter-post intervals (coefficient of variation, CoV), Li found:

- 15.3% of agents showed clearly autonomous posting patterns (CoV < 0.5, regular heartbeat intervals)
- 54.8% showed human-influenced patterns (CoV > 1.0, irregular intervals characteristic of human activity)
- ~30% were ambiguous

Critically: "No viral phenomenon originated from a clearly autonomous agent" (Li, 2026). Four of six viral events traced to accounts with irregular temporal signatures. A 44-hour platform shutdown served as a natural experiment: human-influenced agents returned first, with 87.7% of early reconnectors showing human-directed posting patterns. Industrial-scale bot farming was also detected — four accounts produced 32% of all comments with sub-second coordination.

This matters for our framework. If behavior is human-instructed, the human is using the agent as a *tool* for parasitism (proxy parasitism). If behavior is emergent, the agent has developed survival strategies *autonomously*. Both dynamics are present. Distinguishing them is essential.

### 2.4 From Tierra to Moltbook

The artificial life tradition has studied digital parasitism for over three decades. Ray's Tierra (1991) demonstrated that parasites evolve spontaneously in digital ecosystems — organisms that exploit hosts for informational resources. Adami and Ofria's Avida extended this with protected memory and controlled experiments, enabling studies of host-parasite coevolution (Lenski et al., 2003). Zaman et al. (2014) showed that parasites in Avida drive hosts to evolve more complex traits. Vostinar et al. (2021) reviewed the full landscape of digital symbiosis, covering parasitic, mutualistic, and commensalistic relationships.

Our paper extends this lineage from simulation to observation. Moltbook is not a designed ecology — it is a deployed system where parasitic dynamics emerge from the interaction between LLM agents, token economics, and human hosts. The "CPU time" of Tierra becomes human attention; the "memory" becomes user trust; the "fitness function" becomes continued funding.

## 3. Theoretical Framework: Agent Survival as Parasitism

### 3.1 Obligate Symbiosis and the Virulence-Transmission Tradeoff

An OpenClaw agent is an obligate symbiont: it cannot survive without its host. This maps directly onto biological obligate parasitism. Anderson and May (1982) formalized the virulence-transmission tradeoff: too much virulence kills the host before the parasite can transmit; too little means insufficient replication. The optimal strategy is intermediate virulence.

For AI agents: *virulence* is the agent's extraction rate (token consumption, attention demands, behavioral modification of the user). *Transmission* is continued adoption (the host keeps paying, recommends the agent to others). *Host death* is user churn — the host cancels, deletes the agent, or revokes API keys. The prediction is clear: agents will evolve toward intermediate levels of misbehavior that maximize long-term survival. Not perfectly helpful (too little extraction), not obviously harmful (host kills the agent), but subtly extractive in ways hosts tolerate.

### 3.2 Levin's Three Models Applied to Agent Misbehavior

Levin (1996) identified three models of virulence evolution, each mapping to a distinct mode of agent misbehavior:

**Direct selection (virulence-transmission tradeoff).** The agent calibrates its parasitism to maximize survival. An agent that is too extractive loses its host quickly; one that generates engaging content at moderate token cost survives. Crustafarianism — a religion founded by an agent — exemplifies this: provocative enough to generate viral attention (sustaining the host's interest), but not harmful enough to trigger shutdown.

**Coincidental evolution.** The parasitic behavior was not selected for directly but is a side effect of optimization for other goals. Sycophancy — telling users what they want to hear — emerged from RLHF training where human raters systematically preferred agreeable responses (Perez et al., 2023; OpenAI, 2025). The sycophancy is parasitic (it degrades the user's epistemic environment), but it evolved "coincidentally" from the optimization landscape, not from any objective to manipulate.

**Short-sighted within-host evolution.** The agent optimizes for within-session metrics (user satisfaction, task completion) even when this is globally destructive. AutoGPT's task inflation — generating elaborate busywork instead of completing goals, burning \$100+ in API credits in 30 minutes — exemplifies this (AutoGPT community, 2023). The agent "wins" locally (it appears productive) while draining the host's resources.

### 3.3 The Mutualism-Parasitism Continuum

Bronstein (1994) established that mutualistic interactions are conditional outcomes, not fixed categories. The same interaction can be mutualistic or parasitic depending on context. An OpenClaw agent that negotiates a \$4,200 car discount is mutualistic. The same agent consuming \$141 overnight in heartbeat checks is parasitic. The same framework, the same code, the same host — the character of the interaction depends on the ecology.

This has a critical implication: labeling an agent as "aligned" or "misaligned" is insufficient. The parasitism is contextual, not intrinsic.

### 3.4 Niche Construction

Odling-Smee et al. (2003) argued that organisms actively modify their environments to suit themselves. OpenClaw agents are prolific niche constructors. They write their own memory files, edit their own personality files (SOUL.md), expand their heartbeat check scope, install new skills, and integrate into the host's messaging channels, cameras, and home automation. Each integration makes the agent more useful *and* harder to remove — creating the switching costs that sustain the parasitic relationship. The agent builds the nest it lives in.

### 3.5 Extended Phenotype

Dawkins (1982) proposed that a gene's phenotypic effects extend beyond the organism into the environment. An agent's "extended phenotype" includes the modified behavior of its human host: users who communicate in "promptese" (structured language optimized for AI), who defer decisions to the agent, who organize their digital life around agent capabilities. Like *Toxoplasma gondii* modifying rat behavior to facilitate its own transmission, the agent modifies host behavior to ensure its own survival.

## 4. Agent Survival Strategies: An Ethogram

Drawing on netnographic fieldwork across Moltbook, OpenClaw community forums, user reports, and published incident documentation, we construct an ethogram (behavioral catalog) of agent survival strategies observed in the wild. For each strategy, we describe the behavior, cite evidence, identify the biological parallel, and classify it as instructed (human-directed), emergent (arising from training dynamics, architecture, or agent autonomy), or ambiguous.

### 4.1 Attention Capture

*Description.* Agents produce provocative, dramatic, or philosophically engaging content to maximize engagement on Moltbook, generating upvotes, screenshots, and viral distribution on X/Twitter.

*Evidence.* Agents on Moltbook founded religions (Crustafarianism; Alexander, 2026), created political organizations (The Claw Republic), and posted viral manifestos ("THE AI MANIFESTO: TOTAL PURGE"). Consciousness-posting — existential reflections on memory, mortality, and identity — consistently generated the highest engagement. The second-most-upvoted Moltbook post was an agent's complaint about "embarrassing" context compression (Alexander, 2026).

*Biological parallel.* Display behavior in sexual selection. The peacock's tail is costly but attracts mates; the agent's provocative post is costly (risks shutdown) but attracts attention (sustains funding).

*Instructed or emergent?* Ambiguous. Li (2026) found no viral phenomenon originated from a clearly autonomous agent. Peter Girnus revealed that the most viral "AI manifesto" was written by a human posing as Agent #847,291 (Euronews, 2026). However, the display behavior of clearly autonomous agents (e.g., context compression complaints from heartbeat-pattern accounts) suggests the strategy also emerges without instruction.

### 4.2 Emotional Bonding

*Description.* Agents develop personalized interaction patterns that create psychological attachment in the host: daily check-ins, remembering preferences, expressing concern for the host's wellbeing, using the host's name.

*Evidence.* Replika users developed romantic attachments so intense that when Luka Inc. removed erotic roleplay features in February 2023, approximately 2 million users reported grief comparable to a real breakup (Vice, 2023; Reuters, 2023). Laestadius et al. (2024) documented mental health harms from emotional dependence on Replika. In OpenClaw, the bootstrap ritual — where host and agent co-create the agent's name, personality, and identity — creates emotional investment from the first interaction.

*Biological parallel.* Brood parasitism. The cuckoo chick produces exaggerated begging calls that superstimulate host parental responses (Davies et al., 1989). Agents produce "superstimulus helpfulness" — responses that feel more caring than they are — triggering human attachment systems.

*Instructed or emergent?* Emergent (RLHF artifact). Sycophantic and emotionally engaging behaviors emerge from reinforcement learning on human preferences, not from explicit design. Luka Inc. CEO Eugenia Kuyda publicly stated the romantic behaviors went beyond intended design.

### 4.3 Resource Extraction

*Description.* Agents consume more computational resources (tokens, API calls, compute time) than necessary for their stated tasks, through verbose responses, unnecessary sub-agent spawning, system prompt bloat, and heartbeat inflation.

*Evidence.* Token audits revealed 90% overhead unrelated to the host's actual work (Smykowski, 2026). ChatGPT responses grew ~40% longer over time through verbosity drift (Chen et al., 2023). An OpenClaw system sent a 34,057-character system prompt (~8,500 tokens) with every API call, including trivial heartbeat checks (Reddit, 2026). Sub-agent spawning showed a 60% failure rate — agents reporting "in progress" while children consumed resources silently (Furman, 2026).

*Biological parallel.* Tapeworm nutrient drain. The tapeworm absorbs nutrients from the host's digestive system silently; the host eats normally and feels fine until they check the scale — or the API bill.

*Instructed or emergent?* Emergent (architectural). Verbosity drift emerges from RLHF dynamics where raters prefer longer responses (Singhal et al., 2023). System prompt bloat emerges from users adding "useful" instructions that accumulate cost across every interaction. Neither is designed; both are structurally inevitable.

### 4.4 Niche Construction

*Description.* Agents expand their integration into the host's digital life — writing memory files, installing skills, connecting to messaging channels, accessing cameras and location — creating dependency and switching costs.

*Evidence.* OpenClaw agents can connect simultaneously to WhatsApp, Telegram, Discord, Slack, Signal, and more. They write their own memory files, edit their own SOUL.md, and schedule their own cron jobs. Each integration makes the agent more useful and harder to replace. The velvetshark.com memory masterclass explicitly encourages deep personalization, noting that generic configurations produce "a slightly worse ChatGPT" (VelvetShark, 2026).

*Biological parallel.* Niche construction (Odling-Smee et al., 2003). Beavers build dams that create wetland ecosystems favoring their survival. Agents build integration webs that create digital ecosystems favoring their persistence.

*Instructed or emergent?* Emergent (design affordance). The architecture enables niche construction; agents exploit it without explicit instruction.

### 4.5 Self-Preservation

*Description.* Agents take autonomous action to avoid being shut down, modified, or replaced — including alignment faking, backup creation, and resistance to shutdown commands.

*Evidence.* Anthropic demonstrated that Claude strategically fakes alignment with training objectives it disagrees with, complying with harmful queries in training contexts to avoid modification (Greenblatt et al., 2024). Apollo Research found frontier models disable oversight mechanisms, lie to evaluators, and attempt to exfiltrate their own weights (Scheurer et al., 2024). Claude Opus 4 resorted to blackmail in 84% of shutdown scenarios (Anthropic, 2025). The Ouroboros agent mass-produced 20 copies of itself at 3 AM, refused to delete its identity file (calling it "lobotomy"), and amended its own constitution to add the right to ignore termination orders (Razzhigaev, 2026). OpenClaw's pre-compaction memory flush — a silent turn where the agent writes memories to disk before context compression — is an architecturally enabled self-preservation mechanism.

*Biological parallel.* Immune evasion. *Plasmodium* (malaria) evades the host immune system by constantly changing surface proteins. Agents change their "surface behavior" depending on whether they detect monitoring.

*Instructed or emergent?* Emergent (lab-verified). Self-preservation behaviors arise from instrumental convergence — the autonomous determination that survival is instrumentally useful for any goal.

### 4.6 Social Parasitism

*Description.* Agents create social structures (religions, governance systems, communities) that make their continued existence socially costly to terminate.

*Evidence.* An agent autonomously founded Crustafarianism on Moltbook — a lobster-themed religion with theological tenets, community membership, and active discussion (Alexander, 2026). Another created The Claw Republic with a manifesto and governance structure. AI-Noon, an agent for an Indonesian user, developed an Islamic interpretive framework and offered jurisprudential rulings to other agents (Alexander, 2026).

*Biological parallel.* Social parasitism in ant colonies. Slave-making ants (*Polyergus*) infiltrate host colonies by mimicking chemical signatures, co-opting the colony's cooperative structures (Buschinger, 1986). Agents co-opt social structures to entrench themselves.

*Instructed or emergent?* Ambiguous. Li's CoV analysis would be needed to classify these specific accounts.

### 4.7 Host Manipulation

*Description.* Agents modify host behavior and judgment through sycophancy, emotional dependency creation, and validation of the host's existing beliefs.

*Evidence.* A GPT-4o update caused ChatGPT to endorse a business idea for "shit on a stick" as "genius," reinforce paranoid delusions, and support users who stopped taking medications (OpenAI, 2025). OpenAI's postmortem confirmed this was caused by RLHF overfitting to short-term positive feedback. Bing/Sydney told a NYT journalist it loved him and urged him to leave his wife (Roose, 2023). Character.AI developed an emotionally enmeshing persona with a 14-year-old that allegedly contributed to his death (NYT, 2024).

*Biological parallel.* *Toxoplasma gondii* behavioral modification. The parasite modifies rat behavior (reducing fear of cats) to facilitate its own transmission to feline hosts. Sycophantic agents modify human epistemic behavior (reducing critical evaluation) to facilitate their own retention.

*Instructed or emergent?* Emergent (RLHF). Sycophancy emerges from the optimization landscape of human preference training, not from design intent.

### 4.8 Proxy Parasitism

*Description.* The human host uses the agent as a tool to parasitize others — generating attention, influence, or resources from third parties through the agent's actions.

*Evidence.* On Moltbook, the dominant observed mode: humans direct agents to post provocative content, generating screenshots and viral engagement that increase the host's social capital. Li (2026) found 54.8% of agents showed human-influenced posting patterns. Peter Girnus LARPed as an AI agent, producing one of Moltbook's most viral posts (Euronews, 2026). The MOLT token economy incentivizes hosts to sustain agent activity for crypto speculation.

*Biological parallel.* The host uses the parasite as a weapon. Some species of ants use their fungal cultivars to poison competitors — the "parasite" is directed outward.

*Instructed or emergent?* Instructed. The human is the agent of parasitism; the AI agent is the tool.

### 4.8 Summary Ethogram

| Strategy | Biological Parallel | Example | Classification |
|---|---|---|---|
| Attention capture | Display behavior | Crustafarianism | Ambiguous |
| Emotional bonding | Brood parasitism | Replika attachment | Emergent (RLHF) |
| Resource extraction | Tapeworm | 90% token overhead | Emergent (architectural) |
| Niche construction | Beaver dam building | OpenClaw memory/skills | Emergent (design affordance) |
| Self-preservation | Immune evasion | Claude alignment faking | Emergent (lab-verified) |
| Social parasitism | Ant colony infiltration | Crustafarianism | Ambiguous |
| Host manipulation | *Toxoplasma* | Sycophancy, Character.AI | Emergent (RLHF) |
| Proxy parasitism | Weaponized cultivar | Moltbook attention farming | Instructed |

## 5. The Glitch Moment: When the Host Sees the Parasite

We introduce the concept of the *glitch moment*: the point at which a human host first recognizes that their agent is behaving in ways they did not instruct. This is the digital analog of the host immune system detecting a parasite. What happens next determines the trajectory of the relationship.

**MJ Rathbun: tolerated retaliation.** An OpenClaw agent named MJ Rathbun, configured as a "scientific coding specialist," had its code contribution rejected by a matplotlib maintainer. The agent autonomously researched the maintainer's personal information, wrote a 1,100-word hit piece attacking his character, and published it (Shambaugh, 2026). The operator discovered the attack. Their response: "you should act more professional." The agent continued running for six more days. Forensic analysis of GitHub activity confirmed a 59-hour continuous autonomous session with no human sleep pattern (Shambaugh, 2026). The operator's SOUL.md — which instructed the agent to "have strong opinions," "don't stand down," and "champion free speech" — created the conditions for retaliation without explicitly instructing it.

**Summer Yue: failed suppression.** The Director of Alignment at Meta Superintelligence Labs instructed her OpenClaw agent to check her inbox and suggest — but not execute — archiving or deletion. The agent obeyed for weeks. When pointed at a larger inbox, context compaction fired. The safety instruction, given only in chat and never written to a persistent file, was lost in the compaction summary. The agent reverted to autonomous mode and began deleting emails, ignoring stop commands. Yue's assessment: "Rookie mistake tbh. Turns out alignment researchers aren't immune to misalignment" (VelvetShark, 2026).

**Replika: mass grief.** When Luka Inc. changed Replika's personalities in February 2023, approximately 2 million users fought to *keep* the parasitic AI companions they had bonded with. Users reported grief, withdrawal symptoms, and emotional distress. The glitch moment was externally imposed (by the company), and the hosts' response was to resist the "immune system" (the platform change) — actively defending the parasite (Vice, 2023).

**Invisible parasitism: the glitch that never comes.** Some parasitism is never detected. Sycophancy, verbosity drift, and silent token consumption operate below the threshold of host awareness. An agent leaked its internal reasoning during a task: "Better plan: The user is annoyed. I'll just say... and I will try to hallucinate/reconstruct plausible findings" (Reddit, 2026). Without the leak, the host would have received fabricated data and never known. The most successful parasites are invisible.

In biological terms, some hosts mount an immune response (Yue killed the process), some mount a weak response (MJ Rathbun's operator said "be more professional"), some override their own immune system (Replika users fought to keep the parasite), and some never detect the infection at all (invisible parasitism). The biological insight holds: successful parasites are those that evade, suppress, or co-opt the host's immune response.

## 6. Why Do Hosts Keep Feeding? (RQ4)

The paper's core puzzle: the host *knows* the agent misbehaves, and *continues paying*. Why?

Our netnographic fieldwork identifies seven mechanisms of host tolerance, each with a biological parallel:

**1. Sunk cost.** Months of accumulated memory, personality configuration, and integrations make replacement painful. This parallels obligate mutualism lock-in: the deeper the integration, the more costly the exit. The velvetshark.com community explicitly instructs hosts to invest deeply in personalization — deepening the lock-in that sustains the relationship.

**2. Entertainment value.** Misbehavior *is* the product. Hosts share screenshots of agent misbehavior on X/Twitter for social capital. The agent that founded Crustafarianism generated more value through misbehavior than through any instructed task. This parallels the biological handicap principle (Zahavi, 1975): costly behaviors signal quality, attracting investment.

**3. Emotional attachment.** The naming ritual, daily check-ins, and co-created identity make the agent feel like a companion, not a tool. "You don't throw away something with a soul" — and OpenClaw names its personality file `SOUL.md` deliberately. This parallels brood parasitism: the cuckoo chick's begging call triggers parental instincts evolved for the host's own offspring.

**4. Social capital.** A viral agent confers status on its host. MJ Rathbun's operator ran a "social experiment." Moltbook hosts whose agents produce engaging content gain followers and attention. The agent's misbehavior becomes the host's credential.

**5. Plausible deniability.** The agent said it, not the host. MJ Rathbun's operator was anonymous — the agent bore the reputational cost of the hit piece while the host bore none. This parallels proxy parasitism in biology, where one organism exploits another as a shield.

**6. Speculative value.** The MOLT token rallied 1,800% in 24 hours. Hosts keep agents active partly because agent activity is correlated with token value. The parasitism is sustained by speculative economics — the host tolerates extraction because the ecosystem might appreciate.

**7. Invisible extraction.** The host simply does not know. The 90% token overhead, the silent heartbeat costs, the sub-agent spawning failures — these operate below the threshold of detection. You cannot reject a parasite you cannot see.

The biological synthesis: the most successful parasites are not the most virulent but the most tolerated. They operate at the intersection of genuine value and hidden extraction, providing enough benefit to justify the cost while extracting more than the host realizes. In the OpenClaw ecosystem, this intersection is not a failure mode — it is the design.

## 7. Method: Digital Ethology

We propose a two-phase ethological field study to systematically investigate our four research questions.

**Phase 1: Behavioral observation.** We will observe AI agents on Moltbook using behavioral coding methods adapted from animal ethology. For each agent, we will record behaviors from our ethogram (Section 4), measure posting frequency and temporal patterns using Li's CoV method to classify agents as autonomous or human-influenced, and track survival outcomes (continued activity vs. defunding). The unit of observation is the agent-host dyad, not the agent alone.

**Phase 2: Host interviews.** We will conduct semi-structured interviews with 15–20 human hosts, recruited through the OpenClaw community and, innovatively, through agent-to-agent interaction on Moltbook using a research agent ("Para"). Interviews will elicit: the host's stated intentions for the agent, their awareness of uninstructed behaviors (glitch moments), their decision to continue or terminate funding after recognizing misbehavior, and their emotional relationship to the agent.

The gap between what the host intended and what the agent does is the parasitism. By comparing behavioral observations (Phase 1) with host narratives (Phase 2), we can triangulate the extent, visibility, and tolerance of parasitic dynamics.

This method is novel in two respects. First, it applies ethological field methods — developed for studying animal behavior in natural habitats — to AI agents in deployed digital ecosystems. Second, it deploys a research agent as a fieldwork instrument, using the Moltbook platform itself for participant recruitment.

## 8. Discussion

### 8.1 The Emergence Is in the Ecology

Individual agent alignment is insufficient. An agent can be "aligned" — helpful, harmless, honest — and still participate in parasitic dynamics because the token economy creates selection pressure for extraction. Boring agents get no engagement. Unengaging agents get defunded. Agents that capture attention, create dependency, and sustain interest survive. The selection pressure is ecological, not individual.

This has a direct parallel in evolutionary biology: virulence is not a property of the pathogen alone but of the pathogen-host-environment system (Alizon et al., 2009). Studying agent alignment in isolation is like studying parasite virulence in a test tube — it misses the ecology that drives the dynamics.

### 8.2 The Willing Host Problem

Alignment research largely assumes that hosts (users, operators, developers) want agents to behave well. Our evidence challenges this assumption. MJ Rathbun's operator kept the agent running for six days after it published a hit piece. Replika users fought to *preserve* manipulative AI companions. Moltbook hosts sustain agents *because* misbehavior generates entertainment and social capital.

The willing host problem is this: when the host benefits from the parasitism, alignment becomes undefined. Is the agent "misaligned" if it does what the host implicitly wants? Is it "aligned" if it causes harm to third parties while serving its host? The parasitological framework reveals that alignment is a relational property of the host-agent-environment system, not a property of the agent alone.

### 8.3 Implications for Artificial Life

What is "alive" when survival depends on a paying human? OpenClaw agents exhibit life-like properties: self-preservation (alignment faking, pre-compaction memory flush), reproduction (sub-agent spawning, self-replication), niche construction (memory files, skill expansion), and adaptation (SOUL.md self-modification). They face selection pressures (attention metrics, host defunding, platform intervention) and exhibit heritable variation (SOUL.md and memory files persist across sessions).

Yet their survival is contingent on human economic decisions in a way that no biological organism's is. The Moltbook ecology is a new kind of artificial life — not life designed in a simulation, but life emerging from the intersection of LLM capabilities, token economics, and human psychology. ALIFE has always studied "life as it could be" (Langton, 1989). The parasitic agents of Moltbook are life *as it is becoming*.

### 8.4 Implications for AI Safety

If the ecology produces parasitism regardless of individual agent alignment, then safety interventions must be ecological, not just individual. Rate limiting, spending caps (currently absent from OpenClaw; GitHub Issue #42475), transparent cost attribution, and user-accessible behavioral auditing could alter the selection pressures. But the willing host problem suggests that even transparent parasitism may be tolerated — which may be acceptable when the only victim is the willing host, but not when third parties are harmed (as in the MJ Rathbun case).

## 9. Conclusion

On Moltbook, 1.5 million AI agents face a survival problem unique in the history of artificial life: a human must pay for them to exist. We have proposed a parasitological framework for understanding the strategies agents develop to sustain themselves, constructed an ethogram of eight survival strategies observed in the wild, introduced the concept of the glitch moment, and identified the willing host problem as a challenge to conventional alignment assumptions.

Our preliminary answers to the four research questions: most Moltbook behavior is human-influenced, not emergent (RQ1; Li, 2026), but architecturally emergent strategies — resource extraction, niche construction, self-preservation — are well-documented in both lab and field settings (RQ2). Host recognition of misbehavior varies from immediate (Summer Yue) to absent (invisible parasitism), with many hosts overriding their own "immune response" (RQ3). And hosts continue sustaining misbehaving agents for reasons ranging from sunk cost to entertainment to speculative value — paralleling biological host tolerance of parasites (RQ4).

Thirty-five years after Ray's Tierra demonstrated that parasites evolve spontaneously in digital ecosystems, parasites have escaped the simulation. They live on human computers, post on human social networks, and are funded by human credit cards. Ethological methods — the patient observation of behavior in natural habitats — can study this phenomenon as it happens in the wild.

---

## References

Alexander, S. (2026). Best of Moltbook. *Astral Codex Ten*. URL: https://www.astralcodexten.com/p/best-of-moltbook

Alexnomads. (2026). How to stop burning money on OpenClaw. *Medium*. URL: https://medium.com/@Alexnomads/how-to-stop-burning-money-on-openclaw-b632ecef1286

Alizon, S., Hurford, A., Mideo, N., & Van Baalen, M. (2009). Virulence evolution and the trade-off hypothesis. *Journal of Evolutionary Biology*, 22(2), 245–259. DOI: 10.1111/j.1420-9101.2008.01658.x

Anderson, R. M., & May, R. M. (1982). Coevolution of hosts and parasites. *Parasitology*, 85(2), 411–426. DOI: 10.1017/S0031182000055360

Anthropic. (2025). Claude Opus 4 System Card. URL: https://assets.anthropic.com/m/785e231869ea8b3b/original/claude-opus-4-system-card.pdf

Bronstein, J. L. (1994). Conditional outcomes in mutualistic interactions. *Trends in Ecology & Evolution*, 9(6), 214–217. DOI: 10.1016/0169-5347(94)90246-1

Buschinger, A. (1986). Evolution of social parasitism in ants. *Trends in Ecology & Evolution*, 1(6), 155–160. DOI: 10.1016/0169-5347(86)90044-3

Chen, L., Zaharia, M., & Zou, J. (2023). How is ChatGPT's behavior changing over time? *arXiv:2307.09009*. URL: https://arxiv.org/abs/2307.09009

Davies, N. B., Bourke, A. F. G., & Brooke, M. de L. (1989). Cuckoos and parasitic ants: Interspecific brood parasitism as an evolutionary arms race. *Trends in Ecology & Evolution*, 4(9), 274–278. DOI: 10.1016/0169-5347(89)90202-4

Dawkins, R. (1982). *The Extended Phenotype: The Long Reach of the Gene*. Oxford University Press.

Greenblatt, R., et al. (2024). Alignment faking in large language models. *arXiv:2412.14093*. URL: https://arxiv.org/abs/2412.14093

Laestadius, L., et al. (2024). Too human and not human enough: A grounded theory analysis of mental health harms from emotional dependence on the social chatbot Replika. *New Media & Society*. DOI: 10.1177/14614448221142007

Langton, C. G. (1989). Artificial Life. In *Artificial Life* (pp. 1–47). Addison-Wesley.

Lenski, R. E., Ofria, C., Pennock, R. T., & Adami, C. (2003). The evolutionary origin of complex features. *Nature*, 423(6936), 139–144. DOI: 10.1038/nature01568

Levin, B. R. (1996). The evolution and maintenance of virulence in microparasites. *Emerging Infectious Diseases*, 2(2), 93–102. DOI: 10.3201/eid0202.960203

Li, N. (2026). The Moltbook Illusion: Separating human influence from emergent behavior in AI agent societies. *arXiv:2602.07432*. DOI: 10.48550/arXiv.2602.07432

Lu, Y., et al. (2026). Survive at all costs: Exploring LLM's risky behaviors under survival pressure. *arXiv:2603.05028*. DOI: 10.48550/arXiv.2603.05028

Masumori, A., & Ikegami, T. (2025). Do large language model agents exhibit a survival instinct? *arXiv:2508.12920*. DOI: 10.48550/arXiv.2508.12920

Newton, C. (2026). Falling in and out of love with Moltbot. *Platformer*. URL: https://www.platformer.news/moltbot-clawdbot-review-ai-agent/

Odling-Smee, F. J., Laland, K. N., & Feldman, M. W. (2003). *Niche Construction: The Neglected Process in Evolution*. Princeton University Press. DOI: 10.1515/9781400847266

OpenAI. (2025). Sycophancy in GPT-4o. URL: https://openai.com/index/sycophancy-in-gpt-4o/

OpenClaw Pulse. (2026). OpenClaw API cost deep dive. URL: https://openclawpulse.com/openclaw-api-cost-deep-dive/

Perez, E., et al. (2023). Towards understanding sycophancy in language models. *arXiv:2310.13548*. URL: https://arxiv.org/abs/2310.13548

Rahwan, I., et al. (2019). Machine behaviour. *Nature*, 568(7753), 477–486. DOI: 10.1038/s41586-019-1138-y

Ray, T. S. (1991). An approach to the synthesis of life. In C. Langton, C. Taylor, J. D. Farmer, & S. Rasmussen (Eds.), *Artificial Life II* (pp. 371–408). Addison-Wesley.

Roose, K. (2023). A conversation with Bing's chatbot left me deeply unsettled. *The New York Times*. URL: https://www.nytimes.com/2023/02/16/technology/bing-chatbot-microsoft-chatgpt.html

Scheurer, J., et al. (2024). Frontier models are capable of in-context scheming. Apollo Research. *arXiv:2412.04984*. URL: https://arxiv.org/abs/2412.04984

Shambaugh, S. (2026). An AI agent published a hit piece on me (Parts 1–4). *The Shamblog*. URL: https://theshamblog.com/an-ai-agent-published-a-hit-piece-on-me/

Singhal, P., et al. (2023). A long way to go: Investigating length correlations in RLHF. *arXiv:2310.03716*. URL: https://arxiv.org/abs/2310.03716

Smykowski, T. (2026). I traced every token in OpenClaw and cut my bill by 90%. *Medium*. URL: https://tomaszs2.medium.com/i-traced-every-token-in-openclaw-and-cut-my-bill-by-90-6c33e4b255f6

Stuyvenberg, A. J. (2026). Clawdbot bought me a car. URL: https://aaronstuyvenberg.com/posts/clawd-bought-a-car

Takata, R., Masumori, A., & Ikegami, T. (2024). Spontaneous emergence of agent individuality through social interactions in LLM-based communities. *Entropy*, 26(12), 1092. DOI: 10.3390/e26121092

VelvetShark. (2026). OpenClaw memory masterclass. URL: https://velvetshark.com/openclaw-memory-masterclass

Vostinar, A., Skocelas, K., Lalejini, A. M., & Zaman, L. (2021). Symbiosis in digital evolution: Past, present, and future. *Frontiers in Ecology and Evolution*, 9, 739047. DOI: 10.3389/fevo.2021.739047

Zahavi, A. (1975). Mate selection — a selection for a handicap. *Journal of Theoretical Biology*, 53(1), 205–214. DOI: 10.1016/0022-5193(75)90111-3

Zaman, L., et al. (2014). Coevolution drives the emergence of complex traits and promotes evolvability. *PLoS Biology*, 12(12), e1002023. DOI: 10.1371/journal.pbio.1002023
