## 二項分布
### ベルヌーイ分布
\\(p\\)の確率で興味がある事象,\\(1-p\\)の確率で興味がない事象が発生する試行をベルヌーイ試行(Bernoulli trial)という.
この確率関数は,\\(x=1\\)を興味のある事象,\\(x=0\\)を興味のない事象とすると,この確率は
\\[
P(X=x:p) = \left\\{\begin{array}{ll}
p & (x = 1) \\\\
1-p & (x = 0) \\\\
\end{array}
\right.
\\]
と表される.この確率密度関数は,
\\[
	f_X(x) = p^x (1-p)^x, \qquad x=0,1 \quad 0 \leq p \leq 1
\\]
であり,\\(\mathcal{Be}(p)\\)と表す.
#### 平均
\\[
	E[X] = \int_{\Omega} x f_X(x) dx = p
\\]

#### 分散
\\[
\begin{align}
	{\rm var}(X) &= E[(X-\mu)^2] = E[X^2] - E[X]^2 = \int_{\Omega} x^2 f_X(x) dx - p^2 \\\\
	&= p - p^2 = p(1-p)
\end{align}
\\]

#### 積率母関数
\\[
\begin{align}
	M_X(t) &= E[e^{tX}] =\int_{\Omega} e^{tx} f_X(x) dx \\\\
	&= (1-p) + pe^t
\end{align}
\\]

#### 特性関数
\\[
\begin{align}
	\varphi_X(t) &= E[e^{itX}] =\int_{\Omega} e^{itx} f_X(x) dx \\\\
	&= (1-p) + pe^{it}
\end{align}
\\]

### 二項分布
ベルヌーイ試行を独立に\\(n\\)回行ったときに,"成功"の回数を事象とすると,
その分布を**二項分布**(binomial distribution)という.
まず単純に,\\(n\\)回の試行で最初の\\(k\\)回が成功する確率は,
\\(i\\)回目に成功となる事象を\\(A_i\\)とすると,
\\[
	P(A _1 \cap A _2 \cap \cdots \cap A _k \cap {A _{k+1}}^c \cap \cdots \cap {A _n}^c) = \\\\
	P(A _1)P(A _2) \cdots P(A _k) P({A _{k+1}}^c) \cdots P({A _n}^c) = p^k (1-p)^{n-k}
\\]

\\(n\\)回の試行で\\(k\\)回の成功が含まれる場合の数は,
\\[
	_n C _k = \left(  \begin{array}{l}
		n \\\\
		k
	\end{array} \right) = \frac{n!}{k!(n-k)!}
\\]
となり,\\(x\\)回の成功が発生する確率は,
\\[
	P(X) = { _n C _x } p^x (1-p)^{n-x}
\\]
二項分布のパラメータは,\\(n,p\\)なので,
\\[
	P(X:n,p) = { _n C _x } p^x (1-p)^{n-x}
\\]
と書き,\\(\mathcal{Bin}(n,p)\\)と表す.

#### 平均
\\[
\begin{align}
	E[X] &= \sum^{n}_{x=0} x \\{  _n C _k  p^x (1-p)^{n-x} \\} \\\\
	&= \sum ^{n} _{x=0} x \frac{n!}{x!(n-x)!} p^x (1-p)^{n-x} \\\\
	&= \sum ^{n} _{x=0} \frac{n!}{(x-1)!(n-x)!} p^x (1-p)^{n-x} \\\\
	&= \sum ^{n} _{x=0} \frac{n(n-1)!}{(x-1)!(n-1-(x-1))!} p^x (1-p)^{n-x} \\\\
	&= n \sum ^{n-1} _{x=0} { _{n-1} C _{x-1}} p^x (1-p)^{n-x} \\\\
	&= n p \sum ^{n-1} _{x=0} { _{n-1} C _{x-1}} p^{x-1} (1-p)^{n-1-(x-1)} \\\\
	&= n p
\end{align}
\\]

#### 分散
\begin{align}
	E[X(X-1)] &= \sum^{n}_{x=0} x(x-1) { _n C _x } p^x (1-p)^{n-x} \\\\
	&= \sum ^{n} _{x=0} (x-1) \frac{n(n-1)!}{(x-1)!(n-1-(x-1))!} p^x (1-p)^{n-x} \\\\
	&= \sum ^{n} _{x=0} \frac{n(n-1)!}{(x-2)!(n-1-(x-1))!} p^x (1-p)^{n-x} \\\\
	&= \sum ^{n} _{x=0} \frac{n(n-1)(n-2)!}{(x-2)!(n-2-(x-2))!} p^2 p^{x-2} (1-p)^{n-2-(x-2)} \\\\
	&= n(n-1)p^2 \sum ^{n-2} _{x=0} \frac{(n-2)!}{(x-2)!(n-2-(x-2))!} p^{x-2} (1-p)^{n-2-(x-2)} \\\\
	&= n(n-1)p^2
\end{align}
\\[
	E[X(X-1)] = E[X^2] - E[X] = n(n-1)p^2
\\]
	から
\\[
	\begin{align}
		{\rm var}(X) &= E[X^2] - E[X]^2 = E[X^2] - E[X] + E[X] - E[X]^2 \\\\
		& = n(n-1)p^2 + np - n^2p^2 \\\\
		& = n^2p^2 -np^2 + np - n^2p^2 = np(1-p)
	\end{align}
\\]

#### 確率母関数
\\[
\begin{align}
	G_X(t) &= E[t^X] \\\\
	&= \sum ^{n} _{x=0} t^x { _n C _x } p^x (1-p)^{n-x} \\\\
	&= \sum ^{n} _{x=0}  { _n C _x } (tp)^x (1-p)^{n-x} \\\\
	&= (tp + (1-p))^n
\end{align}
\\]

#### 積率母関数
\\[
\begin{align}
	M_X(t) &= E[e^{Xt}] \\\\
	&= \sum ^{n} _{x=0} e^{xt} { _n C _x } p^x (1-p)^{n-x} \\\\
	&= \sum ^{n} _{x=0}  { _n C _x } (e^tp)^x (1-p)^{n-x} \\\\
	&= (e^tp + (1-p))^n
\end{align}
\\]

#### 特性関数
\\[
\begin{align}
	\varphi_X(t) &= E[e^{iXt}] \\\\
	&= (e^{it}p + (1-p))^n
\end{align}
\\]
