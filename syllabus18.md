<!--- compile: pandoc syllabus18.md -o syllabus18.pdf --toc --toc-depth=4 -->
##### Statistics 159/259: Reproducible and Collaborative Statistical Data Science
##### [Philip B. Stark](http://www.stat.berkeley.edu/~stark), Department of Statistics, UC Berkeley
##### [www.stat.berkeley.edu/~stark](http://www.stat.berkeley.edu/~stark) pbstark@berkeley.edu @philipbstark
##### Office: 403 Evans Hall. Office hours: TBA

##### This version: 16 August 2018. Latest version: [here](http://www.stat.berkeley.edu/~stark/Teach/S159/syllabus18.pdf)

# Reproducible and Collaborative Statistical Data Science: Overview

This course teaches reproducible and collaborative research techniques through
applied statistics, including reproducing published work and re-analyzing
the data in that work using other methods--reproducibly.

Examples will be drawn from a variety of fields, including agriculture, health, and
climate.

There will be roughly five small assignments and several larger projects.
Much of the work will be collaborative in groups of 4-5.
You will be asked to review your own contributions and each others contributions
to group projects.
There will not be a final exam, but there will be final presentations of group work.

## Administrativia

### Prerequisites
+ Statistics 133, 134, 135
+ Willingness to pick up programming languages and software tools independently 
(tools used will include 
Python; Jupyter Notebooks; the Python "scientific stack" of
numpy, scipy, matplotlib, and perhaps pandas and scikit; git; GitHub; Travis CI; LaTeX,
Markdown, pandoc)

### Format and assessment
+ 3 hours of lecture per week
+ written assignments (40% of grade)
+ term projects (60% of grade) 

_Submitting assignments:_ Written assignments will be submitted using pull requests; details
to follow.


### Code of conduct; attribution of work
The high academic standard at the University of California, Berkeley, is reflected in each degree 
awarded.
Every student is expected to maintain this high standard by ensuring that all
academic work reflects unique ideas or properly attributes the ideas to the original sources.

These are some basic expectations of students with regards to academic integrity:
Any work submitted should be your own individual thoughts, and should not have been submitted
for credit in another course unless you have prior written permission to re-use it in this 
course from this instructor.

All assignments must use "proper attribution," meaning that you have identified the original
source and extent or words or ideas that you reproduce or use in your assignment.
This includes drafts and homework assignments!
If you are unclear about expectations, ask your instructor.

Do not collaborate or work with other students on assignments or projects unless the 
instructor gives you permission or instruction to do so.

### Disability accommodations
If you need an accommodation for a disability, if you have information your wish to share with 
the instructor about a medical emergency,
or if you need special arrangements if the building needs to be evacuated, please inform the 
instructor as soon as possible.

If you are not currently listed with DSP (the Disabled Students' Program) and believe you might 
benefit from their support, please apply online at dsp.berkeley.edu

## Main topics by week 

### Week 1

#### Reading for discussion

1. [J.B. Buckheit and D.L. Donoho, 1995. Wavelab and Reproducible Research](https://statweb.stanford.edu/~wavelab/Wavelab_850/wavelab.pdf)

1. Freedman, D.A., and R. Berk, 2001. Statistical Assumptions as Empirical Commitments,  
http://escholarship.org/uc/item/0zj8s368#page-1
(also in Freedman, D.A., 2010. _Statistical Models and Causal Inference: A dialog with the Social Sciences_,
Cambridge University Press. D. Collier, J. Sekhon, P.B. Stark, eds.)

1. Klemes, V., 1989. The Improbable Probabilities of Extreme Floods and Droughts, in O. Starosolsky and O.M. Meldev (eds), _Hydrology and Disasters_, James and James, London, 43--51.  
https://www.itia.ntua.gr/en/getfile/1107/1/documents/1997_ImprobProbabilities_OCR.pdf

1. Morabia, A., 2006. Pierre-Charles-Alexandre Louis and the evaluation of bloodletting, 
_J. Roy. Soc. Medicine_, _99_, 158--160. 
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1383766/pdf/0158.pdf

1. https://digest.bps.org.uk/2017/06/20/5-reasons-its-so-hard-to-think-like-a-scientist/
https://www.sciencedirect.com/science/article/pii/S0079742116300214

1. Stark, P.B., and Saltelli, A., 2018. Cargo-Cult Statistics and Scientific Crisis,
_Significance_, https://www.significancemagazine.com/593

1. Stark, P.B., 2018. No Reproducibility Without Preproducibility, _Nature_, _557_, p613.
https://www.nature.com/magazine-assets/d41586-018-05256-0/d41586-018-05256-0.pdf 
doi: 10.1038/d41586-018-05256-0

1. Stark, P.B., 2017. [Preface](https://www.practicereproducibleresearch.org/core-chapters/0-preface.html) to 
_The Practice of Reproducible Research_, Justin Kitzes, Daniel Turek, Fatma Deniz, eds.,
University of California Press, Berkeley

1. Stark, P.B. and D.A. Freedman, 2003. What is the Chance of an Earthquake? in
_Earthquake Science and Seismic Risk Reduction_, F. Mulargia and R.J. Geller, eds.,
NATO Science Series IV: Earth and Environmental Sciences, v. 32, Kluwer, Dordrecht, The Netherlands, 201–213.  
Preprint:  
http://www.stat.berkeley.edu/~stark/Preprints/611.pdf

1. Stark, P.B., 2016a. 
[Pay no attention to the model behind the curtain](https://www.stat.berkeley.edu/~stark/Preprints/eucCurtain15.pdf)

#### Topics

+ What is reproducibility?
    - Why is reproducibility an issue?
    - Terms in different fields. Computational, experimental, ...
    - "Preproducibility"
    - What is contributing to lack of reproducibility in science?
    - Importance of replication
    - "Virtual witnessing"

+ Attempting computational reproducibility in data analysis
    - data
        + get the data
            - can be hard even if journal/funder requires making data available
        + figure out what format it's really in
            - data dictionaries sometimes help
            - proprietary formats common
        + figure out whether it's the right data
            - sniff tests
            - consistency tests
            - sleuthing
        + pre-processing, cleaning, etc.
    - analysis
        + figure out what they claim to have done
        + figure out what they did
        + figure out what they should have done
        + compare

+ Sciencing is hard
    - confirmation bias
    - easiest person to fool is yourself
    - misperceptions of probability
    - confidence and accuracy unrelated
    - shiny models and methods
    - broken reward structure
    - ritualization
    - Cargo-cult science and statistics

+ Papers/Datasets for the term
    - chose papers where there seemed to be a chance to get the data
    - chose topics with social impact: food, health, 
    - chose some paper I think are bogus
    - chose some papers whose conclusions I like---to avoid confirmation bias

+ Software engineering
    - revision/version control
    - documentation
    - modularity and abstraction
        - consistency: APIs, calling signatures, object-oriented coding
        - separating data, computation, presentation
        - how general is the problem your approach can solve?
            - what's the right level of abstraction?
            - does it solving it require other broadly useful tools?
            - consider other approaches to subproblems? 
            - don't re-invent the wheel...but understand how wheels work
    - unit tests, integration tests, regression tests, coverage tests
    - code review
    - pair programming
    - scripted analyses
    - automation
    - accountability

#### Assignment
1. **To hand in:** Look at 
[the data Morabia transcribed from P.C.A. Louis on bloodletting for pneumonia](http://www.epidemiology.ch/history/louis.htm). 
Is Louis's work an observational study or an experiment? 
Do you think it amounts to a "natural experiment"?
Why or why not? 
Give two scientific questions (_statistical hypotheses_) those data might address. 
What do you think the most important confounding factors would be, for those two hypotheses? 
What would be the most natural "as-if" randomization to use in analyzing 
the data to address the hypotheses you formulated, if you were to consider 
the data to be a natural experiment? 
What are the controls? Is the experiment blind? Double-blind? 
Explain how you might use the Neyman model to analyze the data. 
Is the randomization assumption reasonable? 
Why or why not? Is the non-interference assumption reasonable? Why or why not?
Implement permutation tests (in R or Python) for the hypotheses about 
bloodletting you formulated, using the data Morabia transcribed from Louis. 
Discuss numerical issues in implementing the permutation tests. 
What pseudo-random number generator did you use? How did you set the seed? 
How did you choose the number of random permutations or random samples to generate? 
How did you implement the procedure? (Is there a principle you might use to decide the number? 
If so, what?) What test statistic(s) did you use? Why did you pick those? 
How to they connect to the relevant alternative hypotheses? 
Do you think the results would be qualitatively different if you had used a 
different test statistic? 
Discuss your findings, including any weaknesses in your framing of the problem 
(the statistical assumptions) and in the numerical analysis. 
Test each component of your code using a unit test. 
Turn in your results and your code, including the unit tests of the code.

#### Lecture topics
+ reasoning and fallacies 
(reading: [SticiGui: Reasoning and fallacies](http://www.stat.berkeley.edu/~stark/SticiGui/Text/reasoning.htm))
+ observational studies and experiments 
(reading: [SticiGui: Does Treatment Have an Effect?](http://www.stat.berkeley.edu/~stark/SticiGui/Text/experiments.htm))
    - longitudinal and cross-sectional studies
    - confounding
    - controls
    - historical controls
    - randomization
    - placebos and the placebo effect

### Week 2

#### Reading for discussion



#### Assignment
Find three examples of probabilities in the popular press this week relating to
something scientific (not, for instance, sports).
For each, give a citation, a brief synopsis of the issue/claim, and explain what "probability"
means in the context of the article. 
In particular, explain whether the probability results from actual randomization, from a truly
stochastic phenomenon, or from a (metaphorical) model.
Is it a reflection of data, of physics, of expert opinion, of modeling choices, or what?
Try to assess whether the number is malleable: would different assumptions have led to
different numbers?
Or would it take different underlying data to yield different numbers?
How "objective" is each probability?

#### Lecture topics
+ what does "probability" mean?
(reading: [SticiGui: Probability: Philosophy and Mathematical Background](http://www.stat.berkeley.edu/~stark/SticiGui/Text/probabilityPhilosophy.htm);
[Stark, P.B. and D.A. Freedman, 2003](http://www.stat.berkeley.edu/~stark/Preprints/611.pdf))
+ the ontology of probability in science
    - deliberate randomization (random samples, randomized experiments)
    - stochastic phenomena (quantum physics, thermodynamics, "noise" processes)
    - models / assumptions (mostly invented--based on metaphor)
    - how do you justify a (stochastic) model?
        + scientific basis ("truth")
        + predictive power
        + compact description of data (goodness of fit)
        + other utility?
    - case study: Schwarzenegger's acrostic veto
    - case study: chance a couple has children born 8/8/08, 9/9/09, and 10/10/10
    - case study: the chance of a major earthquake in the Bay Area by 2030
+ surveys (reading: [SticiGui: Sampling](http://www.stat.berkeley.edu/~stark/SticiGui/Text/sampling.htm))
    - common survey designs
    - populations, frames, parameters, and statistics
    - response rates, self-selection, nonresponse bias
    - margin of error and confidence intervals
        + meaningless unless the sample is random
        + need to account for bias and nonresponse
        + can't blindly plug into formula: have to account for the sample design
    - priming, wording, etc.
    - semi-attached figures and red herrings
    - Internet surveys
    - snowball samples, sampling social networks, etc.
    - case studies:
        + The Hite Report
        + student evaluations of teaching

### Week 3

#### Reading for discussion


#### Assignment
Find an example of a margin of error or confidence interval
for a survey and a claim of statistical significance
(for any kind of study) in the popular press this week.
For each, give a citation and brief synopsis of the issue/claim and the experiment or
data source.
Explain/interpret the margin of error, confidence interval, and the significance level 
or p-value in plain
language.
Assess whether the uses of the margin of error, confidence interval
or test of significance are appropriate.
Was there a random sample? If so, what was the sample design? Was it a simple random sample?
Stratified? Cluster? Multi-stage? What was the response rate? Did the authors give you enough
information to evaluate the results?
What is the null hypothesis for the test of significance? Is is realistic, or a "straw man"?
Where does the probability "come from" in the confidence interval or
test of significance? Was there a randomized
experiment, a random sample, or something else?
Can you tell what formulae were used to find the margin of error, confidence interval,
or the p-value?
Do they fit the way the data were collected, or are they mechanical calculations
using irrelevant formulae?

#### Lecture topics

+ interpreting p-values; statistical significance and practical significance
    - null and alternative hypotheses
    - what are p-values, and why do people love to hate them?
    - "straw-man" null hypotheses; parametric and nonparametric tests
    - multiplicity, significance hunting. Voodoo correlation
    - does it matter?
    - are most scientific results wrong?
    - reproducibility and replicability
    - case study: banning p-values by _Basic and Applied Social Psychology_
    - case study: telepathy over the Internet
+ interpreting confidence intervals
+ meta-analysis
    - how many bad studies does it take to make a good study?
    - underlying assumptions
+ causal inference
    - hypothetical counterfactuals
    - importance of randomization and intervention
    - association versus causation
    - intention-to-treat analyses
    - quantifying the effect of treatment
    - generalizability
    - are Big Data a substitute for randomization and experimental design?

### Week 4

#### Reading for discussion



#### Assignment
Work on your [term project](./project.pdf).

#### Lecture topics



## Collected Reading List:

1. Boring, A., K. Ottoboni, and P.B. Stark, 2016. Student evaluations of teaching (mostly) do not measure teaching effectiveness, _ScienceOpen Research_, DOI: 10.14293/S2199-1006.1.SOR-EDU.AETBZC.v1 https://www.scienceopen.com/document?vid=818d8ec0-5908-47d8-86b4-5dc38f04b23e
1. Cornell, C.A., 1968. Engineering seismic risk analysis, _Bull. Seism. Soc. Am_, _58_, 1583--1606. 
1. Feynman, R., 1974. CalTech Commencement Address,  
http://calteches.library.caltech.edu/51/2/CargoCult.htm
1. Freedman, D.A., 1995. Some issues in the foundations of statistics, _Foundations of Science_, _1_, 19--39. https://doi.org/10.1007/BF00208723
1. Freedman, D.A., 1999. From association to causation: some remarks on the history of statistics, _Statistical Science_, _14_(3), 243--258.
1. Freedman, D.A., 2008. On types of scientific inquiry: the role of qualitative reasoning, _The Oxford Handbook of Political Methodology_, Box-Steffensmeier, J.M., H.E. Brady, and D. Collier (eds), Oxford University Press, Oxford. DOI: 10.1093/oxfordhb/9780199286546.003.0012. [Preprint](https://www.stat.berkeley.edu/~census/anomaly.pdf)
1. Freedman, D.A., 2009. _Statistical Models: Theory and Practice_, 2nd edition, Cambridge University Press.
1. Freedman, D.A., R. Pisani, and R. Purves, 2007. _Statistics, 4th edition_, W.W. Norton, New York.
1. Klemes, V., 1989. The Improbable Probabilities of Extreme Floods and Droughts, in O. Starosolsky and O.M. Meldev (eds), _Hydrology and Disasters_, James and James, London, 43--51.  
https://www.itia.ntua.gr/en/getfile/1107/1/documents/1997_ImprobProbabilities_OCR.pdf
1. LeCam, L., 1977.  Note on metastatistics or 'An essay toward stating a problem in the doctrine of chances,' _Synthese_, _36_, 133-160.
1. Morabia, A., 2006. Pierre-Charles-Alexandre Louis and the evaluation of bloodletting, _J. Roy. Soc. Medicine_, _99_, 158--160. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1383766/pdf/0158.pdf
1. Mulargia, F., P.B. Stark, and R.J. Geller, 2017. Why is probabilistic seismic hazard analysis (PSHA) still used? 
1. Stark, P.B., and D.A. Freedman, 2003. What is the Chance of an Earthquake?, in _Earthquake Science and Seismic Risk Reduction_, F. Mulargia and R.J. Geller, eds., NATO Science Series IV: Earth and Environmental Sciences, v. 32, Kluwer, Dordrecht, The Netherlands, 201-213. https://www.stat.berkeley.edu/~stark/Preprints/611.pdf
1. Stark, P.B., 1997. [SticiGui](https://www.stat.berkeley.edu/~stark/SticiGui/) Various chapters assigned below.
1. Stark, P.B., 2015. Constraints versus priors. _SIAM/ASA Journal on Uncertainty Quantification_, _3_(1), 586--598. doi:10.1137/130920721,  
Reprint: http://epubs.siam.org/doi/10.1137/130920721,  
Preprint: https://www.stat.berkeley.edu/~stark/Preprints/constraintsPriors15.pdf.
1. Stark, P.B., 2016a. [Pay no attention to the model behind the curtain](https://www.stat.berkeley.edu/~stark/Preprints/eucCurtain15.pdf)
1. Stark, P.B., 2016b. The value of P-values, _The American Statistician_, _70_, DOI:10.1080/00031305.2016.1154108
1. Stark, P.B., 2017. [Mathematical Foundations](https://github.com/pbstark/S157F17/blob/master/math-foundations.ipynb), [Inequalities](https://github.com/pbstark/S157F17/blob/master/math-inequalities.ipynb), [Introduction to permutation tests](https://github.com/pbstark/S157F17/blob/master/permute-intro.ipynb), [Rabbits and Cargo-Cult Statistics](https://github.com/pbstark/S157F17/blob/master/rabbits.ipynb), [Generating pseudo-random samples and permutations](https://github.com/pbstark/S157F17/blob/master/permute-sample.ipynb)
1. Stark, P.B., and A. Saltelli, 2018. Cargo-cult Statistics and Scientific Crisis, _Significance_, _15_(4), 40--43. Preprint: https://www.significancemagazine.com/593
1. Urban, M.C., 2015. Accelerating extinction risk from climate change, _Science_, _348_, Issue 6234, 571--573, DOI: 10.1126/science.aaa4984, http://science.sciencemag.org/content/348/6234/571.full


__Foundations of Statistics__

1. LeCam, L., 1977.  Note on metastatistics or 'An essay toward stating a problem in the doctrine of chances,' _Synthese_, _36_, 133-160.


__Agriculture, Ecology, and Health__

LeCanne, C.E., and J.G. Lundgren, 2018.
Regenerative agriculture: merging farming and natural resource conservation profitably,
_PeerJ_ 6:e4428 https://doi.org/10.7717/peerj.4428

__Earthquake probabilities__

USGS 2008 Bay Area Earthquake Probabilities.  
http://earthquake.usgs.gov/regional/nca/ucerf/

Stark, P.B. and D.A. Freedman, 2003. What is the Chance of an Earthquake? in
_Earthquake Science and Seismic Risk Reduction_, F. Mulargia and R.J. Geller, eds.,
NATO Science Series IV: Earth and Environmental Sciences, v. 32, Kluwer, Dordrecht, The Netherlands, 201–213.  
Preprint: http://www.stat.berkeley.edu/~stark/Preprints/611.pdf

__Impact of Climate Change__

The American Climate Prospectus:  Economic Risks in the United States, 2014.
Trevor Houser, Robert Kopp, Solomon Hsiang, Michael Delgado, Amir Jina, Kate Larsen,
Michael Mastrandrea, Shashank Mohan, Robert Muir-Wood, DJ Rasmussen, James Rising, and Paul Wilson.  
http://rhg.com/reports/climate-prospectus

Saltelli, A., P.B. Stark, W. Becker, and P. Stano, 2015.
Climate Models as Economic Guides: Scientific Challenge or Quixotic Quest?, 
_Issues in Science and Technology_,
Spring 2015.  
Reprint: http://www.stat.berkeley.edu/~stark/Preprints/saltelliEtal15.pdf


