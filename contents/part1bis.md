# Part 1 : Cluster-level negativity

To analyze the behavior of negativity across Reddit, we first needed to group subreddits based on their semantic content. This helps us identify communities with similar thematic interests, which may exhibit different levels of hostility. 
The primary goal of this step was to explore how subreddits cluster into groups and whether certain clusters (e.g., political subreddits) are more likely to generate negative interactions.

## Clustering subreddits
In order to reduce the high-dimensional embedding vectors of subreddits into two dimensions we used UMAP (Uniform Manifold Approximation and Projection). This allowed us to visualize the semantic relationships between them.

[Cluster's map]
> The UMAP scatterplot shows that subreddits naturally form clusters based on their thematic focus. [Give example ?]

[Bubble chart]
> We can also visualize the size of each thematic group. This allows us to determine the size of the largest clusters for example.


## High-level cluster characterization
After clustering subreddits, we explored their characteristics by analyzing how negative interactions are distributed across these clusters. This section aims to understand the extent of negativity within each cluster and how much engagement occurs within each group.

We aggregated the total interactions within each high-level cluster by summing the number of negative references (outgoing negative links). This allowed us to visualize the total level of hostility within each cluster, as well as the distribution of negative interactions among subreddits.

- [Plot distribution of high level clusters]
- [PLot histogram of total interactions per cluster subreddit (as sum of each subreddit in cluster)]


## Which are most negative ? where are main flows ? 
This section investigates the flow of negativity between different clusters, aiming to identify which subreddits are the primary sources of negative interactions and how negativity propagates across Reddit. By studying the flow, we can identify whether certain communities act as "gateways" for negativity, redirecting hostility to other subreddits, or if some communities accumulate negativity.

- [Main distribution of negativity across clusters ]

To analyze the flow of negativity, we used a chord diagram to visualize the connections between clusters. The thickness of the chords represents the amount of negative interaction flowing from one cluster to another. 
- [Study flows between clusters (chord diagram)]

Additionally, we created a correlation heatmap to measure the relationships between negative ratios in high-level clusters. This helped us identify patterns of contagion: do spikes in one cluster (e.g., political discussions) lead to spikes in others?
- [plot correlation heatmap of negative ratios between high level clusters]

En plus :
- [extra cluster negative links]


## Monthly negativity trends per clusters : who sends more negativity over time ? 
This section explores how negativity evolves over time within each cluster. 
By examining monthly trends, we can identify which subreddits contribute the most negativity over time and track how top negative subreddits evolve.

We analyzed the monthly negativity ratios for all high-level clusters, using a time series to capture fluctuations over the course of several months. 

- [Monthly negativity / ratio per cluster => Plot graph of monthly negativity ratios for all high level clusters from monthly_matrix_all]

Additionally, we identified the top subreddits responsible for the highest amount of negativity and explored how their negative behavior evolves monthly.
- [Top subreddits => who focuses negativity ? table : Subreddits responsible for 50% of negative outlinks]
- [more detailed analysis of top 5 negative and their evolution monthly => graph]

now works ? 
<iframe width="100%" height="600" src="https://public.flourish.studio/visualisation/26553662/embed" frameborder="0" allowfullscreen></iframe>

<div class="flourish-embed flourish-bar-chart-race" data-src="visualisation/26553662">
    <script src="https://public.flourish.studio/resources/embed.js"></script>
    <noscript>
        <img src="https://public.flourish.studio/visualisation/26553662/thumbnail" width="100%" alt="bar-chart-race visualization" />
    </noscript>
</div>
 ---

