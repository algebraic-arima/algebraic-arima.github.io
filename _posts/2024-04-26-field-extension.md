## 域扩张

*algebraic-arima当然要学algebra啦！！*

***Lemma 1.***  $[K:F]=[K:E][E:F]$， 如果$K/E/F$是域扩张. 

若 $[K:F]$ 有限，则称$K/F$是**有限**扩张. 

### 构造

通过向域$F$中添加元素来扩张. 

设 $K/F$, $S\subseteq K$，$S$是$K$的子集，$F(S)$表示$F$和$S$生成的最小扩张. 

***Lemma 2.***
$F(S)=\{\frac{f(u_1,\dots,u_n)}{g(u_1,\dots,u_n)}: f,g\in F[x_1,\dots,x_n],g|_u\neq 0,u_i\in S\}$

若$S$有限，则称$F(S)$为$F$上的**有限生成**扩张. 

***Proof.*** 首先$RHS$是域. 

最小$\Longrightarrow$
$F(S)\subseteq RHS$；

$RHS$是域，$F\subseteq RHS$，$S\subseteq RHS$，故$F(S)\subseteq RHS$. $\blacksquare$

***Corollary 3.***
如果$\alpha\in F(S)$，存在有限子集$S_0\subseteq S$，使得$\alpha\in F(S_0)$. 

***Lemma 4.***
$F(S_1\cup S_2)=F(S_1)(S_2)=F(S_2)(S_1)$.

***Proof.*** $F(S_1\cup S_2)$ 是
包含$F$和$S_1\cup S_2$的最小域，故$F(S_1\cup S_2)\subseteq F(S_1)(S_2)$.

$F(S_1)(S_2)$ 是包含$F(S_1)$ 和 $S_2$的最小域，故$F(S_1)(S_2)\subseteq F(S_1\cup S_2)$.
$\blacksquare$

***Corollary 3*** 和 ***Lemma 4*** 说明，域扩张的构造是可交换的，
而且可以通过有限次的构造得到（?）. 
总之，域扩张可归结为单扩域. 

***Do not eat a fat man at one time***