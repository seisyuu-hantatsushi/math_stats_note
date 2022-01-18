# 大数の法則
試行の回数が多く取ると平均が真の平均に近づくことを保証したのが,大数の法則である.

## 大数の弱法則
平均\\(\mu < \infty\\),分散\\(\sigma^2 < \infty\\)とし,\\(\\{X_n\\}\\)が\\((\mu,\sigma^2)\\)に従うとする.
このとき,**算術平均**
\\[
\overline{X} = \displaystyle \frac{1}{n} \sum^{n} _ {i=1} X_i
\\]
は
\\[
	\overline{X} \xrightarrow{p} \mu
\\]
と平均に確率収束する.

- 証明  
  \\[
  \begin{align}
E[(\overline{X}-\mu)^2] &=  E[(\frac{1}{n} \sum^{n} _ {i=1} X_i-\mu)^2] \\\\
&=  E[\frac{1}{n^2}(\sum^{n} _ {i=1} X_i- n\mu)^2] \\\\
&=  \frac{1}{n^2}E[\sum^{n} _ {i=1}(X_i- \mu)^2] \\\\
&= \frac{\sigma^2}{n^2}
  \end{align}
  \\]
より,上式は平均収束する.
\\[
\lim_{n \to \infty} E[(\overline{X}-\mu)^2] = \lim_{n \to \infty} \frac{\sigma^2}{n^2} = 0
\\]
平均収束ならば,Chebyshevの不等式より確率収束する.

## 大数の強法則

