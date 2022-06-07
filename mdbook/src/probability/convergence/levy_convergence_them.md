## Levyの収束定理
Levyの連続性定理とも言う.

### Levyの収束定理
確率変数列\\(\\{X _n \\} _{n \in \mathbb{N} _+} \\)を用意して,
分布関数列\\(\\{F _{X _n}\\} _{n \in \mathbb{N} _+} \\)に対応する特性関数列を
\\( \\{ \varphi _{X _n} \\} _{n \in \mathbb{N} _+} \\)とする.

\\[
	\varphi _{X _n}(t) = E[e^{itX_n}] = \int^{\infty} _{-\infty} e^{itx} dF _{X _n}(x) =\int^{\infty} _{-\infty} e^{itx} f _{X _n}(x) dx
\\]
1. 確率変数\\(X _n\\)の分布収束の先が確率変数\\(X\\)であるとき,確率変数\\(X\\)に対応する特性関数を\\(\varphi\\)とすると,
   \\[
	   X _n \xrightarrow{d} X \Rightarrow \varphi _{X _n}(t) \to \varphi(t). (n \to \infty, t \in \mathbb{R})
   \\]
1. \\(\varphi: \mathbb{R} \mapsto \mathbb{C} \\)が存在して,\\(\forall t \in \mathbb{R}, \varphi_n(t) \to \varphi(t)\\;(n \to \infty)\\)で,
   \\(t=0\\)近傍で一様収束するなら,\\(\varphi\\)を確率変数\\(X\\)の特性関数とし,
   \\[
	   \varphi _{X _n}(t) \to \varphi(t). (n \to \infty) \Rightarrow X _n \xrightarrow{d} X
   \\]

- 証明  
  1. \\(g(x) = e^{itx}\\)は有界連続関数なので,Portmanteau定理により,
  \\[
	  X _n \xrightarrow{d} X \Rightarrow E[e^{itX_n}]] \to E[e^{itX}]] \\; (n \to \infty)
  \\]
  なので,題意は成立.
  1. 難しい...
