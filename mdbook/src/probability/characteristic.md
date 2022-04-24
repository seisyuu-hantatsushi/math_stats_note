# 特性関数
確率密度関数のフーリエ変換を特性関数と言う.

## 特性関数
確率変数\\(X\\)の特性関数を以下のように定義する.
\\[
\begin{align}
\varphi _X(t) = E[e^{itX}] &= \int _{\Omega} e^{itX(\omega)} P(d\omega) \\\\
&= \int ^{\infty} _{-\infty} e^{itx} dP(x) \\\\
&= \int ^{\infty} _{-\infty} e^{itx} f_X(x)dx
\end{align}
\\]

フーリエ変換の単射性により,変換元の関数と変換先の関数が1対1に対応する.
同じように,確率測度と特性関数は1対1対応するはずである.
確率測度が微分可能なら,累積分布関数,確率密度関数も特性関数に1対1対応する.
それを保証するのが以下のLevyの反転定理である.

## Levyの反転定理
\\(P(\cdot)\\)を確率測度とし,その特性関数を\\( \varphi _X (t) \\)とすると
以下が成立する.

\\[
	P(a < X < b) + \frac{1}{2}(P(X=a)+P(X=b)) = \lim_{T \to \infty} \frac{1}{2 \pi} \int ^{T} _{-T} \frac{e^{-ita}-e^{-itb}}{it} \varphi _X(t) dt
\\]

- 証明  
\\[
\begin{align}
F(T) &= \int ^{T} _{-T} \frac{e^{-ita}-e^{-itb}}{it} \varphi _X(t) dt \\\\
	&= \int ^{T} _{-T} \frac{e^{-ita}-e^{-itb}}{it} \int ^{\infty} _{-\infty} e^{itx} dP(x) dt \\\\
	&= \int ^{\infty} _{-\infty} \int ^{T} _{-T} \frac{e^{-ita}-e^{-itb}}{it} e^{itx} dt dP(x) \\: (Fubiniの定理より) \\\\
	&= \int ^{\infty} _{-\infty} \int ^{T} _{-T} \frac{e^{-it(a-x)}-e^{-it(b-x)}}{it} dt dP(x) \\\\
	&= \int ^{\infty} _{-\infty} \int ^{T} _{-T} \frac{\cos(t(a-x))-i\sin(t(a-x))-\cos(t(b-x))+i\sin(t(b-x))}{it} dt dP(x) \\\\
	&= \int ^{\infty} _{-\infty}\left(\int ^{T} _{-T} \frac{\cos(t(a-x))-\cos(t(b-x))}{it} dt + \int ^{T} _{-T} \frac{i\sin(t(b-x))-i\sin(t(a-x))}{it} dt \right) dP(x)
\end{align}
\\]
\\(\frac{\cos(t(a-x))-\cos(t(b-x))}{it}\\)は奇関数なので,積分範囲が対称だと0になる.
\\[
\begin{align}
	&= \int ^{\infty} _{-\infty}\left(\int ^{T} _{-T} \frac{\sin(t(b-x))-\sin(t(a-x))}{t} dt \right) dP(x) \\\\
	&= \int ^{\infty} _{-\infty}\left(\int ^{T} _{-T} \frac{\sin(t(b-x))}{t} dt - \int ^{T} _{-T} \frac{\sin(t(a-x))}{t} dt \right) dP(x)
\end{align}
\\]

\\(F(T)\\)に\\(\frac{1}{2\pi}\\)を乗して,\\(T \to \infty\\)の極限を取る.

\\[
\begin{align}
\lim_{T \to \infty} \frac{1}{2 \pi} F(T) &= \lim_{T \to \infty} \frac{1}{2 \pi} \int ^{\infty} _{-\infty}\left(\int ^{T} _{-T} \frac{\sin(t(b-x))}{t} dt - \int ^{T} _{-T} \frac{\sin(t(a-x))}{t} dt \right) dP(x) \\\\
&= \frac{1}{2 \pi} \int ^{\infty} _{-\infty} \left(\lim _{T \to \infty} \int ^{T} _{-T} \frac{\sin(t(b-x))}{t} dt - \lim _{T \to \infty} \int ^{T} _{-T} \frac{\sin(t(a-x))}{t} dt \right) dP(x)
\end{align}
\\]
\\(\frac{\sin(t(a-x))}{t}\\)は\\(t\\)の関数と見ると,偶関数なので,
\\[
\begin{align}
f_a(x) &= \lim _{T \to \infty} \int ^{T} _{-T} \frac{\sin(t(a-x))}{t} dt = \lim _{T \to \infty} 2 \int ^{T} _{0} \frac{\sin(t(a-x))}{t} dt \\\\
&= \left\\{ \begin{array}{ll}
	\pi & (x < a) \\\\
	0 & (x = a) \\\\
	-\pi & (x > a) \\\\
\end{array} \right.
\end{align}
\\]

から,
\\[
\begin{align}
 \frac{1}{2 \pi} \int ^{\infty} _{-\infty} \left(\lim _{T \to \infty} \int ^{T} _{-T} \frac{\sin(t(b-x))}{t} dt - \lim _{T \to \infty} \int ^{T} _{-T} \frac{\sin(t(a-x))}{t} dt \right) dP(x) &=
  \frac{1}{2 \pi} \int ^{\infty} _{-\infty} (f_b(x) - f_a(x)) dP(x)
\end{align}
\\]

\\(f_a(x)\\)は指示関数で書き直すと,\\(f_a(x) = \pi (I _{x < a}(x) - I _{x > a}(x)) \\)
\\[
\begin{align}
  \frac{1}{2 \pi} \int ^{\infty} _{-\infty} (f_b(x) - f_a(x)) dP(x) &= \frac{1}{2 \pi} \int ^{\infty} _{-\infty} (\pi (I _{x < b}(x) - I _{x > b}(x)) - \pi (I _{x < a}(x) - I _{x > a}(x))) dP(x) \\\\
  &= \frac{1}{2} \int ^{\infty} _{-\infty} (I _{x > b}(x) - I _{x < b}(x) - I _{x < a}(x) + I _{x > a}(x)) dP(x) \\\\
  &= \frac{1}{2} \int ^{\infty} _{-\infty} (2 I _{a < x < b}(x) + I _{x > a \land x = b}(x) + I _{x < b \land x = a}(x)) dP(x) \\\\
  &= P(a < x < b) + \frac{1}{2}(P(X=a)+P(X=b))
\end{align}
\\]

証明終わり.
