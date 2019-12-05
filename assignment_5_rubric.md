## Assignment 5 rubric

+ How many of the co-authors in Silberzahn et al. are in Statistics departments?
    - **1 is in a department of Math & Stats, and 1 is at Westat (a company that specializes in statistics). Most are in psychology, sociology, or business/management**
    
+ The basic question the teams are supposed to answer is "are soccer referees are more likely 
to give red cards to dark-skin-toned players than to light-skin-toned players?" 

    - Explain in your own words what "more likely" means here.
         - **very hard to turn this into a math question, because it confounds player behavior skin tone. It should mean something like, "if a darker-skinned player had lighter skin, he would have gotten fewer flags; if a light-skinned player had had darker skin, he would have gotten more flags**
         - **another view is that a given act (or style of play) committed by a light-skinned players gets a flag less often than the same act committed by a darker-skinned player**
         - **it can't just mean that the rate of flags differs for players with different skin tones--that can just be calculated. It doesn't involve inferences or counterfactuals. However, one could ask whether the difference in rates is larger than one would expect by chance, if skin tone were a random label.**
         
    - Is there anything random going on? If so, what? What makes it random?
        - **nothing random. many "haphazard" or unpredictable things**
        
    - What would "equally likely" look like in the real world?
        - **very hard to say**
        - **One possible hypothetical counterfactual is that changing a given player's skin tone would not change the number of flags he received.**
        
    - Is the question about individual referees, or referees in general?
        - **as framed, the research question isn't clear, but the analyses seem to be about referees in general. However, analyses that separate things geographically or by league may be controlling to some extent for differences among referees in different leagues**
        
+ For teams 1--6 and 12 (seven teams) in Silberzahn et al., explain the following:
    - Does the analysis implicitly or explicitly involve a model? If it does:
        - Describe the model
        - List and explain the assumptions of the model
        - Assess the evidence that the model is a response schedule
        - Describe any goodness-of-fit tests the team used to check the adequacy of the model
        - Explain in words what "OR" means for each of the models. 
            + What is OR or what parameter does it estimate? 
            + Are the confidence intervals really confidence intervals? Why or why not? 
                - **None is a confidence interval, even approximately, because nothing is random here: no random sample of games, players, etc.; no random measurement error; etc.**

### Summary of teams' final methods

#### Team 1
+ Tried multiple analyses, so p-values and confidence intervals don't mean anything, even if the sample had been random.
+ Models: linear probability model, "nonlinear" linear probability model with dummy variables for skin tone, logistic regression
    - linear probability model, "nonlinear" model: flag is a linear function of skin tone (on scale of 1-5, or using dummy variables), player characteristics (height,height-squared, weight, weight-squared, age, and age-squared), and fixed effects for  referee, league country, club, and player position 
    - logistic regression
    - in all 3 cases, they use 5 different combinations of covariates: 
        1. skin tone alone (either quantitative or categorical)
        1. tone + player characteristics
        1. tone + player + league + position
        1. tone + player + league + position + club
        1. tone + player + league + position + club + referee
    - no reason to think models are response schedules; inconsistent with each other
    - no goodness of fit test
    - not clear how they get the estimated OR. It should be the chance of a flag for darkest skin tone minus chance for lightest skin tone, but that depends on the other covariates. Must average over something or normalize somehow.
    - CIs are not really CIs: nothing really random, model unrealistic, ignores multiplicity

#### Team 2
+ Tried multiple analyses, so p-values and confidence intervals don't mean anything, even if the sample had been random.
+ Models: Linear probability model, logistic regression. Models chance of at least one red card, not distribution of red cards. Fixed effect for referee country of origin.
    - LPM probability of a flag is a linear function of the covariates
    - LR probability of a is a logistic function of covariates
    - no reason to think either is a response schedule; inconsistent with each other
    - no goodness-of-fit test
    - OR comes from the logistic regression, where it gives the ratio of the (estimated) probability of a flag for darkest skin tone divided by (estimated) probability for lightest skin tone
    - CIs are not really CIs: nothing really random, model unrealistic, ignores multiplicity
    
#### Team 3 
+ Tried multiple analyses, so probabilities don't mean anything. Adjusted the model after the fact to make the credible region exclude zero!
+ Multilevel Bayesian binomial logistic regression 
    - flags Binomial per (player, ref) pair; n=games played, probability of success is logistic in skin tone, position, league, referee country of origin; prior for coefficients is Normal with mean 0 and variances set in an unspecified way (possibly fit to the data)
    - no reason to think model is a response schedule; extremely contrived prior
    - no goodness-of-fit test, but did look at the predictive accuracy in an ad hoc way. Notes that "null" model does essentially as well.
    - OR comes from coefficient of skin tone in logit; in the model, it's the right probability ratio
    - Credible regions are not really credible regions: model adjusted a posteriori. Model unrealistic. Moreover, credible intervals are not confidence intervals.
    
#### Team 4 
+ Added a variety of analyses, but didn't change the primary analysis---which does show positive association.
+ Test based on Spearman correlation, but "judgment" turned significant positive correlation into "no effect"
    - correlation not stratified or otherwise adjusted for reasonable confounders
+ no explicit model; under the null, values of skin tone are conditionally exchangeable given flags
+ exchangeability assumption seems like a "straw man" null hypothesis, since it doesn't control for position, etc.
+ no goodness of fit test (but no model)
+ OR should 1 according to the analysis
+ no CI
    
#### Team 5 
+ Formulated model after looking at the data, so all bets are off regarding p-values, etc.
+ Generalized linear mixed model; some data transformations. Reduced flags per game to indicator.
    - Flags binomial for (player, ref) pairs. n=games. P(flag) has dummy for referee and a coefficient for "playersShort" (never defined, but the description talks about a random effect for each player. Perhaps it's the "short name" for each player.)
    - no reason to think anything is a response schedule.
    - no goodness-of-fit test; scatterplots suggest model doesn't fit well
    - OR comes from a coefficient in the model
    - CIs are not real CIs: nothing random, model unrealistic, model selection involved
    
#### Team 6 
+ Tried several formulations, but finds nothing significant for any of them, so multiplicity isn't an issue. Uses only a subset of the data: first encounter between ref and player.
+ Linear probability model with dummy variables for skin tone; notes problems with confounding and lack of randomization. Discussion is Bayesian (refers to "priors" a referee might have), but the analysis is not Bayesian.
    - no reason to think model is a response schedule (but that's not required given the way the author frames things)
    - no goodness-of-fit test
    - OR estimate comes from ratio of average probabilities for darkest (card v no card) to lightest (card v no card) skin tones; not really an OR
    - reports t statistics and has significance asterisks in some table entries, but doesn't seem to report CIs. The significance numbers are not meaningful because nothing is stochastic, and the model is unrealistic. Moreover, tried several analyses.

#### Team 12 

+ Zero-inflated Poisson regression
    - covariates included skintone (continuous/linear), implicit & explicit bias in referee's country of origin, player weight, position, and number of games for the (player, referee) pair.
    - reports fitting four variations of the model, so multiplicity is an issue
    - no reason to think anything is a response schedule.
    - no goodness-of-fit test or even plots of the data
    - OR presumably derived from skin-tone coefficient, but not clear from description
    - significance levels and CIs are not real: nothing random, model unrealistic, model selection involved
