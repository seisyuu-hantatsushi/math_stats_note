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
より,
\\[
\begin{align}
\frac{1}{b _i} \sum ^{i} _{k=1} x _k &= \frac{1}{b _i} \sum ^{i} _{k=1} b _k (s _k - s _{k-1}) \\\\
&= \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _k - b _k s _{k-1} \\\\
&= \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _k - \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _{k-1} \\\\
&= s _i - \frac{1}{b _i} \sum ^{i-1} _{k=1} b _k s _k - \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _{k-1} \\\\
&= s _i + \frac{1}{b _i} \sum ^{i} _{k=1} b _{k-1} s _{k-1} - \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _{k-1} \\\\
&= s _i - \frac{1}{b _i} \sum ^{i} _{k=1} (b _k - b _{k-1}) s _{k-1}
\end{align}
\\]

\\(\\{b _i\\}\\)は,増加正数列なので,
\\[
b _k - b _{k-1} \geq 0, b _n = \sum^{n} _{k=1} b _k - b _{k-1} \\; (b _0 = 0)
\\]
\\(\lim _{i \to \infty} s _i = s _{\infty}\\)とし,
\\[
\begin{align}
\frac{1}{b _i} \sum ^{i} _{k=1} x _k &= s _i - \frac{1}{b _i} \sum ^{i} _{k=1} (b _k - b _{k-1}) s _{k-1} \\\\
&=  s _i - \frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1}) s _{k-1} - \frac{1}{b _i} \sum ^{I} _{k=1} (b _k - b _{k-1}) s _{k-1} \\\\
&=  s _i - \frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1}) s _{\infty} - \frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) - \frac{1}{b _i} \sum ^{I} _{k=1} (b _k - b _{k-1}) s _{k-1} \\\\
&=  s _i - \frac{(b _i - b _{I-1})}{b _i}s _{\infty} - \frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) - \frac{1}{b _i} \sum ^{I} _{k=1} (b _k - b _{k-1}) s _{k-1} \\\\
\end{align}
\\]
上式の\\(i \to \infty\\)を取る.
\\[
\begin{align}
\frac{1}{b _i} \sum ^{\infty} _{k=1} x _k  &=  s _{\infty} - \lim _{i \to \infty}\frac{(b _i - b _{I-1})}{b _i}s _{\infty} - \lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) - \lim _{i \to \infty} \frac{1}{b _i} \sum ^{I} _{k=1} (b _k - b _{k-1}) s _{k-1} \\\\
\end{align}
\\]
第2項は
\\[
\lim _{i \to \infty}\frac{(b _i - b _{I-1})}{b _i}s _{\infty} = \lim _{i \to \infty} (1 - \frac{b _{I-1}}{b _i})s _{\infty}
\\]
\\(\\{b _i\\}\\)は正に発散する増加数列なので,
\\[
\lim _{i \to \infty}\frac{(b _i - b _{I-1})}{b _i}s _{\infty} = s _{\infty}
\\]
第4項は\\(\\{b _i\\}\\)は正に発散する増加数列なので,\\(i \to \infty\\)ならば0になる.
から,もとの式は
\\[
\begin{align}
\frac{1}{b _i} \sum ^{\infty} _{k=1} x _k  &=  s _{\infty} - \lim _{i \to \infty}\frac{(b _i - b _{I-1})}{b _i}s _{\infty} - \lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) - \lim _{i \to \infty} \frac{1}{b _i} \sum ^{I} _{k=1} (b _k - b _{k-1}) s _{k-1} \\\\
&= s _{\infty} -s _{\infty} - \lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) \\\\
&= - \lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) \\\\
\end{align}
\\]
最後の式は,\\(\varepsilon = \max _{k} (s _{k-1} - s _{\infty}) \\)とすると,
\\[
\begin{align}
\lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) & \leq \lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})\varepsilon \\\\
& = \lim _{i \to \infty}\frac{1}{b _i} (b _i - b _{I-1})\varepsilon \\\\
& = \lim _{i \to \infty}(1 - \frac{b _{I-1}}{b _i})\varepsilon \\\\
& = \varepsilon
\end{align}
\\]
なので,\\(i \to 0\\)とすれば,\\(\varepsilon \to 0\\)となる.
より,\\(\sum ^{\infty} _{i=1} \frac{x _i}{b _i}\\)が収束するならば,\\(\frac{1}{b _i} \sum ^{i} _{k=1} x _k \to 0\\)
