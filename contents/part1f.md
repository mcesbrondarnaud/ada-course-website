# I. 🧭 Know Your Surroundings: What Kind of Neighborhood Are You In?

Defense starts with situational awareness: before defending yourself, you need context. Some subreddits are isolated villages. Others sit on busy crossroads where negativity travels fast.
So to start we need to get to know our surroundings: how are communities shaped? And where are the main channels where negativity travels?
### 1. Clustering: getting to know your neighbors
Luckily we already have a dataset of embeddings, which translate main thematics of subreddits into a mathematical space. Through this, by exploring the similarity between these vectors, we can reconstruct communities of subreddits.

[Fig 1.1 Clustering]
<iframe src='https://flo.uri.sh/visualisation/26887294/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:70%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

Alright! This colorful map shows the high diversity of the reddit landscape; some clusters are small and tightly packed, with specific themes, whereas others spread across wider topics. To avoid getting lost in this high variety of communities, we have grouped them into a smaller number of higher-level clusters, which will shape our exploration.

[Fig 1.2 Clusters & HLC doghnut] 
<iframe src='https://flo.uri.sh/visualisation/26558499/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:70%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

3 main communities pop-out: one ‘Informative’ a bit mixed, and two more focused (‘Gaming’ and Politics’. 
These categories will help us track where negativity concentrates.

### 2. Negativity: The big picture
Now we’ve identified main communities, let’s focus on negativity. Negativity is characterised by links of negative sentiment being sent from one source subreddit to one target subreddit.
First, let’s identify the highways of negativity: where can we find the main flows of negative sentiment?

[Fig 1.3 Intra/extra pie charts]
<iframe src='https://flo.uri.sh/visualisation/26649034/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:70%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

We can see that some clusters tend to keep their conflicts at home. It is especially the case for Sports, Gaming and Technology. We can speculate that these specific thematic clusters have internal disagreements about shared topics. On the other hand, some clusters tend to be more aggressive and distribute negativity outwards.
Let’s try and characterize these main flows between different clusters:

[Fig 1.4 Extra-cluster flows]
Here we can already identify main routes of animosity between clusters. We can notice two main sources who tend to be more negative in general: Politics and Informative.

But is it always the case?
Of course, negativity is not a fixed quantity. It evolves dynamically; as a result, we can track its evolution across the duration of our dataset. 

[Fig 1.5 Cluster evolution]

Despite fluctuations, this confirms that Politics and Informative remain top actors throughout.

Can we find, in a similar way, the top actors? That is - individual subreddits that consistently output high negativity?

[Fig 1.6 Top 5 evolution]
<iframe src='https://flo.uri.sh/visualisation/26553662/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:70%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

Now we have an idea of how our surroundings and their negativity are shaped, we can deep-dive into studying when negativity becomes overwhelming.
