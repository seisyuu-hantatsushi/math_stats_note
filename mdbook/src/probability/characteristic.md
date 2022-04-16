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
