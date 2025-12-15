Our core data consists of two complementary datasets of inter-subreddit hyperlinks, representing references made by users from one subreddit to another:
- Title hyperlinks dataset: links appearing in post titles
- Body hyperlinks dataset: links embedded in the body of posts

These two sources capture different interaction mechanisms: titles often reflect explicit framing or confrontation, while body links tend to arise from more contextual or argumentative references.

Each hyperlink record contains the following information:
- `SOURCE_SUBREDDIT` : Subreddit where the post originates
- `TARGET_SUBREDDIT` : Subreddit referenced by the link
- `POST_ID` : Unique identifier of the post
- `TIMESTAMP` : Time of posting
- `LINK_SENTIMENT` : Sentiment label (-1 = negative, 1 = neutral or positive)
- `POST_PROPERTIES` : Vector of text-derived numerical features

This structure enables us to analyze who interacts with whom, when, and with what sentiment, forming the backbone of our network analysis.

## Subreddit Embeddings and Semantic Structure
To move beyond individual interactions and capture thematic similarity between communities, we also use a dataset of subreddit embeddings.
Each subreddit is represented by a 300-dimensional vector encoding its semantic position in topic space.

These embeddings allow us to:
- group subreddits into coherent thematic clusters (e.g. politics, gaming, sports),
- measure topical proximity between communities,
- and study whether negativity follows semantic boundaries.
To visualize this high-dimensional structure, we apply dimensionality reduction techniques such as PCA and t-SNE, revealing clear cluster separation in a low-dimensional space.

<iframe src='https://flo.uri.sh/visualisation/26634242/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:80%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

This projection already suggests that Reddit communities are not randomly distributed, but organized around well-defined thematic regions.

<section class="container my-4">
<div class="row justify-content-center">
<div class="col-12 col-lg-10">
<div class="card shadow-sm">
<div class="card-body p-4">

<h5 class="mb-2">Key insight</h5>

<p class="mb-0">
This projection already suggests that Reddit communities are
<strong>not randomly distributed</strong>,
but instead organized around
<strong>well-defined thematic regions</strong>.
</p>

</div>
</div>
</div>
</div>
</section>


## Cluster Sizes and Representation
Once clusters are identified, we examine their relative sizes, measured by the number of subreddits they contain. This step is important to distinguish between large, dominant thematic areas and more niche communities.

<iframe src='https://flo.uri.sh/visualisation/26558499/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

This distribution highlights strong imbalances across themes, which later proves crucial when interpreting negativity levels and flows: large clusters naturally generate more interactions, but not necessarily more hostility.

<section class="container my-4">
<div class="row justify-content-center">
<div class="col-12 col-lg-10">
<div class="card shadow-sm">
<div class="card-body p-4">

<h5 class="mb-2">Key insight</h5>

<p class="mb-0">
This distribution highlights strong imbalances across themes, which later proves crucial
when interpreting negativity levels and flows.
<strong>
Large clusters naturally generate more interactions, but not necessarily more hostility.
</strong>
</p>

</div>
</div>
</div>
</div>
</section>



## External Context: GDELT Dataset

Finally, to place Reddit dynamics within a broader real-world context, we incorporate data from the Global Database of Events, Language, and Tone (GDELT).
This dataset is aggregated daily by world region (Europe, Asia, Africa, North America, South America, Oceania) between 2014 and 2017.

It summarizes global media activity through indicators such as:
- total number of events,
- number of media mentions,
- average event tone,
- protest and conflict-related counts.

By combining GDELT with Reddit time series, we can explore whether spikes of online negativity coincide with periods of heightened real-world tension or media attention.


