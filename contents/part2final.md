# Part 2 - dynamics 

While the previous section highlighted where negativity is concentrated on Reddit and how it flows between communities, it did not yet explain when negativity becomes most intense. In practice, hostility on Reddit does not remain constant over time. Instead, it tends to rise and fall in waves, with short periods during which negative interactions sharply intensify.

Understanding these temporal dynamics is essential. Peaks of negativity are precisely the moments when online discourse becomes most polarized, most visible, and potentially most influential. They may reflect reactions to external events, internal platform dynamics, or the activity of a small number of highly influential communities.


## Identifying statistically significant peaks (3.a.2)

To understand how negativity spreads across time, we first track the overall evolution of negative links across Reddit. This allows us to visualize waves of negativity — periods where hostility increases significantly. We then break this evolution into weekly bins to better understand the temporal spread of negativity. 
After identifying the overall evolution of negativity, we now focus on identifying significant peaks of hostility. These peaks indicate when negative interactions reached their highest levels, often tied to specific events or discussions on Reddit.

We examined the negativity ratio (the proportion of negative links relative to total links) over time and identified the most significant peaks in the data. By identifying these peaks, we can focus on the periods when negativity was at its highest.

[notebook + commentaires]



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

<iframe src='https://flo.uri.sh/visualisation/26805788/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

Several clear patterns emerge:
- Original sources dominate negativity levels during peaks, confirming Hypothesis 1.
- Recurrent neighbors exhibit negativity levels comparable to sources, and clearly higher than unrelated subreddits.
This already provides qualitative evidence that peaks are not purely global phenomena, but are shaped by local network structure.



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




