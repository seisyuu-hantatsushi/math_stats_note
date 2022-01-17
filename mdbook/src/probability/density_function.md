# 確率密度関数

## 累積分布関数
\\[
	F_X(x) := P(X \leq x) = P(\\{\omega|X(\omega) \leq x\\})
\\]
を**累積分布関数**と言う.定義の通り,観測値が\\(x\\)以下である事象が発生する確率を得ることができる関数である.
任意の関数\\(F(x)\\)が累積分布関数になるための必要十分条件は,
以下の3つの条件が成立することである.
1. \\(\lim_{x \to -\infty} F(x) = 0, \\; \lim_{x \to \infty} F(x) = 1\\)
1. \\( \forall x_1, \forall x_2, x_1 < x_2 \to F(x_1) \leq F(x_2) \\)
1. \\(\lim_{x \to a+0} F(x) = F(a) \\)

2は非減少関数であること,3は関数が右連続関数であることを示す.
累積分布関数の定義より,
\\[
\begin{align}
P(a < X \leq b) &= P(\\{X \leq b\\} \backslash \\{a \leq X\\}) \\\\
&= P(\\{X \leq b\\}) - P(\\{a \leq X\\}) \\\\
&= F_X(b) - F_X(a) \\\\
&  \\\\
P(a < X) &= P(\\{\omega | a < X(\omega) \\}) \\\\
&= P(\\{\omega | X(\omega) \leq a \\}^c) \\\\
&= 1 - P(X \geq a) \\\\
&= 1 - F_X(a)
\end{align}
\\]

## 確率密度関数
累積分布関数の\\(x\\)での変化量を得ることができると,積分することにより任意の事象に対する確率が得られる.

\\[
\begin{align}
\frac{dP(x)}{dx} &= \lim _ {dx \to 0} \frac{P(\\{\omega| X(\omega) < x+dx\\})- P(\\{\omega| X(\omega) < x\\}) }{dx} \\\\
&= \lim _ {dx \to 0} \frac{F_X(x+dx) - F_X(x)}{dx} \\\\
&= \frac{dF_X(x)}{dx}
\end{align}
\\]

\\( F_X(x) \\)が微分可能ならば\\( \frac{dF_X(x)}{dx} = f_X(x) \\)として,\\(f_X(x)\\)を**確率密度関数**と言う.

定義から,
\\[
\begin{align}
P(a < X \leq b) &= F_X(b) - F_X(a) \\\\
	&= \int^b_{-\infty} f_X(x)dx - \int^a_{-\infty} f_X(x)dx \\\\
	&= \int^b_{a} f_X(x)dx \\\\
	& \\\\
	f(x) &\geq 0 \\\\
	\int^{\infty}_{-\infty} f_X(x) dx &= 1
\end{align}
\\]

## 離散的確率変数

## 確率質量関数
