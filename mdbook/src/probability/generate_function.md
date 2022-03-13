# 確率母関数・積率母関数
確率関数,モーメントを生成できる関数,母関数というものを考える.

## 確率母関数
\\[
\begin{align}
	G_X(t) &= E[t^X] \\\\
	&= \int _\Omega t^{X(\omega)}P(d\omega) \\\\
	&= \int ^{\infty} _{-\infty} t^x dP(x) \\\\
	&= \int ^{\infty} _{-\infty} t^x f_X(x) dx
\end{align}
\\]

## 積率母関数
\\[
\begin{align}
	M_X(t) &= E[e^{tX}] \\\\
	&= \int _\Omega e^{tX(\omega)} P(d\omega) \\\\
	&= \int ^{\infty} _{-\infty} e^{tx} dP(x) \\\\
	&= \int ^{\infty} _{-\infty} e^{tx} f_X(x) dx
\end{align}
\\]
