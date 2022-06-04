# 平均・分散・モーメント
平均・分散・モーメントは,確率変数の特性を表す値である.

## 平均値・分散
\\(g(X)=X\\)としたときの期待値を**平均**といい,
\\[
\mu = E[X]
\\]と表す.

\\(g(X)=(X-\mu)^2\\)としたときの期待値を**分散**といい,
\\[
	{\rm var}(X)=E[(X-\mu)^2]
\\]
と表す.また\\(\sigma = \sqrt{{\rm var}(X)}\\)と置き,**標準偏差**という.

分散は期待値の線形性より,
\\[
	E[(X-\mu)^2]=E[X^2-2\mu X+\mu^2] = E[X^2]-\mu^2 = E[X^2]-E[X]^2
\\]

### Chebyshevの不等式
確率変数\\(X\\)の平均を\\(\mu\\),分散を\\(\sigma^2\\)とする.\\(\varepsilon \geq 0\\)に対して,
\\[
	P(|X-\mu| \geq \varepsilon) \leq \frac{\sigma^2}{\varepsilon^2} \tag{Chebyshev}
\\]
が成立する.

- 証明  
Markovの不等式にて\\(g(X)=(X-\mu)^2,\\,a=\varepsilon^2\\)と置くと,
\\[
E[(X-\mu)^2] \geq \varepsilon^2 P(|X-\mu| \geq \varepsilon)
\\]
から
\\[
P(|X-\mu| \geq \varepsilon) \leq \frac{\sigma^2}{\varepsilon^2} \\\\
\\]

## モーメント
\\(k \in \mathbb{N},k \geq 1\\\)に対して,
\\[
E[(X-\mu)^k] = \int ^{\infty} _{-\infty} (x-\mu)^k f_X(x) dx
\\]
を**平均値周りの\\(k\\)次モーメント**と言う.\\(k=2\\)の場合は分散となる.
モーメントは**積率**とも言う.
