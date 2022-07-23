## 指数分布
ポアソン分布は,所定時間内に平均\\(\lambda\\)回発生する確率分布であるが,
逆に所定時間内に平均\\(\lambda\\)回発生する事象が,指定された時間内に1回事象が
発生する確率を考える.

まず,単位時間当たりに平均\\(\lambda\\)回発生する事象が発生する平均の経過時間は\\(\theta=\frac{1}{\lambda}\\)である.
時間\\(t\\)までに事象が発生する確率を\\(P(T \leq t)\\)とする.
では,時間\\(t\\)から\\(t+\Delta t\\)までに事象が発生する確率は,
\\[
P(t < T \leq t + \Delta t) = (1 - P(T \leq t))\left(\frac{\Delta t}{\theta}\right)
\\]
となる.
\\(P\\)の累積確率分布関数を\\(F_T\\)とすると,

\\[
	F _T(t + \Delta t) - F _T(t) = (1 - F _T(t))\left(\frac{\Delta t}{\theta}\right)
\\]

両辺\\(\Delta t\\)で割ると,
\\[
	\frac{F_T(t + \Delta t) - F_T(t)}{\Delta t} = (1 - F_T(t))\left(\frac{1}{\theta}\right)
\\]
\\(\Delta t \to 0 \\)の極限を取ると,
\\[
	\frac{dF_T(t)}{d t} = (1 - F_T(t))\left(\frac{1}{\theta}\right)
\\]
\\(F_T\\)の確率密度関数を\\(f_T\\)とすると,
\\[
	f_T(t) = \left(1 - \int ^{t} _{0} f_T(t) dt \right) \left(\frac{1}{\theta}\right) \tag{1}
\\]
これを,\\(t\\)で微分すると,
\\[
	\frac{df_T(t)}{dt} = \frac{- f_T(t)}{\theta}
\\]
この方程式の解は,
\\[
	f_T(t) = Ce^{-\frac{t}{\theta}}
\\]
拘束条件
\\[
	\int ^{\infty} _{0} f _T(t) dt = 1
\\]
より,
\\[
	f _T(t) = \frac{1}{\theta} e^{-\frac{t}{\theta}}
\\]
改めて,単位時間当たりに平均\\(\lambda\\)回発生する事象が,時間\\(t\\)までに発生する確率分布は
**指数分布**(exponential distribution)と呼ばれ,
\\[
	\mathcal{Ex}(\lambda) = f _T(t:\lambda) = \lambda e^{-\lambda t}
\\]
という,確率密度関数として表される.

### 平均
\\[
\begin{align}
 E[T] &= \int ^{\infty} _{0} t f _T(t) dt \\\\
 &= \int ^{\infty} _{0} t \lambda e^{-\lambda t} dt
\end{align}
\\]
\\(x=\lambda t\\)と置くと,
\\[
\begin{align}
 \int ^{\infty} _{0} t \lambda e^{-\lambda t} dt &= \int ^{\infty} _{0} x e^{-x} \frac{1}{\lambda} dx \\\\
	&= \frac{1}{\lambda} \left\\{ \int ^{\infty} _{0} x e^{-x} dx \right\\} \\\\
	&= \frac{1}{\lambda} \left\\{ \int ^{\infty} _{0} x (-e^{-x})' dx \right\\} \\\\
	&= \frac{1}{\lambda} \left\\{ \left[ -xe^{-x} \right] ^{\infty} _{0} - \int ^{\infty} _{0} (-e^{-x}) dx \right\\} \\\\
	&= \frac{1}{\lambda} \left\\{ \left[ -xe^{-x} \right] ^{\infty} _{0} - [ e^{-x} ]^{\infty} _{0} \right\\} = \frac{1}{\lambda}
\end{align}
\\]

### 分散
\\[
	E[T^2] = \int ^{\infty} _{0} t^2 \lambda e^{-\lambda t} dt
\\]
\\(x=\lambda t\\)と置くと,
\\[
\begin{align}
\int ^{\infty} _{0} t^2 \lambda e^{-\lambda t} dt &= \int ^{\infty} _{0} \left(\frac{x}{\lambda}\right)^2 \lambda e^{-x} \frac{1}{\lambda} dx \\\\
&= \frac{1}{\lambda^2} \int ^{\infty} _{0} x^2 e^{-x} dx \\\\
&= \frac{1}{\lambda^2} \int ^{\infty} _{0} x^2 (-e^{-x})' dx \\\\
&= \frac{1}{\lambda^2} \left\\{ \left[ -x^2 e^{-x} \right]^{\infty} _{0} - \int ^{\infty} _{0} 2x (-e^{-x}) dx \right\\} \\\\
&= \frac{1}{\lambda^2} \left\\{  2 \int ^{\infty} _{0} x e^{-x} dx \right\\} = \frac{2}{\lambda^2}
\end{align}
\\]
から,
\\[
	{\rm var}(T) = E[T^2] - E[T]^2 = \frac{2}{\lambda^2} - \frac{1}{\lambda^2} = \frac{1}{\lambda^2}
\\]

### 積率母関数
\\[
\begin{align}
	M_X(t) &= E[e^{tX}] =\int ^{\infty} _{0} e^{tx} \lambda e^{-\lambda x} dx \\\\
	&= \int ^{\infty} _{0} \lambda e^{(t-\lambda) x} dx \\\\
\end{align}
\\]
\\(y = (\lambda-t) x\\)と置く,\\(\frac{dy}{dx} = (\lambda-t)\\).
\\[
\begin{align}
	\int ^{\infty} _{0} \lambda e^{(t-\lambda) x} dx &= \int ^{\infty} _{0} \lambda e^{-(\lambda-t) x} dx \\\\
	&= \lambda \int ^{\infty} _{0} e^{-y}\frac{dy}{(\lambda-t)} \\\\
	&= \frac{\lambda}{(\lambda-t)}
\end{align}
\\]

### 特性関数
\\[
\begin{align}
\varphi_X(t) = E[e^{itX}] = \frac{\lambda}{(\lambda-it)}
\end{align}
\\]

### ハザード関数
上記の(1)式から,
\\[
\lambda(t) = \frac{f_T(t)}{1 - \int ^{t} _{0} f_T(t) dt} = \frac{f_T(t)}{1 - F _T(t)}
\\]
が得られる.これは,**ハザード関数**,**故障率関数**(hazard function)といい,
\\(t\\)時間まで事象が発生せず,\\(t\\)時間に故障が発生する確率になる.
