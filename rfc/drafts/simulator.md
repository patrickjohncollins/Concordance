# The simulator and Pattern Sharing data

```
RFC:        (assigned on agreement)
Slug:       simulator
Title:      The simulator and Pattern Sharing data
Status:     Draft
Intended:   Experimental
Authors:    Patrick Collins
Created:    2026-11-22
Updates:    none
Licence:    CC-BY-SA-4.0
Discussion: stewards' circle
```

A long-lived simulator of society tests whether Concordance's virtuous cycle holds (help builds trust, trust brings giving, visible results bring invitations, circles split and federate, trust land makes gains permanent) and what breaks it. It is built test first, runs the real accord engine, and is fed over time with real patterns from circles that choose to share them.

**Architecture**

- **Shared core (Rust):** the same accord engine and record validation as the app, so simulations test the real accords. A Python layer, through Rust–Python bindings, for scenarios, experiments and analysis.
- **Synthetic populations** for real places, built from census and survey data (iterative proportional fitting), with household, kin, neighbor, work, faith and friendship ties.
- **Environment and shocks:** geography from OpenStreetMap, public services, cost of living, holy days; individual shocks (illness, job loss, birth, death) and shared ones (recession, heatwave, flood, outage).
- **Economy as conditions, not a full model:** household facts (income, time use, housing, care burden, connectivity) and social facts (trust, participation, networks) matter most; macroeconomics enters only as shocks, with feedback into the wider economy deferred to later versions.
- **Time:** daily steps, hourly during crises; every action written to an event log.

**Agents**

- **Rule-based agents** for towns and cities: time budgets, generosity, trust, fatigue, reciprocity; joining follows complex contagion (an agent joins after enough close ties have), which Damon Centola's research suggests spreads committed behavior best through tight clusters.
- **AI-model agents** for small samples, with personas and a fixed action set (help, ask, join, leave, object, propose). Their agreeableness suits the seed phase of likely early adopters, so they get time budgets, fatigue and some strong disagreements; more varied, skeptical, time-poor agents test crossing the chasm to the pragmatic majority. Their behavior is summarized into rules for the large-scale engine.

**Metrics:** unmet needs, loneliness, wellbeing, burnout, adoption, circle survival, inequality of unmet needs between groups, cross-group ties, trust, land in trust, always including worst-off outcomes as well as averages.

**Testing, non-binary where it should be**

- **Binary:** rules and invariants (time is never created; a tool is in one place at once; trust land never leaves trust); reproducibility from a seed; reproducing Schelling's segregation and Axelrod's cooperation results.
- **Statistical:** Concordance claims as Given/When/Then scenarios over many seeds, checked by ranges, confidence intervals and worst-case bounds.
- **Calibration:** group sizes, volunteering rates and growth roughly match real data.
- **Regression:** every change to the Charter, an accord or the app reruns the simulation suite; changes that worsen burnout, exclusion or inequality are flagged before release. Results inform judgment; real pilots are the acceptance tests.

**Real data through the Pattern Sharing accord** Patterns, never people. Circles opt in by agreement and choose each item shared (circle health, responsiveness, accords used, crisis response, optional anonymous wellbeing answers, land in trust). Figures are computed on the circle's hearths; only aggregates leave, with minimum group sizes and differential privacy. Never shared: names, message content, who helped whom, attendance, precise locations. Not available to circles under Anonymity or High Risk. Data is used only to improve Concordance, never sold, never given to authorities, never used to judge circles; results are published openly. A pattern steward role answers members' questions. Records: `pattern.adopted`, `pattern.item.changed`, `pattern.sent`, `pattern.withdrawn`.

**Build order**

1. Spec, with the first claims written as tests.
2. A minimal town of 5,000 rule-based agents with the Charter and Mutual Aid.
3. The shared accord engine running real provisions.
4. Adoption, splitting, mentoring and whole communities adopting together.
5. Crises and federation.
6. AI-model agents for the seed phase and the chasm.
7. Synthetic populations of real rural, suburban and urban places, calibrated.
8. Continuous comparison with real circles through Pattern Sharing.

The simulator lives in `sim/` beside the app and is built alongside the core library, since both use the accord engine.
