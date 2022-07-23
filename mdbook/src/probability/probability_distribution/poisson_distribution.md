## ポアソン分布
二項分布\\(P(X:n,p) = { _n C _x } p^x (1-p)^{n-x}\\)を\\(np=\lambda\\)として,
\\(n \to \infty\\)とすると,

\\[
\begin{align}
	\lim _{n \to \infty} P(X = x) &= \lim _{n \to \infty} { _n C _x } p^x (1-p)^{n-x} \\\\
	&= \lim _{n \to \infty} \frac{n!}{k!(n-x)!} p^x (1-p)^{n-x} \\\\
	&= \lim _{n \to \infty} \frac{n!}{k!(n-x)!} \left(\frac{\lambda}{n}\right)^x \left(1-\frac{\lambda}{n}\right)^{n-x} \\\\
	&= \lim _{n \to \infty} \frac{n!}{k!(n-x)!} \left(\frac{\lambda^x}{n^x}\right) \left(1-\frac{\lambda}{n}\right)^{n-x} \\\\
	&= \lim _{n \to \infty} \frac{n!}{(n-x)!n^x} \left(\frac{\lambda^x}{k!}\right) \left(1-\frac{\lambda}{n}\right)^n \left(1-\frac{\lambda}{n}\right)^{-x} \\\\
	&= \lim _{n \to \infty} \frac{n(n-1)(n-2)\cdots(n-(x-1))}{n^x} \left(\frac{\lambda^x}{x!}\right) \left(1-\frac{\lambda}{n}\right)^n \left(1-\frac{\lambda}{n}\right)^{-x} \\\\
	&= \lim _{n \to \infty} \frac{n(n-1)(n-2)\cdots(n-(x-1))}{n^x} \left(\frac{\lambda^x}{x!}\right) \left(1-\frac{\lambda}{n}\right)^n \left(1-\frac{\lambda}{n}\right)^{-x} \\\\
	&= \lim _{n \to \infty} \left(1 + o(n^{-1})\right) \left(\frac{\lambda^x}{x!}\right) \left(1-\frac{\lambda}{n}\right)^n \left(1-\frac{\lambda}{n}\right)^{-x} \\\\
	&= \left(\frac{\lambda^x}{x!}\right) e^{-\lambda}
\end{align}
\\]

改めて,\\(\lambda\\)を母数とする以下の確率分布を**ポアソン分布**(poisson distribution)という.
\\[
	\mathcal{Po}(\lambda) = P(X:\lambda) = \left(\frac{\lambda^x}{x!}\right) e^{-\lambda}
\\]
上記の確率は,所定時間内に平均\\(\lambda\\)回発生する事象が,\\(x\\)回発生する確率に相当する.

### 平均
まず,\\(e^{-\lambda}\\)のマクローリン展開から,
\\[
	e^{\lambda} = 1 + \frac{1}{2}\lambda + \frac{1}{3!}\lambda^2 + \cdots = \sum^{\infty} _{n = 0} \frac{\lambda^n}{n!} 
\\]
より,
\\[
	\sum ^{\infty} _{x=0} \left(\frac{\lambda^x}{x!}\right) e^{-\lambda} = \frac{\sum ^{\infty} _{x=0} \frac{\lambda^x}{x!}}{\sum^{\infty} _{n = 0} \frac{\lambda^n}{n!} } = 1
\\]

\\[
\begin{align}
	E[X] &= \sum ^{\infty} _{x=0} x \left(\frac{\lambda^x}{x!}\right) e^{-\lambda} \\\\
	&= \lambda \sum ^{\infty} _{x=1} \left(\frac{\lambda^{x-1}}{(x-1)!}\right) e^{-\lambda} \\\\
	&= \lambda
\end{align}
\\]

### 分散
\\[
\begin{align}
	E[X(X-1)] &= \sum ^{\infty} _{x=0} x(x-1) \left(\frac{\lambda^x}{x!}\right) e^{-\lambda} \\\\
	&= \lambda^2 \sum ^{\infty} _{x=2}  \left( \frac{\lambda^{x-2}}{(x-2)!} \right) e^{-\lambda} = \lambda^2
\end{align}
\\]

#### 確率母関数
\\[
\begin{align}
	G_X(t) &= E[t^X] \\\\
	&= \sum ^{n} _{x=0} t^x \left(\frac{\lambda^x}{x!}\right) e^{-\lambda} \\\\
	&= \sum ^{n} _{x=0} \left(\frac{(t\lambda)^x}{x!}\right) e^{-\lambda} \\\\
	&= e^{(t\lambda)}e^{-\lambda} \\\\
	&= e^{(t-1)\lambda}
\end{align}
\\]

### 積率母関数
\\[
\begin{align}
	M_X(t) &= E[e^{Xt}] \\\\
	&= \sum ^{n} _{x=0} e^{xt} \left(\frac{\lambda^x}{x!}\right) e^{-\lambda} \\\\
	&= \sum ^{n} _{x=0} \left(\frac{(e^{t}\lambda)^x}{x!}\right) e^{-\lambda} \\\\
	&= e^{(e^{t}\lambda)} e^{-\lambda} \\\\
	&= e^{(e^{t}-1)\lambda}
\end{align}
\\]

### 特性関数
\\[
\begin{align}
	\varphi_X(t) &= E[e^{iXt}] \\\\
	&= e^{(e^{it}-1)\lambda}
\end{align}
\\]
