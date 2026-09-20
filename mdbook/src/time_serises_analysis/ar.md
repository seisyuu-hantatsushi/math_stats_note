### AR過程
#### AR(1)過程
AR過程の一番単純なモデル.
\\[
	X_t = c + \phi_1 X_{t-1} + W_t \\\\
	\mathrm{E}[W_t] = 0 \\\\
	\mathrm{V}[W_t] = \sigma^2 \\\\
	\mathrm{Cov}[W_t,W_{t-s}] = 0 \\\\
	\mathrm{Cov}[X_t,W_s] = 0 \\\\
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

定常過程の場合,\\(\mathrm{E}[X\_t] = \mu\\)なので,
\\[
\begin{align} 
\mu &= c + \phi_1 \mu \\\\
\mu &= \frac{c}{1-\phi_1}
\end{align} 
\\]

弱定常過程の場合,\\(\mathrm{V}[X_t] = \gamma(0), \mathrm{Cov}[X_t,X_{t-s}] = \gamma_{|s|} = \gamma(s)\\)なので,
\\[
\begin{align}
\mathrm{V}[X_t] &= \mathrm{V}[c + \phi_1 X_{t-1} + W_t] \\\\
				&= {\phi_1}^2\mathrm{V}[X_{t-1}] + \sigma^2 \\\\
   \gamma(0) &= {\phi_1}^2\gamma(0) + \sigma^2 \\\\
   \gamma(0) &= \frac{\sigma^2}{1-{\phi_1}^2}
\end{align}
\\]
\\(\gamma(0) > 0 \\)なので,AR(1)過程が弱定常過程ならば,\\({\phi_1}^2 < 1,|\phi_1| < 1,\\)
\\[
\begin{align}
\mathrm{Cov}[X_t,X_{t-1}] &= \mathrm{Cov}[c + \phi_1 X_{t-1} + W_t,X_{t-1}] \\\\
&= \mathrm{Cov}[\phi_1 X_{t-1} + W_t,X_{t-1}] \\\\
&= \mathrm{E}[(\phi_1 X_{t-1} + W_t - \mathrm{E}[\phi_1 X_{t-1} + W_t])(X_{t-1} - \mu)] \\\\
&= \mathrm{E}[\phi_1 X_{t-1}(X_{t-1} - \mu)] \\\\
&= \mathrm{E}[(\phi_1 X_{t-1} - \phi_1\mu + \phi_1 \mu)(X_{t-1} - \mu)] \\\\
&= \phi_1\mathrm{V}[X_{t-1}] \\\\
&= \phi_1\frac{\sigma^2}{1-{\phi_1}^2}
\end{align}
\\]
\\[
\begin{align}
\mathrm{Cov}[X_t,X_{t-s}] &= \mathrm{Cov}[ X_{t-s} + \sum^{s}\_{u=1} {\phi_1}^{t-u} (W\_{u} + c),X_{t-s}] \\\\
&= {\phi_1}^s \mathrm{V}[X_{t-s}] \\\\
&= {\phi_1}^s \frac{\sigma^2}{1-{\phi_1}^2} \\\\
\end{align}
\\]
なので,
\\[\gamma(s) = {\phi_1}^s \frac{\sigma^2}{1-{\phi_1}^2}\\]
\\[\rho(s) = \frac{\gamma(s)}{\gamma(0)} = \frac{{\phi_1}^s \frac{\sigma^2}{1-{\phi_1}^2}}{\frac{\sigma^2}{1-{\phi_1}^2}} = {\phi_1}^s \\].

#### AR(2)過程
2次のAR過程のを考察する.
\\[
	X_t = c + \phi_1 X_{t-1} + \phi_2 X_{t-2} + W_t 
\\]

定常過程の場合,\\(\mathrm{E}[X\_t] = \mu\\)なので,
\\[
\begin{align}
\mathrm{E}[X\_t] &= \mathrm{E}[c + \phi_1 X\_{t-1} + \phi_2 X\_{t-2} + W_t] \\\\
&= c + \phi_1\mathrm{E}[X\_{t-1}] + \phi_2\mathrm{E}[X\_{t-2}] \\\\
\mu &= c + \phi_1\mu + \phi_2\mu \\\\
\mu &= \frac{c}{1 - \phi_1 - \phi_2}
\end{align}
\\]
ここで,\\(c=0\\)とすると,\\(\mu=0\\). なので,これは,\\(X'_t = X\_t-\mu\\)として,
\\[
	X_t-\mu = \phi_1 (X\_{t-1}-\mu) + \phi_2 (X\_{t-1}-\mu) + W_t \\\\
	X'_t = \phi_1 X'\_{t-1} + \phi_2 X'\_{t-2} + W_t \\\\
\\]
とすることをできる.\\(X'_t\\)は\\(X_t\\)の平均を0に標準化したものとみなせる.   
共分散の時間発展を考察するのは,平均を0に標準化でも同じなので,
\\[
	X_t = \phi_1 X\_{t-1} + \phi_2 X\_{t-2} + W_t \\\\
\\]
で考察を続ける.



行列で表すと,
\\[
	\begin{pmatrix}
	X_t \\\\
	X_{t-1}
	\end{pmatrix} =
	\begin{pmatrix}
	\phi_1 & \phi_2 \\\\
	1  & 0
	\end{pmatrix}
	\begin{pmatrix}
	X\_{t-1} \\\\
	X\_{t-2}
	\end{pmatrix} +
	\begin{pmatrix}
	1 \\\\
	0
	\end{pmatrix} W_t
\\]
\\[
	\boldsymbol{X}_t = 	\begin{pmatrix}
	X_t \\\\
	X\_{t-1}
	\end{pmatrix},\\;
	\mathbf{A} = \begin{pmatrix}
	\phi\_1 & \phi\_2 \\\\
	1  & 0
	\end{pmatrix},\\;
	\mathbf{B} = \begin{pmatrix}
	1 \\\\
	0
	\end{pmatrix}
\\]
として,
\\[
	\mathbf{X}_t = \mathbf{A}\mathbf{X}\_{t-1} + \mathbf{B}W_t
\\]
と表せる.
