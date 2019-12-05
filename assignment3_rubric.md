## Assignment 3 rubric

+ Urban reports, "Overall, 7.9% of species are predicted to become extinct from climate 
change; (95% CIs, 6.2 and 9.8) (Fig 1)."
    - Urban derives his estimate using "Bayesian meta-analysis"
        + Explain what meta-analysis is, including the assumptions (see Berk and Freedman)
            - _results are a random sample of possible experiments_
            - _experiments are independent of each other_
            - _the same thing is measured in every experiment_
            - _"effect size" (after the normalization by SE) has a normal distribution_
        + If you can, state the additional assumptions of Bayesian meta-analysis (this might require research)
            - _effect size has a prior probability distribution, i.e., nature generates it by drawing at random from some known probability distribution_
        + If you can figure it out from the paper and supplemental materials, state the prior Urban uses
    - Urban points out that there are several general approaches the underlying 131 studies use to estimate the number of species that will go extinct.
Sketch how these work:
        + Species-area relationships
            - _empirically, the larger area you look at, the more species you find. Generally represented as species are proportional to area to some power_
        + Expert opinion
            - _ask experts what they think. not necessarily any scientific bases_
        + Species distribution models
           - _observed associations between environmental variables and species presence or abundance_
    - Recall that the taxonomy of life is Kingdom, Phylum, Class, Order, Family, Genus, Species. 
There are about 1.9 million known species of eukaryotes (everything but bacteria), and it is estimated that there are 8.7 million in all.
There are estimated to be from millions to trillions of species of bacteria (prokaryotes).
        + Estimate the number of species included in the 131 studies Urban relied on (this might require research: explain how you get your estimate)
            - _on the order of hundreds; at most a few thousands_
        + Are those species a random sample of all known species? Of all species?
            - _no, no_
        + What animal genus has the most species?
            - _beetles_
            - Do any of the studies Urban relies on examine that genus? 
            - _no (as far as I can tell, no insects at all)_
        + What plant genus has the most species?
            - _ferns overall, but among flowering plants, Astragalus)_
            - Do any of the studies Urban relies on examine that genus?
            - _not clear. At most two, one of which is a study in Scandinavia_
        + Do any of the studies Urban relies on consider bacterial species?
            - _no_
        + What families does Urban's estimate consider? (do your best to figure this out--I don't expect you to read all 131 studies)
            - _he doesn't even identify the taxa consistently: puts on the same level "plants," "mammals," "invertebrates," etc. Some of the plant studies are only trees. Some are vascular plants of unidentified genera. My guess is on the order of a few hundred, but perhaps fewer.__
    - What data go into Urban's estimate?
            - _generally, estimates made by others using a variety of ad hoc methods, with no consistency_
    - What, if anything, is random in Urban's estimate?
        - _nothing_
    - Is the estimate of 7.9% of species unbiased? Why or why not? 
        - _no. The underlying "sample" and "population" aren't even well defined, much less the parameter he's trying to estimate_
    - Is the range (6.2%, 9.8%) a confidence interval? Why or why not?
        - _No. It is a posterior credible region. There's no random sampling anywhere, no consideration of bias, etc. The procedure has no known probability (if any) of producing an interval that includes the true parameter value._
    - Urban's estimate does not have a timeline: it's "climate change," not "climate change over the next 50y," for instance. How does that make sense?
        - _he links it to a fixed temperature change_
    - List 5 potentially large sources of uncertainty that Urban did not consider or did not address adequately
        - _geographic sampling, species sampling, literature sampling, model form, uncertainty in species-area relationships, uncertainty in species distribution models (SDM), bias in SDM samples because of the tendency to look for rare species instead of common species, publication bias (treated slightly), treating species-area relationships and SDMs as response schedules, none of the assumptions of meta-analysis are true, arbitrariness of the prior, multiple data transformations and model selection, etc._
    - On balance, do you think the 7.9% ((6.2%, 9.8%) figures are reliable? Useful? Interpretable?