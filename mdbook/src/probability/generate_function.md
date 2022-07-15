## 確率母関数・積率母関数
確率関数,モーメントを生成できる関数,母関数というものを考える.

### 確率母関数
\\[
\begin{align}
	G_X(t) &= E[t^X] \\\\
	&= \int _\Omega t^{X(\omega)}P(d\omega) \\\\
	&= \int ^{\infty} _{-\infty} t^x dP(x) \\\\
	&= \int ^{\infty} _{-\infty} t^x f_X(x) dx
\end{align}
\\]

### 積率母関数
\\[
\begin{align}
	M_X(t) &= E[e^{tX}] \\\\
	&= \int _\Omega e^{tX(\omega)} P(d\omega) \\\\
	&= \int ^{\infty} _{-\infty} e^{tx} dP(x) \\\\
	&= \int ^{\infty} _{-\infty} e^{tx} f_X(x) dx
\end{align}
\\]
積率母関数は\\(t\\)に関して\\(k\\)階微分すると\\(k\\)次モーメントを得る.
\\[
	\left. \frac{d}{dt}M_X(t) \right| _{t=0} = \left. \frac{d}{dt} \int ^{\infty} _{-\infty} e^{tx} f_X(x) dx \right| _{t=0} = \int ^{\infty} _{-\infty} x f_X(x) dx = E[X] \\\\
	\left. \frac{d^2}{dt^2}M_X(t) \right| _{t=0} = \left. \frac{d^2}{dt^2} \int ^{\infty} _{-\infty} e^{tx} f_X(x) dx \right| _{t=0} = \int ^{\infty} _{-\infty} x^2 f_X(x) dx = E[X^2] \\\\
	\left. \frac{d^k}{dt^k}M_X(t) \right| _{t=0} = \left. \frac{d^k}{dt^k} \int ^{\infty} _{-\infty} e^{tx} f_X(x) dx \right| _{t=0} = \int ^{\infty} _{-\infty} x^k f_X(x) dx = E[X^k]
\\]
