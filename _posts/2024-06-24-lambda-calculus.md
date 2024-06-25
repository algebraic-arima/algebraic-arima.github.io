---
title: 'Lambda Terms$'
date: 2024-06-14
permalink: /posts/2024/06/lambda-terms/
tags:
  - type theory
---

# Lambda Terms

An intuitive thought: for $x$, $x^2+1$ can be a function or merely a number.

Thus we distinguish them, by denoting the function by $\lambda x.x^2+1$.

***Definition 1.*** Let $V$ be an infinite variable set $\{x,y,z,\dots\}$, $\Lambda$ be a set of Lambda terms.

(1) If $u\in V$, then $u\in \Lambda$. 

(2)(juxtaposition for application) If $M,N\in \Lambda$, then $(M\;N)\in\Lambda$.

(3) If $x\in V$, $N\in \Lambda$, then $(\lambda x.N)\in\Lambda$.

Or in short, $\Lambda=V|(\Lambda\Lambda)|(\lambda V.\Lambda)$.

***Definition 2.*** Subterms.

(1) $\text{Sub}(x)=\{x\}$, for $x\in V$

(2) $\text{Sub}(M\;N)=\text{Sub}(M)\cup\text{Sub}(N)\cup\{(M\;N)\}$

(3) $\text{Sub}(\lambda x.M)=\text{Sub}(M)\cup\{(\lambda x.M)\}$

proper: sub but not $\equiv$.

**Reflexivity and Transitivity**

$\equiv$ says that two $\lambda$-terms are exactly the same.

Tree of $(y(\lambda x.(xz)))$

(a:application,l:lambda)

```
  y
 /
a     x
 \   /
  l-a
     \
      z
   

```

***Notation 3.***

- It's recommended that you should not omit the parentheses.
- Application is left-associative, with $MNL$ denoting $((MN)L)$
- Abstruction is right-associative, with $\lambda xy.M$ denoting $(\lambda x.(\lambda y.M))$
- Application takes precedence over abstraction, with $\lambda x. MN$ denoting $\lambda x.(MN)$


