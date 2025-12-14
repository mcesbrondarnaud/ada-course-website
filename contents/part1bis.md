# Part 1 : Cluster-level negativity

To analyze the behavior of negativity across Reddit, we first needed to group subreddits based on their semantic content. This helps us identify communities with similar thematic interests, which may exhibit different levels of hostility. 
The primary goal of this step was to explore how subreddits cluster into groups and whether certain clusters (e.g., political subreddits) are more likely to generate negative interactions.

## Clustering subreddits
- UMAP Scatterplot => Show how subreddits cluster based on embeddings (visualized on UMAP).
- Cluster Sizes => Show a bubble chart or bar plot with the size of each cluster (e.g., number of subreddits in each thematic group).

## High-level cluster characterization 
- [Plot distribution of high level clusters]
- [PLot histogram of total interactions per cluster subreddit (as sum of each subreddit in cluster)]


## Which are most negative ? where are main flows ? 
- Main distribution of negativity across clusters 
- Study flows between clusters (chord diagram)
- plot correlation heatmap of negative ratios between high level clusters
- extra cluster negative links


## Monthly negativity trends per clusters : who sends more negativity over time ? 
- Monthly negativity / ratio per cluster => Plot graph of monthly negativity ratios for all high level clusters from monthly_matrix_all
- Top subreddits => who focuses negativity ? table : Subreddits responsible for 50% of negative outlinks
- more detailed analysis of top 5 negative and their evolution monthly => graph


<div class="flourish-embed flourish-bar-chart-race" data-src="visualisation/26553662">
  <script src="https://public.flourish.studio/resources/embed.js"></script>
  <noscript>
    <img src="https://public.flourish.studio/visualisation/26553662/thumbnail" width="100%" alt="bar-chart-race visualization" />
  </noscript>
</div>

