# Notes from Learning at Scale - Day 1

[Go back to main page](/las2017)

[Go to Day 2](/las2017/notes2)

[See the proceedings on ACM](http://dl.acm.org/citation.cfm?id=3051457&preflayout=flat)

## Robust Evaluation Matrix

Doroudi et al.
A/B testing?
Instructional policy : flowchart

Calibrate a best policy for one student model
=> Might not be good for other models
! Not try to be good everywhere, otherwise overfitting

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">Shayan Doroudi, Vincent Aleven, Emma Brunskill of <a href="https://twitter.com/CSDatCMU">@CSDatCMU</a> on &quot;Robust Evaluation Matrix&quot; <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a> <a href="https://t.co/mer7cZbprM">pic.twitter.com/mer7cZbprM</a></p>&mdash; ACM Learning Center (@acmeducation) <a href="https://twitter.com/acmeducation/status/855074460797460480">20 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Visual approach

Design space unlimited
Solution space underdefined

Compromise between top-down expert et bottom-up data-driven

Their tool, **tempr** is [on GitHub](https://github.com/fratamico/Tempr---A-visual-knowledge-engineering-tool).

Allows to merge actions and see the amount of these buckets of actions in the logs over time (for high learners and low learners), potentially to verify theories.

Tested on a complex interface for learning electrical engineering:

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">Combining to down and bottom up analyses to understand complex learning at <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a>. <a href="https://twitter.com/PhETsims">@PhETsims</a> <a href="https://t.co/7henvfrUDF">pic.twitter.com/7henvfrUDF</a></p>&mdash; Ido Roll (@hummus_monster) <a href="https://twitter.com/hummus_monster/status/855075352959479808">20 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Next Step Recommendation

Navigational efficiency: jump directly to resource

Use LSTMs (certain type of recurrent neural networks) to model the behavior of a student given their history, and predict the next page on which they will spent more time (in order to recommend it to them).

Do not only train on certified students, in order to get more data.

- Baseline (next lesson): 52%
- n-gram: 61%
- LSTM: 64%

They had to log the visited pages via JavaScript.

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">A new way for MOOCs to automatically adapt themselves based on learners’ behavior, from <a href="https://twitter.com/zpardos">@zpardos</a>: <a href="https://t.co/eUfVE5bvrV">https://t.co/eUfVE5bvrV</a></p>&mdash; Berkeley I School (@BerkeleyISchool) <a href="https://twitter.com/BerkeleyISchool/status/852585950190456833">13 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Computational Approaches to Human Learning (CAHL) Research is [on GitHub](https://github.com/CAHLR).

### Questions

- Why not recommend several pages?
- Indeed we should, more relevant course, more relevant discussion post, etc.
- For adults: several choices is better, for kids: one choice is better.

- You did collaborative filtering, why not content-based?
- We should try, yes.

- Why LSTM, not other approaches?
- Not matrix factorization because there is a high temporal component (but we could do tensor factorization, right).

- What if it hurts? Because you're not optimizing anything.
- Maybe yes.

## Learning to program with localization

Are learning outcomes associated with the presence or absence of localization in educational software?

Did users of Scratch learned programming better if the blocks were in their language?

TL;DR: No.

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">Source code has been translated in <a href="https://twitter.com/scratch">@scratch</a> even if the original project has been built in English. <a href="https://twitter.com/hashtag/crowdsourced?src=hash">#crowdsourced</a> process <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a> <a href="https://t.co/9pjF6klNZi">pic.twitter.com/9pjF6klNZi</a></p>&mdash; Ella Hamonic (@Ella_Hmc) <a href="https://twitter.com/Ella_Hmc/status/855109380035022851">20 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

### Statistics

- 20.8M projects shared
- 17M users
- 107M comments
- 3M studios created

See also [scratch.mit.edu/statistics](https://scratch.mit.edu/statistics)

Study done on Portugal, Italy, Brazil, Germany, Norway.

They discovered: for 80% of the users, language does not change.

Measure of learning: block repertoire (~ vocabulary).

Main advantage: localization may save users that might not learn code at all.

## Teaching Students to Recognize and Implement Good Coding Style

They built AutoStyle, a tutor that automatically generates hints and feedback regarding the style of Python code.

Goal: Optimize readability of the reviewers.

Goal of the research: see if multiple-choice questions / hints can help acquire good style.

- Use of built-in functions
- Avoid unnecessary control structures

Metrics: ABC Score (Assignment, Branch, Conditional)

- We want to avoid that students code in FORTRAN. At least they should learn some idioms. The question is: Is that medium skill learnable?

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">How to teach writing code at scale? Commenting, coding styles... how to assess those skills? <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a> <a href="https://t.co/YIflBhtzBN">pic.twitter.com/YIflBhtzBN</a></p>&mdash; Ella Hamonic (@Ella_Hmc) <a href="https://twitter.com/Ella_Hmc/status/855115095281725440">20 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">An interesting study of AutoStyle <a href="https://twitter.com/hashtag/Tutor?src=hash">#Tutor</a> with auto generated coding style hints by Eliane Wiese at <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a> <a href="https://t.co/UIDt3t7d13">pic.twitter.com/UIDt3t7d13</a></p>&mdash; Peter Brusilovsky (@peterpaws) <a href="https://twitter.com/peterpaws/status/855117340396199936">20 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Detecting Diligence with Online Behaviors on Intelligent Tutoring Systems

> Diligence: Working on academic tasks that are beneficial in the long-run instead of immediate incentives

Academic Diligence Task (ADT) (Galla et al., 2015)

- Study where students can either lay off or work. Surprisingly, it has predictive power on their standardized test scores and whether they will pursue 4-year college.

How to adapt it to adaptive online learning?

TL;DR: Diligence is correlated with success.

- Isn't this an old-fashioned idea?
- Is it a good idea that I'm being distracted or not?

## Epistemic Cognition: A Promising and Necessary Construct for Enriching Large-scale Online Learning Analysis

[PDF](http://delivery.acm.org/10.1145/3060000/3051462/p61-johanes.pdf?ip=192.54.222.4&id=3051462&acc=OPEN&key=4D4702B0C3E38B35%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35%2E6D218144511F3437&CFID=753159252&CFTOKEN=13181410&__acm__=1492713702_69baaafdf41d29663245076db3e00afb)

### Additional Explanatory Power for Learner States and Learning Tasks

Add some epistemic constructs in the predicting, knowledge-tracing approaches may add explanatory power.

### Additional Insight into for Learner and Environment Development

Involve demographic data in order to improve inclusion and diversity in the tasks provided online.

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">Epistemic cognition in online learning, emerging and necessary research topic! <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a> <a href="https://t.co/lFSP5gydt7">pic.twitter.com/lFSP5gydt7</a></p>&mdash; carina211 (@carina211) <a href="https://twitter.com/carina211/status/855132900899135490">20 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
