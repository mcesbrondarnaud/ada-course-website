# VI. 📈 Modeling the Spread: Can We Forecast Negativity?

Up to now, we have built solid foundations to understand how negativity behaves online.

We have seen that:
- negativity is unevenly distributed across communities,
- it concentrates during waves,
- and it spreads through repeated interactions between the same actors.

At this point in the story, our bullied user has learned **how negativity propagates** — but a crucial question remains:
> **Is this propagation predictable?**
To answer this, we now formalize our observations with a **propagation model**.

The goal of this model is not to predict individual comments, but to test whether it is possible to **forecast the level of negativity of a community over time**, using information available in the recent past.
### From intuition to a model
We work at a **weekly timescale**, which previous analyses showed to be a good compromise between noise and signal.

For each cluster of communities, we try to predict the **negativity ratio at week _t+1_**, using information at week _t_.

Two fundamental mechanisms motivate the model:

1. **Persistence**  
   If a community is already negative, does it tend to remain negative?

2. **Exposure**  
   If a community receives negativity from its neighbors, does this increase its own future negativity?
Formally, the model can be written as:
\[
r_{i,t+1}
\;=\;
\alpha \, r_{i,t}
\;+\;
\beta_i \, (W r_t)_i
\;+\;
\varepsilon_{i,t}
\]

where:
- \( r_{i,t} \) is the negativity ratio of cluster \( i \) at week \( t \),
- \( \alpha \) captures **temporal persistence**,
- \( \beta_i \) is a **cluster-specific exposure coefficient**, allowing different communities to react differently,
- \( W \) is the **inter-cluster interaction matrix**,
- \( (W r_t)_i \) represents the **exposure** of cluster \( i \) to the negativity of other clusters,
- \( \varepsilon_{i,t} \) captures unobserved noise.

The exposure term \( (W r_t)_i \) is a **weighted sum of the negativity of other clusters**, where each weight \( W_{ij} \) represents how much cluster \( j \) interacts with (and sends negativity toward) cluster \( i \), and the weights are normalized so that highly connected neighbors contribute more to exposure.

In simple terms:  
**a community is influenced more by the negativity of communities it interacts with frequently.**
---

### Refining the model

To test alternative explanations, we extended the model by adding:
- external event covariates (capturing global news pressure),
- a binary indicator identifying whether a community was the direct target of an attack,
- and heterogeneous exposure coefficients \( \beta_i \), which turned out to be essential.

This last point is crucial: **communities do not all react in the same way to exposure**.

The heterogeneous exposure model provided the most robust fit and is the one we retain for interpretation.
---
### Does the model actually work?
[**Fig 6.1 — Observed vs. predicted negativity over time**]
<iframe src='https://flo.uri.sh/visualisation/26916498/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

The figure compares predicted negativity ratios with the observed ones.

Despite the inherent noise of online interactions, the model captures:
- the overall trends in negativity,
- the timing of the largest peaks,
- and long-term increases or decreases in hostility.

As expected, it does not predict every fluctuation perfectly ( online behavior is chaotic) but the fact that such a simple model can recover most large-scale dynamics is already meaningful.
This tells us something important:
> **Negativity is not random. It follows learnable patterns.**

### What really drives negativity?

Studying the statistical significance of the model’s coefficients (p-value < 0.05) reveals a clear message:

- **Exposure to negativity from neighboring communities is the strongest predictor** of future hostility.
- Past negativity alone plays a much smaller role.
- External global events contribute surprisingly little once exposure is accounted for.

However, the effect of exposure is **not uniform across communities**.
Some clusters are highly sensitive: when exposed to negativity, their own hostility rises sharply. Others are much more resilient.

To explore this, we visualize the exposure sensitivity of each cluster.
[**Fig 6.2 — Cluster-specific sensitivity to exposure**]
<iframe src='https://flo.uri.sh/visualisation/26910918/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

Only a few clusters show a statistically significant reaction to incoming negativity, but these clusters are the ones with the strongest propagation power. This is sufficient to explain much of the global dynamics observed earlier.
In other words:
> **A small number of highly sensitive communities can drive a large share of negativity spread.**

---

### What this means for someone being targeted
This modeling step confirms a central insight of our data story.
Negativity online:
- can be roughly forecasted,
- is driven mainly by exposure to hostile neighbors,
- and spreads outward from a limited set of highly influential sources.

For someone being bullied online, this has a key implication:
> **Stopping negativity is not only about individual resilience, it is about breaking propagation chains.**
But cutting these chains is not easy. It has to be done by bigger institutions than one individual person. Communities cannot simply isolate themselves from the rest of the network, nor can they ignore all sources of hostility.

So what *can* be done?
In the final part, we turn to defense strategies:  
**how communities respond when under attack — and which responses actually reduce future negativity.**
