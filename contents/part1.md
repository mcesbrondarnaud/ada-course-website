## Origins and Concentration of negativity 
## Part 1 - Cluster Landscape : Understanding the thematic structure of Reddit

Before analyzing negativity, we must first understand the thematic structure of Reddit. Subreddits form communities organized around topics such as politics, gaming, entertainment, or technology.
By mapping these communities, we build the foundation needed to interpret where negativity originates and how it spreads.

Reddit is not a uniform space. Subreddits naturally group into thematic clusters, and these clusters influence behavior.
Negativity is unlikely to be random — instead, it tends to emerge from and propagate through specific topical communities.

Understanding this structure helps us answer:
- Which subreddits are the primary sources of negative references?
- Are certain thematic clusters (political, cultural, entertainment etc...) more prone to initiate hostility?
- Is negativity evenly distributed or concentrated in a few communities?
- Can we quantify this inequality (using a Gini coefficient)?



## Which subreddits are the primary sources of negative references? Are certain thematic clusters (political, cultural, entertainment etc...) more prone to initiate hostility?

# Top 10 attacking and attacked subreddits
Let's start by selecting data with negative sentiment in hyperlinks df, and extract attackers (sources of negative sentiment) and attacked (targets of negative sentiment)

[Table of the top 10 attacking subreddits]
[Table of the top 10 attacked subreddits]

Notes on the table : 
> We observe that `subredditdrama` is responsible for > 10% of negative edges ! Moreover, top 10 attackers represent 27,5% of attacks.
> On the other side, the top 10 of victims is more evenly distributed, and represent approximately 18,4% of the attacked.


# Interraction between the top subreddits
Now, let's visualize the interraction between the top subreddits. We will take ony the top 5 attackers and top 5 victims for clarity.

[Subreddit hyperlink network (Red = Negative, Green = positive/ neutral)]




## Is negativity evenly distributed or concentrated in a few communities? Can we quantify this inequality (using a Gini coefficient)?

# Estimate negativity ration per subreddit
We compute the negativity ratio r_minus [r_minus = negative / (positive + negative)], which measures the fraction of a subreddit’s outgoing links that are negative.

[table ? => Distribution of subreddit negativity ratios (below lorenz curve in document]

Note on the graph : 
> The log scale on the y axis shows that the huge majority of subreddits have `r_neg=0`. This again emphasizes the fact that negativity is concentrated among few subreddits. 

# Computing inequality metrics (Gini Coeff and Lorenz curve)
We compute the negativity fraction `r_neg=n_neglinks+n_totlinks` for each subreddit, to then calculate the Gini coefficient. If this coeff is close to one, this means that negativity is focused on only few subreddits. If not, then the negativity is evenly distributed. 

[Give gini coef and plot lorenz curve]
Notes on this : 
> Global Gini = 0.953 → Negativity is highly concentrated among a few subreddits, Here, it is close to 1 so we can assume that reddits' negativity is only due to certain number of subs, and that it isn't global.
> The Lorentz curve calculated using the cumulative `r_neg` (/src/utils/stats.py), deviates from the identity, thus showing again the "not global" characteristic of negativity.


# Correlation among subreddit activity metrics 

[Correlation matrix]
