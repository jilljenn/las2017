# Adaptive testing models

[Go back to main page](/las2017)

Name | Dimensions | Parameters
--- | --- | ---
IRT | K = 1 | Auto
MIRT | K \leq 5 | Auto
SPARFA | K \leq 10 | Auto
--- | --- | ---
DINA | K \leq 20 | Manual
KST | K \leq 50 | Manual
Bandits | K \leq 20 | Manual

## Latent Trait Models

Summative models.

### Item Response Theory (IRT)

- Student $i$ has ability $\theta_i$
- Question $i$ has difficulty $d_j$

$$ Pr(\textsf{correct}_{ij}) = \Phi(\theta_i - d_j) $$

where $Phi : x \mapsto 1/(1 + e^{-x})$ is the logistic function.

### Multidimensional IRT

- $K$ is the number of dimensions measured.
- Student $i$ has level $\theta_{ik}$ over dimension $k$.
- Question $j$ has discrimination $d_{jk}$ over dimension $k$ and easiness (bias) $\delta_j$.

$$ Pr(\textsf{correct}_{ij}) = \Phi\left(\sum_{k = 1}^K \theta_{ik} d_{jk} + \delta_j\right) = \Phi\left(\boldsymbol{\theta_i} \cdot \boldsymbol{d_j} + \delta_j\right) $$

- $\theta_{ik}$ is student $i$'s level along KC $k$;
- $d_{jk}$ is the discrimination parameter of question $j$ over KC $k$;
- $\delta_j$ is the easiness (bias) of question $j$.

### SPARFA

$$ Pr(\textsf{correct}_{ij}) = \Phi\left(\sum_{k = 1}^K \theta_{ik} d_{jk} + \delta_j\right) = \Phi\left(\boldsymbol{\theta_i} \cdot \boldsymbol{d_j} + \delta_j\right) $$

Same as MIRT, but:

- $d_{jk} \geq 0$ for every question $j$ and KC $k$;
- $d_{jk} = 0$ for most of them ($D$ matrix is sparse).

## Knowledge-based Models

Formative models.

### DINA

$$ \Pr(\textsf{correct}_{ij}) \triangleq \left\{\begin{array}{cl}
1 - s_j & \text{if } \textsf{student}_i \text{ masters every requirement of } \textsf{question}_j\\
g_j & \text{otherwise.}
\end{array}\right. $$

### Attribute Hierarchy Model & Knowledge Space Theory

### GenMA

$$ Pr(\textsf{correct}_{ij}) = \Phi\left(\sum_{k = 1}^K \theta_{ik} q_{jk} d_{jk} + \delta_j\right) $$

- $K$ is the number of knowledge components involved.
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
