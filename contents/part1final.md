# Part 1 - The big picture on negativity, main flows across subreddits
This section investigates the flow of negativity between different clusters, aiming to identify which subreddits are the primary sources of negative interactions and how negativity propagates across Reddit. By studying the flow, we can identify whether certain communities act as "gateways" for negativity, redirecting hostility to other subreddits, or if some communities accumulate negativity.


## Incoming vs. outgoing negativity: Who produces, who absorbs?
We first compare, for each high-level cluster, the amount of negative links sent versus negative links received.

<section class="container my-5">
<div class="row g-4 align-items-start">

<div class="col-12 col-lg-7">
<div class="card p-3">
<iframe src="https://flo.uri.sh/visualisation/26649034/embed"
        title="Incoming vs outgoing negativity by cluster"
        class="flourish-embed-iframe"
        frameborder="0"
        scrolling="no"
        style="width:100%;height:600px;"
        sandbox="allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation">
</iframe>
</div>
</div>

<div class="col-12 col-lg-5">
<div class="card p-4 shadow-sm h-100">
<h4>Asymmetry in negativity flows</h4>

<ul>
<li>Some clusters clearly act as <strong>net exporters of negativity</strong>, generating far more negative references than they receive.</li>
<li>Other clusters behave as <strong>net sinks</strong>, receiving negativity from many different sources while contributing little themselves.</li>
</ul>

<p>
This asymmetry indicates that negativity does not circulate randomly across Reddit.
Instead, it follows <strong>structured, directional patterns</strong>, driven by a limited number
of communities that play a disproportionate role in propagating hostile interactions.
</p>
</div>
</div>

</div>
</section>


## Who sends negativity to whom? Inter-cluster flows
To analyze the flow of negativity, we used a chord diagram to visualize the connections between clusters, where:
- Each node represents a cluster,
- Each chord represents negative links sent from one cluster to another,
- The thickness of the chord encodes the volume of negativity exchanged.

<section class="container my-5">
<div class="row g-4 align-items-start">

<div class="col-12 col-lg-7">
<div class="card p-3">
<iframe src="https://flo.uri.sh/visualisation/26513009/embed"
        style="width:100%;height:600px;"
        frameborder="0"
        scrolling="no"></iframe>
</div>
</div>

<div class="col-12 col-lg-5">
<div class="card p-4 shadow-sm h-100">
<h4>Inter-cluster negativity patterns</h4>
<ul>
<li>Negativity is not confined within clusters: inter-cluster hostility is substantial.</li>
<li>Political and ideologically oriented clusters tend to export negativity broadly.</li>
<li>Some clusters are repeatedly targeted, reinforcing their role as accumulators of hostility.</li>
</ul>
<p>
This confirms that negativity behaves as a networked phenomenon, flowing across thematic
boundaries rather than remaining local.
</p>
</div>
</div>

</div>
</section>





## ratio 
<iframe src='https://flo.uri.sh/visualisation/26805661/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

## Top contributors: a small number of actors drive most negativity
We now zoom in on the most influential subreddits by tracking the evolution of the top 5 contributors to negative outlinks over time.

<section class="container my-5">
<div class="row g-4 align-items-start">

<div class="col-12 col-lg-7">
<div class="card p-3">
<iframe src="https://public.flourish.studio/visualisation/26553662/embed"
        title="Top contributors to negative links over time"
        frameborder="0"
        allowfullscreen
        style="width:100%;height:600px;">
</iframe>
</div>
</div>

<div class="col-12 col-lg-5">
<div class="card p-4 shadow-sm h-100">
<h4>Concentration and temporal persistence</h4>

<ul>
<li>A very small number of subreddits consistently dominate the production of negative links.</li>
<li>Despite fluctuations in ranking, the same communities repeatedly reappear at the top.</li>
</ul>

<p>
This pattern reveals a strong <strong>concentration effect</strong> and suggests
<strong>temporal persistence</strong> in the sources of negativity.
Rather than rotating randomly across communities, negativity is repeatedly driven
by a limited set of influential actors — a phenomenon we examine more formally
in the next part of the analysis.
</p>
</div>
</div>

</div>
</section>


## Concentration of Negativity: Ratios vs. Counts
[graph notebook marzio]


## Ratio
[graph notebook marzio]

Results from our analysis show that:
- The top 50 subreddits alone account for roughly 50% of all negative links.
- This extreme concentration confirms that negativity is driven by a small minority of highly influential actors.

This finding directly connects to Part 2 (Dynamics), where we investigate whether these same actors also dominate negativity peaks over time, and whether their behavior helps explain waves of hostility across Reddit.





<div style="margin:2rem 0;"></div>

<section class="container my-5">
<div class="row justify-content-center">
<div class="col-12 col-lg-10">
<div class="card shadow-sm">
<div class="card-body p-4 p-md-5">

<h4 class="card-title mb-3">Overall conclusions on negativity</h4>

<ul class="mb-4">
<li>Negativity flows across Reddit in a highly structured and directional way.</li>
<li>Certain clusters act as sources, others as sinks, and some as gateways that redirect hostility.</li>
<li>Inter-cluster hostility is substantial, showing that negativity easily crosses thematic boundaries.</li>
<li>A small fraction of subreddits is responsible for a disproportionate share of negative interactions.</li>
</ul>

<p class="mb-0">
Together, these results reinforce a central message of our project:
<strong>
online negativity is not diffuse or random — it is concentrated, directional,
and driven by a small set of influential communities.
</strong>
</p>

</div>
</div>
</div>
</div>
</section>




