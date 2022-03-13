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
