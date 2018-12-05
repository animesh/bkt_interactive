# Bayesian Knowledge Tracing Explainable

Bayesian Knowledge Tracing (BKT) is a ML algorithm used in many intelligent tutoring systems to model a student's "mastery" of a particular skill, given a series of questions. While many learners rely on this algorithm to give an accurate prediction of their current learning, however, most do not actually understand how BKT works. The goal of this project is to convey this information to potential users, comparing both interactive and static (reading through text summaries) approaches, through a web-based scrollable "explainable." We will then assess the effectiveness of each technique and the overall sentiments (fairness, trust) users may express now that the algorithm has become more transparent. 

## Methodology 

We will perform our study with Mechanical Turk users, using the survey as our primary method for both pre-test and post-test. For our explainble, we aim to teach the following tasks, as categorized by the Cognitive Process Dimension, a modified version of Bloom's Taxonomy:
1. Recall what BKT stands for.
2. Explain the context in which BKT is used. 
3. List the 4 parameters used in the algorithm and be able to explain what each means:
* P(G): guess parameter, does not know skill but correct response
* P(S): slip parameter, knows skill but incorrect response
* P(L_0): initial probability of knowing each skill
* P(T): probability of learning the skill
4. Explain what it means for parameters to have “weights” and who ultimately determines these weights.
5. Calculate probability of mastery before the student answers any questions given the four parameter values and weights. 
6. Know which formula to use (or at least, that the formulas are different) depending on whether the student gets the subsequent question correct or incorrect.
7. Explain how before a student gives a response, system re-calculates probability that the student knew the skill before response (conditional probability)
8. Assign a skill to be mastered/unmastered based on the current mastery percentage.
9. Be able to make commentaries about whether the algorithm is reliable and whether there are any circumstances where it fails to capture mastery of a certain skill.

The Knowledge Dimension  | Remember | Understand | Apply | Analyze | Evaluate | Create
------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
Factual  | 1 | | | | 5 | |
Conceptual | 2, 3 | 4 | | | 8 | 12
Procedural | | 10 | 6 | 7 | | 13
Meta-cognitive | | | | 9 | | |


## Running on local host

First, install Idyll using `npm`
```
$ npm install -g idyll
```
Then, install all the necessary package dependencies with 
```
$ npm install
```
The working model can now be run on localhost:3000 using the command
```
$ idyll index.idyll --watch
```
Note: Two versions of the explainable, an interactive version and a static version, were created to quantify the effects of including clikable elements to engage the user. Currently, the interactive version is stored in `index.idyll` (default Idyll go-to when running the `--watch` command and the static version is stored in `index_static.idyll`. Running the above code by replacing `index.idyll` with `index_static.idyll` will not work because Idyll has other dependencies linked to that particular filename. Instead, the current workaround would be to rename each file (we did not elect to place them in completely separate repositories as that would generate a large amount of duplicate files).

## Deploying to web

The necessary files for deployment are generated when the `--watch` command is run, as Idyll produces raw HTML/css scripts from our wrapper and stores them in the `\build` folder. Alternatively, if watching was not necessary and only the raw scripts were desired, run `npm build` instead for the same results. 

We chose to host these sites on GitHub Pages. 
Interactive version: https://eutopi.github.io/bkt-explorable/
Non-interactive version: https://eutopi.github.io/bkt-static/
