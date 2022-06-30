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
