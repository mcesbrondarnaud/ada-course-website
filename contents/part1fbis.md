## II. ⚔️ Mapping Conflicts: Who Attacks Whom?

Before studying how negativity spreads and how communities respond to it, we first need to understand **where the conflicts themselves come from**.

Negativity does not appear uniformly or randomly. In many cases, it concentrates between specific communities and follows recurring interaction patterns. To capture this, we explicitly identify **conflicts** between subreddits.

---

### From negative links to conflicts

We start at the **subreddit-pair level**.

For each pair of subreddits with enough activity to provide a reliable signal, we track the weekly number of negative links exchanged between them. Using a peak-detection method, we identify **bursts of unusually high negative activity**, which we interpret as **conflict episodes**.

Importantly, conflicts are detected **at the subreddit-pair level**, but we later aggregate them to the **cluster level** for interpretability.

This preserves fine-grained detection while allowing us to reason at the level of broader community groups.

---

### The conflict landscape between clusters

We first visualize how conflicts flow between clusters over time.

[**Fig 2.1 — Dynamic conflict network between clusters**]

In this animated network:
- nodes represent clusters,
- directed edges represent conflicts,
- edge thickness is proportional to the number of detected conflict episodes.

Even at a glance, two clusters clearly dominate the conflict space:  
**Informative** and **Politics**.

They appear both as major **sources** of conflicts and frequent **targets**, suggesting that they sit at the core of Reddit’s conflict dynamics.

---

### Internal vs external conflicts

To further characterize this behavior, we aggregate conflicts into a Sankey diagram.

[**Fig 2.2 — Sankey diagram of conflict flows (top cluster pairs)**]

This visualization separates:
- **intra-cluster conflicts** (within the same cluster),
- **inter-cluster conflicts** (between different clusters).

Once again, Informative and Politics stand out:
- they generate a large share of conflicts toward other clusters,
- but they also experience a substantial amount of **internal conflict**.

This reveals an important nuance:  
these clusters are not just “attackers”,  they are also deeply divided internally, reflecting strong ideological disagreements within their own communities.

---

### Who are the main sources of conflict?

To confirm this visual intuition, we compute the **share of conflicts originating from each cluster over time**.

[**Fig 2.3 — Share of conflicts as source over time**]

The pattern is striking:
- **Informative** dominates most of the timeline,
- **Politics** consistently follows,
- all other clusters contribute only marginally.

This confirms that conflicts are not evenly distributed across Reddit.  
A small number of ideologically charged communities act as **structural conflict hubs**.

In the context of our data story, these clusters resemble chronic sources of hostility — not because of individual bad actors, but because **ideological polarization naturally generates repeated confrontation**.

---

### Who gets attacked?

Finally, we analyze how conflicts are distributed across clusters in three roles:
- **outgoing conflicts** (being the source),
- **incoming conflicts** (being targeted),
- **internal conflicts** (fighting within the cluster).

We order clusters from left to right by their total number of interactions and compare the relative shares. Note that two clusters are missing because they were not in conflict with any other one, as they are really small and structurally different. 

[**Fig 2.4 — Incoming, outgoing, and internal conflict shares by cluster**]

This reveals a clear pattern:
- “soft” or entertainment-oriented clusters (Sports, Technology, Entertainment, Lifestyle) receive a **disproportionately large share of incoming conflicts**,
- while more controversial clusters (Informative, Politics) generate and absorb most conflicts internally or outward.

In other words:
> **small, less confrontational communities are more often the targets than the initiators.**

This strongly resembles a bullying dynamic:
- highly polarized communities generate conflict,
- quieter communities bear much of the incoming hostility.

---

### What this tells us

This conflict analysis shows that Reddit’s hostility follows patterns we would expect in real-world social dynamics:
- conflicts concentrate around ideological hubs,
- powerful actors both attack others and fight among themselves,
- smaller, less aggressive communities are more likely to be targeted.

With this conflict map in mind, we now turn to **when conflicts erupt**, and how negativity waves unfold over time.
