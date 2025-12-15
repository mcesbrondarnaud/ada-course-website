# Part 2 - dynamics 

## identifying statistically significant peaks (3.a.2)

To understand how negativity spreads across time, we first track the overall evolution of negative links across Reddit. This allows us to visualize waves of negativity — periods where hostility increases significantly. We then break this evolution into weekly bins to better understand the temporal spread of negativity. 
After identifying the overall evolution of negativity, we now focus on identifying significant peaks of hostility. These peaks indicate when negative interactions reached their highest levels, often tied to specific events or discussions on Reddit.

We examined the negativity ratio (the proportion of negative links relative to total links) over time and identified the most significant peaks in the data. By identifying these peaks, we can focus on the periods when negativity was at its highest.

[notebook]



##
Now we want to understand negativity during peaks : main actors, sources, spreading to neighbours
- Hypothesis 1: there are subreddit sources of negativity that trigger peaks
- Hypothesis 2: neighbors of sources are more negative during peaks (contagion)
- Hypothesis 3: neighbors directly exposed to sources are more negative during peaks and have higher increase than others (contagion)


## voir si neighbours réagissent plus que les autres 


<section class="container my-5">
  <div class="row align-items-start g-4">

    <!-- Graphe (Flourish) -->
    <div class="col-12 col-lg-7">
      <div class="card p-3">
        <iframe
          src="https://flo.uri.sh/visualisation/26805788/embed"
          title="Interactive or visual content"
          class="flourish-embed-iframe"
          frameborder="0"
          scrolling="no"
          style="width:100%;height:600px;"
          sandbox="allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation">
        </iframe>
      </div>
    </div>

    <!-- Explication -->
    <div class="col-12 col-lg-5">
      <h3 class="mb-3">Key takeaway</h3>
      <p class="mb-0">
        Original sources dominate negativity, others &amp; tagged_in neighbors are similar,
        but neighbors seem slightly higher.
      </p>
    </div>

  </div>
</section>



<iframe src='https://flo.uri.sh/visualisation/26805788/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

> Original sources dominate negativity, others & tagged_in neighbors are similar but neighbors seem slightly higher



## Let's see if there is evidence of increase of neighbors negativity during slices (wrt to change in others' negativity)

In other words: are neighbors more affected by wave than others? Or are they just more negative on average 
method : Stat test across peaks to see if neighbors have significantly higher increase in negativity during peaks wrt others

[Visualisaiton ? ]
> tagged_in neighbors clearly exhibit increased negativity relative to others during waves


### **Overall conclusions on peaks analysis:** 

<section class="container my-4">
  <div class="row justify-content-center">
    <div class="col-12 col-md-8 col-lg-6">
      <div class="card shadow-sm">
        <div class="card-body">
          <h4 class="card-title mb-2">À retenir</h4>
          <p class="card-text mb-0">
            - neighbors + sources have higher negativity during peaks wrt to othershat do not interact with sources
            - tagged_in neighbors have significantly higher increase in negativity during peaks wrt to others
            - targeting neighbors are mostly inactive during peaks and mask the effect if included
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

- neighbors + sources have higher negativity during peaks wrt to othershat do not interact with sources
- tagged_in neighbors have significantly higher increase in negativity during peaks wrt to others
- targeting neighbors are mostly inactive during peaks and mask the effect if included




