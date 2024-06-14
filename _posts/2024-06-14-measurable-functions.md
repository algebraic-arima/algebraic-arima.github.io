*In Axiomization of probability.*

# Measurable Functions

i.e. Random variables

## Notations

- $\mathcal{L}^+_{b}(\mathcal{C})$: the set of all bounded measurable functions on $\mathcal{C}$.

## Definition and Theorem of Approximation

***Definition 1.*** 设$(\Omega,\mathcal{F})$和$(E,\mathcal{E})$是测度空间，$f:\Omega\to E$是一个映射，如果对于每一个$A\in\mathcal{E}$，$f^{-1}(A)\in\mathcal{F}$，则称$f$是$\mathcal{F}/\mathcal{E}$**-可测映射**.

***Definition 2.*** 令$E=\overline{\mathbb{R}},\mathcal{E}=\mathcal{B}(\overline{\mathbb{R}})$，则称$f$为**Borel可测函数**.
<!-- into english -->

***Example 3.*** Let $\mathscr{F}$ be some collection of $f\in C(0,1)$. Then $\Phi(x)=\sup_{f\in\mathscr{F}} f$ and $\Psi(x)=\inf_{f\in\mathscr{F}} f$ is measurable.

***Proof.*** Consider $E_t={\{x:\Phi(x)>t\}}$. Then $\Phi(x_0)>t$ implies that there exists $f_{x_0}\in\mathscr{F}$ such that $f_{x_0}(x_0)>t$. Since $f$ is continuous, there exists $\delta>0$ s.t. for all $x\in B_{\delta}(x_0)$, $f_{x_0}(x)>t$. Thus $B_{\delta}(x_0)\subseteq E_t$. Hence $E_t$ is open, and $\Phi$ is measurable.
$\blacksquare$

***Example 4.*** Let $\{f_k(x)\}$ be a sequence of measurable functions over $\mathbb{R}^n$. Then $\{x:\lim_{k\to+\infty}f_k(x) \text{ exists}\}$ is measurable.

***Proof.*** Let $E=\{x:\lim_{k\to+\infty}f_k(x) \text{ exists}\}$. Then $E=\bigcap_{m=1}^{\infty}\bigcup_{k=1}^{\infty}\bigcap_{n=k}^{\infty}\bigcap_{l=k}^{\infty}\{x:|f_n(x)-f_l(x)|<\frac{1}{m}\}$, which is measurable.
$\blacksquare$

***Example 5.*** Let $\mathscr{F}$ be some collection of measurable functions. Then $\Phi(x)=\sup_{f\in\mathscr{F}} f$ and $\Psi(x)=\inf_{f\in\mathscr{F}} f$ may not be measurable.

Let $\mathscr{F}=\{\chi_{\{y\}}:y\in N\}$, where $N$ is a  **Vitali Set**. Then $\Phi(x)=\chi_N$ which is not measurable.

***Definition 6.*** $f$ is a **simple function** if $f$ is measurable and takes only finitely many values. (non-continuous r.v.)

For a simple function $f$, $f=\sum_{i=1}^n a_i\chi_{A_i}$, where $A_i$ are disjoint sets. We can prove the representation is unique.

And if all $E_i$ are measurable, then $f$ is measurable.

***Theorem 7.*** Let $f$ be a non-negative measurable function. Then there exists an increasing sequence of simple functions $\{f_n\}$ s.t. $f_n\to f$ pointwise.

***Proof.*** Let $f_n(x)=\sum_{k=0}^{n2^n-1}\frac{k}{2^{n}}\chi_{\{\frac{k}{2^{n}}\leq x < \frac{k}{2^{n+1}}\}}+n\chi_{\{f\geq n\}}$. Then $f_n\to f$ pointwise.

***Theorem 8.*** Let $f$ be a measurable function. Then there exists a sequence of simple functions $\{f_n\}$ s.t. $|f_n(x)|<|f(x)|$ and $f_n\to f$ pointwise.

In particular, if $f$ is bounded, then $f_n\to f$ uniformly.

## Convergence of Measurable Functions

***Definition 9.*** Let $f_n,f$ be measurable functions from $(\Omega,\mathcal{F},\mu)$ to $(\mathbb{R},\mathcal{B}(\mathbb{R}),m)$. Define

- $f_n\to f$ **a.e.** if there exists a zero-measure set $N$ s.t. $f_n(\omega)\rightarrow f(\omega)$ over $N^c$.
- $f_n\to f$ **a.un.** if there exists a zero-measure set $N$ s.t. $f_n(\omega)\rightrightarrows f(\omega)$ over $N^c$.
- $f_n\to f$ **in measure** if $\lim_{n\to\infty}\mu(\{|f_n(\omega)-f(\omega)|>\epsilon\})=0$ for all $\epsilon>0$.
