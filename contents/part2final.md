# Part 2 - dynamics 

While the previous section highlighted where negativity is concentrated on Reddit and how it flows between communities, it did not yet explain when negativity becomes most intense. In practice, hostility on Reddit does not remain constant over time. Instead, it tends to rise and fall in waves, with short periods during which negative interactions sharply intensify.

Understanding these temporal dynamics is essential. Peaks of negativity are precisely the moments when online discourse becomes most polarized, most visible, and potentially most influential. They may reflect reactions to external events, internal platform dynamics, or the activity of a small number of highly influential communities.


## Identifying statistically significant peaks (3.a.2)

To understand how negativity spreads across time, we first track the overall evolution of negative links across Reddit. This allows us to visualize waves of negativity — periods where hostility increases significantly. We then break this evolution into weekly bins to better understand the temporal spread of negativity. 
After identifying the overall evolution of negativity, we now focus on identifying significant peaks of hostility. These peaks indicate when negative interactions reached their highest levels, often tied to specific events or discussions on Reddit.

We examined the negativity ratio (the proportion of negative links relative to total links) over time and identified the most significant peaks in the data. By identifying these peaks, we can focus on the periods when negativity was at its highest.

[notebook + commentaires]




## Analyzing intra- and inter-cluster conflicts between subreddits

To further understand how negativity manifests across Reddit, we move from aggregate negativity measures to a pairwise conflict analysis between subreddits. Rather than focusing solely on volumes of negative links, this approach allows us to detect periods of unusually intense conflict between specific pairs of communities.

## Detecting conflict spikes using z-scores
For each pair of subreddits, we construct a weekly time series of negative interactions. To identify abnormal conflict intensity, we compute a z-score for each pair on a weekly basis, defined as the deviation from its historical mean.

To ensure statistical robustness:
- only pairs active for at least 4 weeks are retained,
- this filtering yields 1,119 valid subreddit pairs.

A conflict spike is defined as a weekly z-score greater than 2, indicating an unusually high level of negative interaction compared to the pair’s baseline behavior. This method allows us to focus on relative surges in conflict, rather than raw interaction counts.


### Week-by-week conflict dynamics

Using the detected spikes, we visualize conflicts on a week-by-week basis, where directed edges represent conflict between clusters.
The thickness of each arrow corresponds to the intensity of the conflict during that week: the larger the arrow, the stronger the negative interaction.

[Python file] 

This dynamic representation highlights that conflict is not uniformly distributed over time, but instead concentrates in short bursts involving specific cluster pairs.

A clear pattern emerges:
the Informative cluster appears to be the primary source of conflicts, closely followed by the Political cluster. These clusters repeatedly initiate or are involved in high-intensity conflict spikes across weeks.

To quantitatively support this observation, we examine the contribution of each cluster to overall conflict activity, as shown in the following plot:

<iframe src='https://flo.uri.sh/visualisation/26800720/embed' title='Cluster contribution to conflicts' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe>

This visualization confirms that a small number of clusters account for a disproportionate share of conflict spikes, reinforcing the idea that conflict dynamics are highly concentrated.



### Most conflictual cluster pairs

We then aggregate conflict spikes across time and identify the 15 cluster pairs with the highest number of conflicts. These pairs are visualized in a diagram that highlights recurrent antagonistic relationships between thematic clusters.

<iframe src='https://flo.uri.sh/visualisation/26805414/embed' title='Most conflictual cluster pairs' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe>

Two key observations stand out:
- A large share of conflicts are intra-cluster, suggesting that hostility often emerges within the same thematic communities.
- Among inter-cluster conflicts, the most prominent exchanges occur from Informative to Political clusters and vice versa, indicating a strong bidirectional antagonism between these two thematic domains.

This asymmetry highlights that while many clusters remain relatively isolated from conflict, a few thematic interfaces repeatedly generate tension.


### Clusters most involved in conflicts

Finally, we examine the five clusters most involved in conflict, accounting for both conflicts sent and conflicts received.

<iframe src='https://flo.uri.sh/visualisation/26805809/embed' title='Top clusters involved in conflicts' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe>

This analysis reveals heterogeneous roles across clusters. For example, the Gaming cluster sends relatively few conflicts to other clusters, yet receives a substantial amount of conflict. This suggests that some communities act primarily as targets rather than initiators of hostility.



## What Happens During Peaks? 

Once peaks are identified, we investigate how negativity is structured during these critical moments.
We test three hypotheses grounded in network contagion theory:

<section class="container my-4">
  <div class="row g-3">
    <div class="col-12 col-lg-4">
      <div class="card p-3 h-100">Hypothesis 1 — Source-driven peaks : A small number of subreddits act as primary sources of negativity, triggering global peaks.</div>
    </div>
    <div class="col-12 col-lg-4">
      <div class="card p-3 h-100">Hypothesis 2 — Neighborhood contagion : Subreddits that are neighbors of negativity sources become more negative during peaks than unrelated communities.</div>
    </div>
    <div class="col-12 col-lg-4">
      <div class="card p-3 h-100">Hypothesis 3 — Direct exposure effect : Subreddits directly exposed to negativity (through incoming links from sources) experience a stronger increase in negativity than other neighbors.</div>
    </div>
  </div>
</section>

These hypotheses allow us to distinguish between:
- general platform-wide negativity,
- structural propagation effects driven by network connections.

## Negativity Levels During Peaks: Sources, Neighbors, Others
To test these hypotheses, we compare negativity levels during peak periods across different groups of subreddits:
- Original sources of negativity,
- Recurrent neighbourgs,
- Other

<section class="container my-5">
<div class="row g-4 align-items-start">

<div class="col-12 col-lg-7">
<div class="card p-3">
<iframe src="https://flo.uri.sh/visualisation/26805788/embed"
        title="Negativity levels during peaks by subreddit category"
        class="flourish-embed-iframe"
        frameborder="0"
        scrolling="no"
        style="width:100%;height:600px;"
        sandbox="allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation">
</iframe>
</div>
</div>

<div class="col-12 col-lg-5">
<div class="card p-4 shadow-sm h-100">
<h4>Negativity patterns during peaks</h4>

<ul>
<li><strong>Original sources</strong> dominate negativity levels during peaks, supporting Hypothesis&nbsp;1.</li>
<li><strong>Recurrent neighbors</strong> exhibit negativity levels comparable to sources, and clearly higher than unrelated subreddits.</li>
</ul>

<p>
These patterns indicate that negativity peaks are not purely global or random phenomena.
Instead, they are strongly shaped by the <strong>local structure of the interaction network</strong>,
with direct exposure to negative sources playing a key role in amplifying hostility.
</p>
</div>
</div>

</div>
</section>




## Are Neighbors More Affected Than Others? Statistical Evidence
To move beyond descriptive patterns, we formally test whether neighbors experience a larger increase in negativity during peaks compared to other subreddits.

In other words: are neighbors more affected by wave than others? Or are they just more negative on average 
method : Stat test across peaks to see if neighbors have significantly higher increase in negativity during peaks wrt others

[Visualisaiton ? ]
> tagged_in neighbors clearly exhibit increased negativity relative to others during waves



<section class="container my-4">
  <div class="row justify-content-center">
    <div class="col-12 col-md-10 col-lg-10">
      <div class="card shadow-sm">
        <div class="card-body">
          <h4 class="card-title mb-2">Overall conclusions on peaks analysis</h4>
          <ul class="card-text mb-3">
            <li>Negativity peaks represent critical moments in Reddit’s interaction dynamics.</li>
            <li>Peaks are source-driven, not random.</li>
            <li>Direct neighbors of negative sources are significantly more affected than other communities.</li>
            <li>The observed patterns provide strong evidence of network-based contagion.</li>
          </ul>
          <p class="card-text mb-0">
            These insights naturally connect to Part 3, where we examine how such dynamics interact with real-world events and whether future negativity waves can be predicted.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>




