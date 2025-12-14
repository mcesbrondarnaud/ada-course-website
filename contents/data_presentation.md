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






