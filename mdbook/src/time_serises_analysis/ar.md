### AR過程
#### AR(1)過程
AR過程の一番単純なモデル.
\\[
	X_t = c + \phi_1 X_{t-1} + W_t \\\\
	\mathrm{E}[W_t] = 0 \\\\
	\mathrm{V}[W_t] = \sigma^2 \\\\
	\mathrm{Cov}[W_t,W_{t-s}] = 0 \\\\
\\]
について考察する.
\\[
\begin{align}
	X\_t &= c + \phi_1 X_{t-1} + W_t\\\\
	&= \phi_1(c + \phi_1 X_{t-2} + W_{t-1}) + W_t + c\\\\
	&= {\phi_1}^2 X_{t-2} + \phi_1(c+W_{t-1}) + W_t + c\\\\
	&= {\phi_1}^2 (c + \phi_1 X_{t-3} + W_{t-2}) + \phi_1  (W_{t-1}+c) + W_t + c\\\\
	&= {\phi_1}^3 X_{t-3} + {\phi_1}^2 (W\_{t-2}+c) + \phi_1  (W_{t-1}+c) + W_t + c \\\\
	&= {\phi_1}^t X_{0} + \sum^{t}\_{s=1} {\phi_1}^{t-s} (W\_{s} + c)
\end{align}
\\]
なので,\\(|\phi_1| < 1\\)の時は,過去遡るほどその影響は小さくなり,
\\(\phi_1 = 1\\)の場合は,同じように影響し,
\\(|\phi_1| > 1\\)の場合は,過去遡るほど現在に影響する.

\\[
\begin{align}
\mathrm{E}[X\_t] &= {\phi_1}^t \mathrm{E}[X_{0}] + \sum^{t}\_{s=1} {\phi_1}^{t-s} \mathrm{E}[W\_{s}+c] \\\\
&= {\phi_1}^t \mathrm{E}[X_{0}] + \sum^{t}\_{s=1} {\phi_1}^{t-s}c
\end{align}
\\]