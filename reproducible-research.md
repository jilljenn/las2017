# Reproducible research

To add an entry, please tweet [@jjvie](https://twitter.com/jjvie) or [do a pull request](https://github.com/jilljenn/las2017).

## Platforms for hosting reproducible code

- [CodaLab](https://worksheets.codalab.org) made by [Percy Liang](https://cs.stanford.edu/~pliang/) (Stanford University) and [Microsoft Research](https://www.microsoft.com/en-us/research/project/codalab/)

From Tum, a Stanford student:

> To use GPUs or perform large amounts of computation, you can [run your own worker](https://github.com/codalab/codalab-worksheets/wiki/Execution#running-your-own-worker) or even [set up your own CodaLab server](https://github.com/codalab/codalab-worksheets/wiki/Server-Setup).

<!-- <blockquote class="twitter-tweet" data-lang="fr"><p lang="en" dir="ltr">Talking about reproducible research at <a href="https://twitter.com/hashtag/las17ed?src=hash">#las17ed</a> → the platform built by Stanford University and Microsoft Research: <a href="https://t.co/lAaCfklChD">https://t.co/lAaCfklChD</a></p>&mdash; Jill-Jênn Vie (@jjvie) <a href="https://twitter.com/jjvie/status/855153523528523776">20 avril 2017</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script> -->

## Data challenges for academia

- [CodeOcean](https://github.com/openHPI/codeocean), the Ruby platform driven by the [Hasso Platner Institute](https://en.wikipedia.org/wiki/Hasso_Plattner_Institute), Germany
- [University of Big Data](http://universityofbigdata.net/?lang=en), the Python platform driven by Kyoto University, Japan
- Of course, Kaggle exists… but… <small>how to say………</small> <small><small>Google acquired it.</small></small>

## Tools for remote execution of code

So you can make data challenges yourself!

- [Camisole](https://camisole.prologin.org), a Python package that abstracts the complex stuff into an API simple to use, made by [Prologin](https://prologin.org) (non-profit student-driven organization that promotes CS through a programming contest) and based on [isolate](https://github.com/ioi/isolate) (used by IOI)
- [Taskgrader](https://github.com/France-ioi/taskgrader), a Python package that abstracts the complex stuff into a wrapper simple to use, made by [France-ioi](http://www.france-ioi.org) (take that, war of standards)

Those are Docker free, but may require Linux: ([isolate](https://github.com/ioi/isolate) can be seen as a light version of Docker, based on [chroot](https://en.wikipedia.org/wiki/Chroot).
