## ガンマ関数

**ガンマ関数**(gamma function)は階乗の一般化である.
まず,
\\[
	\Gamma(n) = (n-1)!
\\]
と定義する.
となると,
\\[
	\Gamma(n+1) = n! = n(n-1)! = n\Gamma(n)
\\]
となり,整数の階乗と同じ性質となる.
\\(x\\)は整数と限らないとした時,\\(\Gamma(x)\\)がどうなるかを考えてみる.

### 無限積表示
\\[
    \begin{align}
	(n+x)! &= (n+x)(n+x-1)(n+x-2) \cdots (n+x-x+1)(n+x-x)(n+x-x-1)(n+x-x-2) \cdots 2 \cdot 1 \\\\
	       &= (n+x)(n+x-1)(n+x-2)\cdots (n+1) n! \\\\
		   &= \frac{n^x(n+x)(n+x-1)(n+x-2)\cdots (n+1) n!}{n^x} \\\\
		   &= n!n^x\left(1+\frac{x}{n}\right)\left(1+\frac{x-1}{n}\right)\left(1+\frac{x-2}{n}\right)\cdots\left(1+\frac{1}{n}\right)\\\\
	\end{align}
\\]
また,
\\[
    \begin{align}
	(n+x)! &= (x+n)(x+n-1)(x+n-2)\cdots(x+n-n+1)(x+n-n)(x+n-n-1)(x+n-n-2)\cdots 2 \cdot 1 \\\\
	&= (n+x)(n+x-1)(n+x-2)\cdots(x+1)x(x-1)!
	\end{align}
\\]
から,
\\[
	(n+x)(n+x-1)(n+x-2)\cdots(x+1)x(x-1)! = n!n^x\left(1+\frac{x}{n}\right)\left(1+\frac{x-1}{n}\right)\left(1+\frac{x-2}{n}\right)\cdots\left(1+\frac{1}{n}\right)\\\\
	(x-1)! = \frac{n!n^x}{(n+x)(n+x-1)(n+x-2)\cdots(x+1)x}\left(1+\frac{x}{n}\right)\left(1+\frac{x-1}{n}\right)\left(1+\frac{x-2}{n}\right)\cdots\left(1+\frac{1}{n}\right)
\\]
改めて上式で,\\(n \to \infty\\)とした時,
\\[
(x-1)! = \lim_{n \to \infty} \frac{n!n^x}{(n+x)(n+x-1)(n+x-2)\cdots(x+1)x} \\\\
\Gamma(x) = \lim_{n \to \infty} \frac{n!n^x}{\prod ^n _{i=0} (x+i)}
\\]
となる.

### 積分表示
\\[
	\Gamma(x) = \int ^{\infty} _{0} t^{x-1} e^{-t} dt
\\]
はガンマ関数の無限積表示と同値である.

- 証明  
\\[
\begin{align}
	\Gamma(x) &= \int ^{\infty} _{0} t^{x-1} e^{-t} dt \\\\
	          &= \lim _{n \to \infty} \int ^{n} _{0} t^{x-1} e^{-t} dt \\\\
	          &= \lim _{n \to \infty} \int ^{n} _{0} t^{x-1} \left(1 - \frac{t}{n} \right)^n dt
\end{align}
\\]
\\(\displaystyle u=\frac{t}{n}\\)と変数変換すると,
\\[
\begin{align}
	\lim _{n \to \infty} \int ^{n} _{0} t^{x-1} \left(1 - \frac{t}{n} \right)^n dt &= \lim _{n \to \infty} \int ^{1} _{0} (un)^{x-1} (1 - u)^n n du \\\\
	&= \lim _{n \to \infty} n^x \int ^{1} _{0} u^{x-1} (1 - u)^n du \\\\
	&= \lim _{n \to \infty} n^x \int ^{1} _{0} \left( \frac{1}{x} u^x \right)' (1 - u)^n du \\\\
	&= \lim _{n \to \infty} n^x \left\\{ \int ^{1} _{0} \left( \frac{1}{x} u^x \right)' (1 - u)^n du \right\\} \\\\
	&= \lim _{n \to \infty} n^x \left\\{ \left[ \frac{1}{x} u^x (1 - u)^n \right] ^1 _0 + \int ^{1} _{0} \frac{u^x}{x} n(1 - u)^{n-1} du \right\\} \\\\
	&= \lim _{n \to \infty} n^x \left\\{  \frac{n}{x} \int ^{1} _{0} \left( \frac{u^{x+1}}{x+1} \right)' (1 - u)^{n-1} du \right\\} \\\\
	&= \lim _{n \to \infty} n^x \frac{n}{x} \left\\{ \int ^{1} _{0} \left( \frac{u^{x+1}}{x+1} \right)' (1 - u)^{n-1} du \right\\} \\\\
	&= \lim _{n \to \infty} n^x \frac{n}{x} \left\\{ \left[\frac{u^{x+1}}{x+1} (1 - u)^{n-1} \right] ^1 _0 + \int ^{1} _{0} \frac{u^{x+1}}{x+1} (n-1)(1 - u)^{n-2} du \right\\} \\\\
	&= \lim _{n \to \infty} n^x \frac{n(n-1)}{x(x+1)} \left\\{\int ^{1} _{0} u^{x+1} (1 - u)^{n-2} du \right\\} \\\\
	&\vdots \\\\
	&= \lim _{n \to \infty} n^x \frac{n!}{\prod ^{n-1} _{i=0} (x+i)} \left\\{\int ^{1} _{0} u^{x+n-1} du \right\\} \\\\
	&= \lim _{n \to \infty} n^x \frac{n!}{\prod ^{n-1} _{i=0} (x+i)} \left[ \frac{1}{x+n} u^{x+n}\right] ^1 _0 \\\\
	&= \lim _{n \to \infty} \frac{n!n^x}{\prod ^{n} _{i=0} (x+i)}
\end{align}
\\]



