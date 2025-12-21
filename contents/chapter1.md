# Chapter I: The Map of the Realm
*"Standard maps won't work here,"* the analyst continues, dimming the lights. *"Reddit isn't a list of websites. It is a galaxy."*

To understand the battlefield, the ADAvengers used **Embeddings** to project every subreddit onto a 2D map based on user overlap. Communities that share users are pulled close together; enemies or strangers are pushed apart.

For each local region, clusters are extracted automatically using a k-nearest neighbors approach. These low-level clusters are then grouped into broad domains.
<section class="container my-5">
  <div class="row g-4 align-items-start">

    <!-- CHART -->
    <div class="col-12 col-lg-7">
      <div class="card p-3">
        <div class="text-center">
          <iframe
            src="https://flo.uri.sh/visualisation/26887294/embed"
            title="Reddit map of subreddits"
            class="flourish-embed-iframe"
            frameborder="0"
            scrolling="no"
            style="width:70%;height:600px;"
            sandbox="allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation">
          </iframe>
        </div>
      </div>
    </div>

    <!-- INSIGHTS BOX -->
    <div class="col-12 col-lg-5">
      <div class="card p-4 shadow-sm h-100">
        <h4 class="mb-3">The Analysis</h4>
        <p class="mb-3">
          This is the satellite view of Reddit. You can clearly see the “continents” forming:
        </p>
        <ul class="mb-0">
          <li><strong>The Gaming Archipelago:</strong> a massive, dense cluster of interconnected games.</li>
          <li><strong>The Political Front:</strong> highly active, often isolated from the more casual zones.</li>
          <li><strong>The Neutral Zones:</strong> hobby and lifestyle communities floating on the periphery.</li>
        </ul>
      </div>
    </div>

  </div>
</section>


(Insert Fig 1.1: Reddit Embeddings Map)
<iframe src='https://flo.uri.sh/visualisation/26887294/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:70%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

**The Analysis:** This is the satellite view of Reddit. You can clearly see the "Continents" forming:
- **The Gaming Archipelago:** A massive, dense cluster of interconnected games.
- **The Political Front:** Highly active, often isolated from the more casual zones.
- **The Neutral Zones:** Hobby and Lifestyle communities floating on the periphery.

This structure reveals an important nuance: the most thematically precise communities tend to form **isolated islands**, while broader themes occupy the middle ground, bridging multiple regions.
*"But a satellite view is too messy for strategy," Lisa argues. "I need to know the chain of command."
"Then look at the Hierarchy,"* the analyst replies.

<iframe src='https://flo.uri.sh/visualisation/26558499/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:70%;height:600px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>

**The Insight:** This visualization organizes the chaos into clear administrative districts. The size of each circle represents the volume of posts. We can instantly see the weight of the Informative, Politics, and Sports clusters compared to smaller niches. This is the board upon which the game is played.
