## Explain the dataset 

We use two complementary datasets of Reddit hyperlinks, each representing inter-subreddit references made by users:
- Title hyperlinks dataset: references contained in post titles.  
- Body hyperlinks dataset: references contained in post bodies.

Each sample contains the following parameters:
- `SOURCE_SUBREDDIT` : Subreddit where the post originates
- `TARGET_SUBREDDIT` : Subreddit referenced by the link
- `POST_ID` : Unique identifier of the post
- `TIMESTAMP` : Time of posting
- `LINK_SENTIMENT` : Sentiment label (-1 = negative, 1 = neutral or positive)
- `POST_PROPERTIES` : Vector of text-derived numerical features

Additionally, we use a subreddit embeddings dataset containing:
- `name`: subreddit name
- 300-dimensional vector embedding representing its semantic position in topic space.
These embeddings allow us to group subreddits into coherent clusters (politics, gaming, sports) and measure topical similarity.

Besides, we include the Global Database of Events (GDELT), aggregated daily by world region (Europe, Asia, Africa, North America, South America, Oceania) between 2014 and 2017. It summarizes global activity, media attention, and event tone through indicators such as total events, mentions, average Goldstein score, and protest counts.
This dataset provides a macro-level context to compare Reddit’s temporal negativity dynamics with external global events, enabling exploratory correlation analyses.



## Computing basic statistics and label distribution

# Top 10 attacking and attacked subreddits
Let's start by selecting data with negative sentiment in hyperlinks df, and extract attackers (sources of negative sentiment) and attacked (targets of negative sentiment)

[Table of the top 10 attacking subreddits]
[Table of the top 10 attacked subreddits]

Notes on the table : We observe that `subredditdrama` is responsible for > 10% of negative edges ! Moreover, top 10 attackers represent 27,5% of attacks.
On the other side, the top 10 of victims is more evenly distributed, and represent approximately 18,4% of the attacked.


# Interraction between the top subreddits
Now, let's visualize the interraction between the top subreddits. We will take ony the top 5 attackers and top 5 victims for clarity.

[Subreddit hyperlink network (Red = Negative, Green = positive/ neutral)]




# Estimate negativity ration per subreddit
We compute the negativity ratio r_minus [r_minus = negative / (positive + negative)], which measures the fraction of a subreddit’s outgoing links that are negative.

[table ? => Distribution of subreddit negativity ratios (below lorenz curve in document]

Note on the graph : The log scale on the y axis shows that the huge majority of subreddits have `r_neg=0`. This again emphasizes the fact that negativity is concentrated among few subreddits. 


# Computing inequality metrics (Gini Coeff and Lorenz curve)
We compute the negativity fraction `r_neg=n_neglinks+n_totlinks` for each subreddit, to then calculate the Gini coefficient. If this coeff is close to one, this means that negativity is focused on only few subreddits. If not, then the negativity is evenly distributed. 

[Give gini coef and plot lorenz curve]
Global Gini = 0.953 → Negativity is highly concentrated among a few subreddits, Here, it is close to 1 so we can assume that reddits' negativity is only due to certain number of subs, and that it isn't global.
The Lorentz curve calculated using the cumulative `r_neg` (/src/utils/stats.py), deviates from the identity, thus showing again the "not global" characteristic of negativity.


# Correlation among subreddit activity metrics 

[Correlation matrix]






