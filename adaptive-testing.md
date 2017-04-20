# Adaptive testing models

[Go back to main page](/las2017)

Name | Dimensions | Calibration | Suitable for cold-start | Number of parameters estimated per question
--- | --- | ---
IRT | $K = 1$ | Auto | No | $n$
MIRT | $K \leq 5$ | Auto | No | $(K + 1)n$
SPARFA | $K \leq 10$ | Auto | No | $(k + 1)n$
--- | --- | ---
DINA | $K \leq 20$ | Manual | Yes | $2n$
KST | $K \leq 50$ | Manual | Yes | 0
Bandits | $K \leq 20$ | Manual | Yes | 0

- $n$ is the number of questions
- $K$ the number of dimensions / knowledge components considered by the model
- $k$ is the rough number of nonzero elements per row (in the question parameters)

## Latent Trait Models

**Summative** models.

### Item Response Theory (IRT)

- Student $i$ has ability $\theta_i$.
- Question $i$ has difficulty $d_j$.

$$ Pr(\textsf{correct}_{ij}) = \Phi(\theta_i - d_j) $$

where $Phi : x \mapsto 1/(1 + e^{-x})$ is the logistic function.

### Multidimensional IRT

- $K$ is the number of dimensions measured.
- Student $i$ has level $\theta_{ik}$ over dimensions $k = 1, \ldots, K$.
- Question $j$ has discrimination $d_{jk}$ over dimensions $k = 1, \ldots, K$ and easiness (bias) $\delta_j$.

$$ Pr(\textsf{correct}_{ij}) = \Phi\left(\sum_{k = 1}^K \theta_{ik} d_{jk} + \delta_j\right) = \Phi\left(\boldsymbol{\theta_i} \cdot \boldsymbol{d_j} + \delta_j\right) $$

### SPARFA

Sparse Factor Analysis.

$$ Pr(\textsf{correct}_{ij}) = \Phi\left(\sum_{k = 1}^K \theta_{ik} d_{jk} + \delta_j\right) = \Phi\left(\boldsymbol{\theta_i} \cdot \boldsymbol{d_j} + \delta_j\right) $$

Same as MIRT, but:

- $d_{jk} \geq 0$ for every question $j$ and dimension $k$;
- $d_{jk} = 0$ for most of them ($D$ matrix is sparse).

## Knowledge-based Models

**Formative** models.

### DINA

- Knowledge components are $1, \ldots, K$.
- Student $i$ has knowledge $\in \{0, 1}^K$.
- Question $j$ has requirements $\in \{0, 1}^K$ and slip and guess parameters $s_j$ and $g_j$.

$$ \Pr(\textsf{correct}_{ij}) = \left\{\begin{array}{cl}
1 - s_j & \text{if student $i$ masters every requirement of question $j$}\\
g_j & \text{otherwise.}
\end{array}\right. $$

### Attribute Hierarchy Model & Knowledge Space Theory

Knowledge components are linked in a graph.  
$u \rightarrow v$ means $u$ has to be mastered before $v$.

### GenMA

- Knowledge components $1, \ldots, K$.
- Student $i$

$$ Pr(\textsf{correct}_{ij}) = \Phi\left(\sum_{k = 1}^K \theta_{ik} q_{jk} d_{jk} + \delta_j\right) $$

- $K$ is the number of knowledge components (KC) involved.
- $\theta_{ik}$ is student $i$'s level along KC $k$;
- $q_{jk}$ the $(j, k)$ element of the q-matrix that is 1 if KC $k$ is involved in the resolution of question $j$, 0 otherwise;
- $d_{jk}$ is the discrimination parameter of question $j$ over KC $k$;
- $\delta_j$ is the easiness (bias) of question $j$.

<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
