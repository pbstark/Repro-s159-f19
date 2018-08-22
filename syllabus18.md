<!--- compile: pandoc syllabus18.md -o syllabus18.pdf --toc --toc-depth=4 -->
##### Statistics 159/259: Reproducible and Collaborative Statistical Data Science
##### [Philip B. Stark](http://www.stat.berkeley.edu/~stark), Department of Statistics, UC Berkeley
##### [www.stat.berkeley.edu/~stark](http://www.stat.berkeley.edu/~stark) pbstark@berkeley.edu @philipbstark
##### Office: 403 Evans Hall. Office hours: TBA

##### This version: 21 August 2018. Latest version: [here](http://www.stat.berkeley.edu/~stark/Teach/S159/syllabus18.pdf)

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
numpy, scipy, matplotlib, and perhaps pandas and scikit; git; GitHub; Travis CI; 
Docker; LaTeX,
Markdown, pandoc)

### Format and assessment
+ 3 hours of lecture and 2 hours of lab per week
+ approximately 5 "small" individual assignments (40% of grade)
+ 2 larger projects (30% of grade) 
+ a group term project (30% of grade)

### Office hours
+ Mondays 12:15-1:15, 403 Evans Hall

### Graduate Student Instructor
+ Mitch Negus, mitchell_negus@b.e
+ Office hours TBA


_Submitting assignments:_ Written assignments will be submitted using pull requests; details
to come.

+ Text documents should be written in LaTeX or Markdown. A pdf and the source file should be submitted. Microsoft Word is not acceptable.
+ Code and analyses should be in python. All code should have accompanying unit tests. In some cases, Jupyter notebooks will be the appropriate thing to submit; in others (more extensive analyses), a collection of .py files will be more appropriate. For term projects, the "deliverable" will include a repository that includes code, data, analyses, unit tests, and coverage tests.


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

## Resources

+ Git and git workflows
    - [Introduction to Git](https://github.com/berkeley-scf/tutorial-git-basics/blob/master/git-intro.md). This is based on the notes we used in this class, but has a fair amount of additional explanation and detail you may find useful through the semester.
    - [Immersion course](http://gitimmersion.com)
    - [git-scm guide](https://book.git-scm.com)
    - [Statlab development git workflow](http://statlab.github.io/permute/dev/index.html)
    
+ Continuous integration
    - [Travis CI for beginners](https://docs.travis-ci.com/user/for-beginners/)
    - [Continuous integration with Travis](http://www.vogella.com/tutorials/TravisCi/article.html) by Simon Scholz
    
+ Scientific Python, Jupyter
    - [Lecture notes on scientific python](https://www.scipy-lectures.org/intro/)
    - [Python for scientific computing](http://fperez.org/py4science/) by Fernando Perez
    - https://hplgit.github.io/primer.html/doc/pub/half/book.pdf
    - [Elegant SciPy](http://proquest.safaribooksonline.com/9781491922927), [Stefan van der Walt](https://bids.berkeley.edu/people/st%C3%A9fan-van-der-walt). The [full book](https://github.com/elegant-scipy/elegant-scipy) and all the [notebooks](https://github.com/elegant-scipy/notebooks) are available.
    - [Getting started with Python for research](https://github.com/TiesdeKok/LearnPythonforResearch), a gentle introduction to Python in data-intensive research.
    - [An introduction to "Data Science"](https://github.com/stefanv/ds_intro), a collection of Notebooks by BIDS' [Stéfan Van der Walt](https://bids.berkeley.edu/people/st%C3%A9fan-van-der-walt).
    - [Effective Computation in Physics](http://proquest.safaribooksonline.com/book/physics/9781491901564), by Kathryn D. Huff; Anthony Scopatz. [Notebooks to accompany the book](https://github.com/physics-codes/seminar).
    - [A Whirlwind Tour of Python](https://jakevdp.github.io/WhirlwindTourOfPython/index.html), by Jake VanderPlas.
    - [Python for Data Analysis, 2nd Edition](http://proquest.safaribooksonline.com/book/programming/python/9781491957653), by  Wes McKinney, creator of Pandas. [Companion Notebooks](https://github.com/wesm/pydata-book)
    - [Effective Pandas](https://github.com/TomAugspurger/effective-pandas), a book by Tom Augspurger, core Pandas developer.

+ Docker
    - to come...

+ LaTeX
    - to come

+ Markdown
    - https://daringfireball.net/projects/markdown/syntax
    - https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
    - https://www.markdownguide.org/getting-started/
    
+ Pandoc
    - 
    
+ General computing tutorials
    - [Berkeley Statistical Computing Facility tutorials](http://statistics.berkeley.edu/computing/training/tutorials)


## Topics by week 

### Week 1

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
            - usually impossible from just the methods section
            - much harder if the analysis was not scripted
            - might be impossible even with their code
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
    - papers where there seemed to be a chance to get the data
    - topics with social impact: food, health, 
    - some paper I think are bogus
    - some papers whose conclusions I like--scrutiny to avoid confirmation bias

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

#### Assignment **Due 9/3, 11:59pm:** 
1. Look at 
[the data Morabia transcribed from P.C.A. Louis on bloodletting for pneumonia](http://www.epidemiology.ch/history/louis.htm) and read Morabia (2006). What do you think of the fact that data from 1828 are available?
Reproduce the results Morabia cites:

- 77 patients
- 2 comparison groups of 41 and 36 patients
- comparable average age (41 and 38 years, respectively)
- number of patients bled on the first day, who had passed the age of fifty, was nearly twice as great as that of the patients of the same age, who were bled at a later period
- duration of disease was an average of 3 days shorter in those who had been bled early compared with those who had been bled late
- `three sevenths' (i.e., 44 %) of the patients who had been bled early died 
- `only one fourth' (i.e., 25 %) of those bled late died  
Is Louis's work an observational study or an experiment? 
Do you think it amounts to a "natural experiment"?
Why or why not? 
Give two scientific questions (_statistical hypotheses_) those data might address. 
What do you think the most important confounding factors would be, for those two hypotheses? 
What would be the most natural "as-if" randomization to use in analyzing 
the data to address the hypotheses you formulated, if you were to consider 
the study to be a natural experiment? 
What are the controls? Is the experiment blind? Double-blind? 
Explain how you might use the Neyman model to analyze the data. 
Is the randomization assumption reasonable? 
Why or why not? Is the non-interference assumption reasonable? Why or why not?

1. Read Karp et al. (2015) and look at the data they provided in Data Dryad.
Which figures and tables in the paper could, in principle, be reproduced from the data they provide?
Which cannot?
Does the methods section describe how they processed the data in adequate detail to
reproduce the analyses? If not, what else would you need to know?


## Collected Reading List:


__Foundations; Statistical Models__

1. Feynman, R., 1974. CalTech Commencement Address,  
http://calteches.library.caltech.edu/51/2/CargoCult.htm

1. Freedman, D.A., 1995. Some issues in the foundations of statistics, _Foundations of Science_, _1_, 19--39. https://doi.org/10.1007/BF00208723

1. Freedman, D.A., 1999. From association to causation: some remarks on the history of statistics, _Statistical Science_, _14_(3), 243--258.

1. Freedman, D.A., and R. Berk, 2001. Statistical Assumptions as Empirical Commitments,  
http://escholarship.org/uc/item/0zj8s368#page-1
(also in Freedman, D.A., 2010. _Statistical Models and Causal Inference: A dialog with the Social Sciences_, Cambridge University Press. D. Collier, J. Sekhon, P.B. Stark, eds.)

1. Freedman, D.A., 2008. On types of scientific inquiry: the role of qualitative reasoning, _The Oxford Handbook of Political Methodology_, Box-Steffensmeier, J.M., H.E. Brady, and D. Collier (eds), Oxford University Press, Oxford. DOI: 10.1093/oxfordhb/9780199286546.003.0012. [Preprint](https://www.stat.berkeley.edu/~census/anomaly.pdf)

1. Freedman, D.A., 2009. _Statistical Models: Theory and Practice_, 2nd edition, Cambridge University Press.

1. Freedman, D.A., R. Pisani, and R. Purves, 2007. _Statistics, 4th edition_, W.W. Norton, New York.

1. Klemes, V., 1989. The Improbable Probabilities of Extreme Floods and Droughts, in O. Starosolsky and O.M. Meldev (eds), _Hydrology and Disasters_, James and James, London, 43--51.  
https://www.itia.ntua.gr/en/getfile/1107/1/documents/1997_ImprobProbabilities_OCR.pdf

1. LeCam, L., 1977.  Note on metastatistics or 'An essay toward stating a problem in the doctrine of chances,' _Synthese_, _36_, 133-160.

1. Stark, P.B., 1997. [SticiGui](https://www.stat.berkeley.edu/~stark/SticiGui/)

1. Stark, P.B., 2016a. 
[Pay no attention to the model behind the curtain](https://www.stat.berkeley.edu/~stark/Preprints/eucCurtain15.pdf)

1. Stark, P.B., 2016b. The value of P-values, _The American Statistician_, _70_, DOI:10.1080/00031305.2016.1154108

1. Stark, P.B., 2017. [Mathematical Foundations](https://github.com/pbstark/S157F17/blob/master/math-foundations.ipynb), [Inequalities](https://github.com/pbstark/S157F17/blob/master/math-inequalities.ipynb), [Introduction to permutation tests](https://github.com/pbstark/S157F17/blob/master/permute-intro.ipynb), [Rabbits and Cargo-Cult Statistics](https://github.com/pbstark/S157F17/blob/master/rabbits.ipynb), [Generating pseudo-random samples and permutations](https://github.com/pbstark/S157F17/blob/master/permute-sample.ipynb)

1. Stark, P.B., and A. Saltelli, 2018. Cargo-cult Statistics and Scientific Crisis, _Significance_, _15_(4), 40--43. https://www.significancemagazine.com/593

__Agriculture, Ecology, and Health__

1. Fagan, J., T. Traavik, and T. Bøhn, 2015. The Seralini affair: degeneration of Science to Re-Science?, _Environmental Sciences Europe_, _27_:19, DOI 10.1186/s12302-015-0049-2

1. Karp, D.S., S. Gennet, C. Kilonzo, M. Partyka, N. Chaumont, E.R. Atwill, and C. Kremen, 2015.  Comanaging fresh produce for nature conservation and food safety, _PNAS_, _112_ (35) 11126-11131. https://doi.org/10.1073/pnas.1508435112

1. LeCanne, C.E., and J.G. Lundgren, 2018. Regenerative agriculture: merging farming and natural resource conservation profitably, _PeerJ_ 6:e4428 https://doi.org/10.7717/peerj.4428

1. Morabia, A., 2006. Pierre-Charles-Alexandre Louis and the evaluation of bloodletting, _J. Roy. Soc. Medicine_, _99_, 158--160. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1383766/pdf/0158.pdf

1. Seralini, G.-E., E. Clair, R. Mesnage, S. Gress, N. Defarge, M. Malatesta, D. Hennequin, and J. Spiroux de Vendômois, 2014. Republished study: long-term toxicity of a Roundup herbicide and a Roundup-tolerant genetically modified maize, _Environmental Sciences Europe_, _26_:14, http://www.enveurope.com/content/26/1/14 

__Earthquake probabilities__

1. USGS 2008 Bay Area Earthquake Probabilities.  
http://earthquake.usgs.gov/regional/nca/ucerf/

1. Cornell, C.A., 1968. Engineering seismic risk analysis, _Bull. Seism. Soc. Am_, _58_, 1583--1606. 

1. 1. Mulargia, F., P.B. Stark, and R.J. Geller, 2017. Why is probabilistic seismic hazard analysis (PSHA) still used? _Physics of the Earth and Planetary Interiors_, _264_, 63-75. https://doi.org/10.1016/j.pepi.2016.12.002

1. Stark, P.B. and D.A. Freedman, 2003. What is the Chance of an Earthquake? in
_Earthquake Science and Seismic Risk Reduction_, F. Mulargia and R.J. Geller, eds.,
NATO Science Series IV: Earth and Environmental Sciences, v. 32, Kluwer, Dordrecht, The Netherlands, 201–213. Preprint: http://www.stat.berkeley.edu/~stark/Preprints/611.pdf

__Impact of Climate Change__

1. Houser, T., R. Kopp, S. Hsiang, M. Delgado, A. Jina, K. Larsen, M. Mastrandrea, S. Mohan, R. Muir-Wood, D.J. Rasmussen, J. Rising, and P. Wilson, 2014. The American Climate Prospectus:  Economic Risks in the United States, 2014. http://rhg.com/reports/climate-prospectus

1. Hsiang, S., R. Kopp, A. Jina, J. Rising, M. Delgado, S. Mohan, D.J. Rasmussen, R. Muir-Wood, P. Wilson, M. Oppenheimer, K. Larsen, and T. Houser, 2017. Estimating economic damage from climate change in the United States, _Science_, _356_, 1362-1369 DOI: 10.1126/science.aal4369

1. Ranson, M., 2014. Crime, weather, and climate change, _Journal of Environmental Economics and Management_, _67_(3), 274-302. https://doi.org/10.1016/j.jeem.2013.11.008

1. Saltelli, A., P.B. Stark, W. Becker, and P. Stano, 2015. Climate Models as Economic Guides: Scientific Challenge or Quixotic Quest?, _Issues in Science and Technology_, Spring 2015. Reprint: http://www.stat.berkeley.edu/~stark/Preprints/saltelliEtal15.pdf

1. Urban, M.C., 2015. Accelerating extinction risk from climate change, _Science_, _348_, Issue 6234, 571--573, DOI: 10.1126/science.aaa4984, http://science.sciencemag.org/content/348/6234/571.full


https://proxy.eplanete.net/galleries/broceliande7/node/1584/1584/pathway

__Reproducibility__

1. J.B. Buckheit and D.L. Donoho, 1995. Wavelab and Reproducible Research, https://statweb.stanford.edu/~wavelab/Wavelab_850/wavelab.pdf

1. [Implementing Reproducible Research](https://osf.io/s9tya), edited by V. Stodden, F. Leisch and R. Peng

1. [The Practice of Reproducible Research: Case Studies and Lessons from the Data-Intensive Sciences](https://www.practicereproducibleresearch.org) Kitzes, Turek and Deniz, eds.

1. [Reproducibility: a Primer on Semantics and Implications for Research](https://www.rti.org/sites/default/files/resources/18127052_Reproducibility_Primer.pdf) 

1. Stark, P.B., 2018. No Reproducibility Without Preproducibility, _Nature_, _557_, p613. https://www.nature.com/magazine-assets/d41586-018-05256-0/d41586-018-05256-0.pdf 
doi: 10.1038/d41586-018-05256-0

1. Stark, P.B., 2017. [Preface](https://www.practicereproducibleresearch.org/core-chapters/0-preface.html) to _The Practice of Reproducible Research_, J. Kitzes, D. Turek, and F. Deniz, eds., University of California Press, Berkeley

