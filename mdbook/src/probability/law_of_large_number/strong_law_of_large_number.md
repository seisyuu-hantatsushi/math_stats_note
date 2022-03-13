## 大数の強法則(Kolmogrovの大数の強法則)
平均\\(\mu < \infty\\),分散\\(\sigma^2 < \infty\\)とし,互いに独立な確率変数\\(\\{X_i\\}\\)が\\((\mu,\sigma^2)\\)に従うとする.
ならば
\\[
\\overline{X} \xrightarrow{P \text{-a.s}} \mu
\\]
と概収束する.
まず,Kronecckerの補題を示す.

### Kroneckerの補題
\\(\\{x _i\\} _{1 \leq i \leq \infty}\\)を実数列,\\(\\{b _i\\} _{1 \leq i \leq \infty}\\)を\\( \infty \\)に発散する増加正数列とする.
\\[
	\sum ^{\infty} _{i=1} \frac{x _i}{b _i}が収束するならば,\frac{1}{b _i} \sum ^{i} _{k=1} x _k \to 0
\\]

- 証明  
\\(i \in \overline{\mathbb{N}} \\)に対し,
\\[
s _0 = 0, \\; s _i = \sum ^{i} _{k=1} \frac{x _k}{b _k}
\\]
と置くと,
\\[
	x _i = b _i (s _i - s _{i-1})
\\]
