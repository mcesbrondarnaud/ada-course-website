# III. 🚨 When Negativity Spikes: Detecting Attacks and First Movers

Not every negative comment is an attack. We identify negativity surges — sudden spikes in hostile links targeting a community within a short time window. These moments mark when a subreddit shifts from casual disagreement to coordinated pressure.

This allows us to:
- Separate background noise from real attacks
- Measure attack intensity and duration
- Compare how often different communities are targeted
- Knowing when you’re under attack is the first step to responding effectively.

### 1. Waves of negativity
Negativity fluctuates; there is always some, but you can probably brush it off when it’s just a few negative comments. However there are peaks during which it can become overwhelming. Here we study the main peaks of negativity and the waves they come in. If we learn what these waves are, we can learn to avoid them.

[Fig 2.1 Peaks of negativity]
[Peaks of negativity](/ada-course-website/contents/graphA.html).

For each peak, we ask: Who acted first? By tracing interactions backward in time, we identify: 
- Original sources that initiate negative interactions,
- Their neighbors
- Others that interact during window

This allows us to separate attack origins from communities that are merely caught in the fallout. Let’s see how the negativity of these groups evolves during peaks.

[Fig 2.2 Neg ratio of groups during peaks]
<iframe src='https://flo.uri.sh/visualisation/26805788/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

We observe that sources have much higher negativity ratios. Interestingly, their neighbors also have a statistically significant gap with others.
But is this just because, as we have seen, some subreddits are generally more negative than others? Or is it because of their interaction with sources?

### 2. Who Gets Pulled In: Sources, Neighbors, Bystanders 
To refine our analysis, we cluster sources and neighbors to identify most recurrent neighbors and most connected sources. First, let’s see where the negativity is during waves:

[Fig 2.3 Bars of negative interactions bt groups]

Neighbor/sources interactions do dominate (vs others)

Are these sources/neighbors random?

[Fig 2.4 Contact map of peaks and neighbor/source similarity]

Comparing the similarity for top sources/neighbors, we see that most peaks share at least 50% of the same, suggesting recurring action from same actors.

¿HERE OR NEXT SECTION?
We can visualize this nicely looking at negativity ratio evolution of each subreddit:

[Fig 2.5? tSNE with neg ratios]
<iframe src="https://flo.uri.sh/visualisation/26634242/embed" title="PCA / t-SNE projection" class="flourish-embed-iframe" frameborder="0" scrolling="no" style="width:80%;height:600px;" sandbox="allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation"> </iframe>
The sources + neighbors appear to be spatially close, and negativity evolution supports our observation of echochambers.


¿NEW SECTION OR JUST 3. ?
