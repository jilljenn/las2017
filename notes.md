# Notes from Learning at Scale

[Go back to main page](/las2017)

[See the proceedings on ACM](http://dl.acm.org/citation.cfm?id=3051457&preflayout=flat)

## Robust Evaluation Matrix

Doroudi et al.
A/B testing?
Instructional policy : flowchart

Calibrate a best policy for one student model
=> Might not be good for other models
! Not try to be good everywhere, otherwise overfitting

## Visual approach

Design space unlimited
Solution space underdefined

Compromise between top-down expert et bottom-up data-driven

Their tool, **tempr** is [on GitHub](https://github.com/fratamico/Tempr---A-visual-knowledge-engineering-tool).

Allows to merge actions and see the amount of these buckets of actions in the logs over time (for high learners and low learners), potentially to verify theories.

## Next Step Recommendation

Navigational efficiency: jump directly to resource

Use LSTMs (certain type of recurrent neural networks) to model the behavior of a student given their history, and predict the next page on which they will spent more time (in order to recommend it to them).

Do not only train on certified students, in order to get more data.

- Baseline (next lesson): 52%
- n-gram: 61%
- LSTM: 64%

They had to log the visited pages via JavaScript.

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
