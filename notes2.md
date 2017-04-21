# Notes from Learning at Scale - Day 2

[Go back to main page](/las2017)

[Go to Day 1](/las2017/notes)

[See the proceedings on ACM](http://dl.acm.org/citation.cfm?id=3051457&preflayout=flat)

## Scaling expert feedback

Question: Why is a college endorsement valuable?

## Gradescope: a fast, flexible, and fair system for scalable assessment of handwritten work

[PDF](http://delivery.acm.org/10.1145/3060000/3051466/p81-singh.pdf?ip=192.54.222.4&id=3051466&acc=OPEN&key=4D4702B0C3E38B35%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35%2E6D218144511F3437&CFID=753159252&CFTOKEN=13181410&__acm__=1492782640_17f1c82ffe7a6611275667a15a74aedd)

Grading parties at CS 50 at berkeley: too long.

Their system Gradescope has been used by:

- 250 schools
- 3000 courses
- 18M pages

They scanned 1400 exams in 2 hours xD

- Does it make grading more fair? — Strongly agree.
- Does it make grading more enjoyable? — Agree

<blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">Awesome grading tool <a href="https://twitter.com/gradescope">@Gradescope</a>:<br>&lt;Me&gt; I told you. <a href="https://twitter.com/UCBerkeley">@UCBerkeley</a> is the future.<br>&lt;Advisor&gt; No. It&#39;s the present. We are prehistory. <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a> <a href="https://t.co/C1DrbFlTvs">pic.twitter.com/C1DrbFlTvs</a></p>&mdash; Jill-Jênn Vie (@jjvie) <a href="https://twitter.com/jjvie/status/855417098230788097">21 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<iframe src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2Fjilljenn%2Fposts%2F10155244442548844&width=500" width="500" height="542" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true"></iframe>

## Writing Reusable Code Feedback at Scale with Mixed-Initiative Program Synthesis

The goal is to correct many programming assignments at the same time, through test cases and teacher hints.

Program synthesis relies in learning code transformations from pairs of incorrect and correct submissions. (Kind of regexp between syntactic trees?)

- They diff between correct and incorrect submissions
- Cluster the patches
- Ask the teacher to rate them
- Propagate to other submissions

Students can receive patches to their solution labelled with hints.

(Not tested yet on large-scale classes?)

### Preventing Keystroke Based Identification in Open Data Sets

University of Helsinki.

They record the timestamps of keystrokes, and would like to open the data anonymously. Unfortunately, this is enough to recover the identify of the Top 10. (Creep.)

Idea: bucketing or roughly rounding the timestamps according to some time window.

Surprise: short time window anonymizes; average time window does NOT anonymize; big time window anonymizes again.

Hypothesis: the peak distribution over delay between keystrokes may explain this behavior. A middle threshold of time window kills the blur.

### Do performance trends suggest wide-spread collaborative cheating on asynchronous exams?

University of Illinois have a Computer-Based Testing Facility where students can spend exams asynchronously (over 4 days).

Problems are randomly parametrized in the exercises, but it might not be enough to prevent cheating.

Collaborative cheating may still be possible.

#### Dataset

- 93 exams
- 29492 exam records

- Most of students choose the last day for exam
- But their performance is lower in average