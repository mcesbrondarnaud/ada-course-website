## V. External Shocks: Are World Events Driving the Waves?

Avant même de blâmer les communautés directement et de les catégoriser comme toxiques, il y a une question importante à soulever :  
**les pics de négativité observés sur Reddit sont-ils une simple réponse aux événements mondiaux ?**

Si cette hypothèse est vérifiée, alors vous saurez que lorsque les news mondiales sont négatives, il y a de fortes chances que certaines communautés Reddit le soient aussi, et qu’il suffit donc de les éviter pendant ces périodes.

Before blaming communities alone, we test a key confounder:  
**What if negativity peaks are driven by world events instead?**

---

### Part 4: External Shocks – Is the World Driving the Anger?

#### The Hook: The “Mirror” Hypothesis

We often assume Reddit is a mirror of the real world:  
*when the news bleeds, the internet fights.*

But is that actually true?  
Or is Reddit just a collection of sealed bunkers that only open their doors for specific kinds of doom?

To find out, we pitted **GDELT (The Global News Pulse)** against **Reddit (The Social Pulse)**, looking for *shockwaves* — moments where a massive media spike was followed immediately (or within one week) by a Reddit hostility spike.

---

## 1. The Investigation: A Tale of Three Realities

Our matrix analysis revealed that Reddit doesn’t just react to everything.  
It filters the world through distinct behaviors — some logical, some totally bizarre.

---

### (A) The True Mirror (Hypothesis Validated)

- **The suspects:** Politics & Informative clusters  
- **The trigger:** Terrorism & Social Protests  
- **The verdict:** ✅ **SYNCED**

When the world shakes, these communities shake.

**Evidence:**  
The data shows clear causal matches during major crises like:
- the Paris Attacks (November 2015),
- the Trump Election (November 2016).

The hostility here isn’t random; it’s a direct downstream consequence of global chaos.

---

### (B) The “Porous Silo” (The Leak)

- **The suspect:** Gaming cluster vs. US_Election_16  
- **The verdict:** ⚠️ **UNEXPECTED LEAK**

We expected gamers to ignore the election.  
Instead, we observed a **64% match rate**.

This was not about tax policy. It was about the *culture war*.  
In 2016, political discourse breached the walls of the gaming sanctuary, proving that even escapist bunkers have cracks when polarization becomes a cultural identity.

---

### (C) The “Parallel Universe” (The False Coincidence)

- **The suspect:** Gaming vs. Social Protest  
- **The verdict:** ❌ **FALSE POSITIVE**

**The data:**  
Both time series spike perfectly in late 2015.

**The reality:**  
- The world was protesting climate change (COP21).  
- Gamers were protesting Konami for banning Hideo Kojima from The Game Awards.

**Lesson:**  
The algorithm sees a match, but context reveals two different worlds screaming at different clouds.

---

### (D) The “Dark Mirror” (The Semantic Accident)

- **The suspect:** AdultContent vs. Terrorism  
- **The verdict:** ⚠️ **SEMANTIC CONFUSION**

**The data:**  
A spooky synchronization occurs on November 22, 2015.

**The reality:**  
- The world locked down due to the Brussels terror threat.  
- The Adult community reacted to Jared Fogle (Subway) being sentenced.

**Lesson:**  
GDELT saw *crime* and *horror*. Reddit saw *crime* and *horror*.  
But the subjects were worlds apart.

---

## 2. The Reality Check: Trusting the p-values

Visuals can be persuasive — and misleading — so we brought in statistical testing using **Student’s t-test**, comparing mean hostility during *peace* versus *media shockwaves*.

---

### ✅ The “Significance” Zone (p < 0.05)

- **TERRORISM → Politics (p = 0.043)**  
  Confirmed. Hostility in r/politics is genuinely different when terror events occur.

- **SOCIAL_PROTEST → Informative (p = 0.028)**  
  Confirmed. News and learning communities reliably react to civil unrest.

- **US_ELECTION → AdultContent (p = 0.021)**  
  Statistically significant, but conceptually suspicious.  
  Interpreted as a **false causal link**, likely due to semantic overlap.

---

### ⚠️ The “Saturation” Zone (Borderline)

- **SOCIAL_PROTEST → Politics (p = 0.087)**  

Surprisingly weak effect.  
Explanation: **saturation**. r/politics is already highly negative, making marginal shocks harder to detect.

> *It’s hard to hear a scream in a room where everyone is already shouting.*

---

### ❌ The “Bunker” Zone (p > 0.10)

- **ARMED_CONFLICT → Lifestyle (p = 0.15)**  
  Lifestyle communities successfully ignore armed conflicts.

- **US_ELECTION → Entertainment (p = 0.27)**  
  Entertainment communities barely react to political shocks.

*(Note: Geography reacted massively to protests (p = 0.000015) but was excluded from the main analysis due to low link volume. It serves as a theoretical baseline.)*

---

## 3. Conclusion: The Verdict

**Does the world drive Reddit’s anger? Yes — but only if the door is unlocked.**

- **Politics & Informative** → open doors, the *Mirror*  
- **Lifestyle & Entertainment** → locked doors, the *Bunkers*  
- **Gaming** → a broken lock: usually closed, but vulnerable to large cultural waves
