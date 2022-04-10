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
&= \frac{1}{b _i} \sum ^{i} _{k=1} (b _k s _k - b _k s _{k-1}) \\\\
&= \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _k - \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _{k-1} \\\\
&= s _i + \frac{1}{b _i} \sum ^{i-1} _{k=1} b _k s _k - \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _{k-1} \\\\
&= s _i + \frac{1}{b _i} \sum ^{i} _{k=1} b _{k-1} s _{k-1} - \frac{1}{b _i} \sum ^{i} _{k=1} b _k s _{k-1} \\\\
&= s _i - \frac{1}{b _i} \sum ^{i} _{k=1} (b _k - b _{k-1}) s _{k-1}
\end{align}
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
最後の式は,\\(\varepsilon = \max _{I \leq k \leq i} (s _{k-1} - s _{\infty}) \\)とすると,
\\[
\begin{align}
\lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})(s _{k-1} - s _{\infty}) & \leq \lim _{i \to \infty}\frac{1}{b _i} \sum ^{i} _{k=I} (b _k - b _{k-1})\varepsilon \\\\
& = \lim _{i \to \infty}\frac{1}{b _i} (b _i - b _{I-1})\varepsilon \\\\
& = \lim _{i \to \infty}(1 - \frac{b _{I-1}}{b _i})\varepsilon \\\\
& = \varepsilon
\end{align}
\\]
なので,\\(i \to \infty\\)とすれば,\\(\max _{I \leq k} (s _{k-1} - s _{\infty}) \\)は,\\(\max _{I \leq k} (s _{k-1} - s _{\infty}) \to 0\\)とするような,\\(I\\)を任意に選べるので,\\(\varepsilon \to 0\\).
より,\\(\sum ^{\infty} _{i=1} \frac{x _i}{b _i}\\)が収束するならば,\\(\frac{1}{b _i} \sum ^{i} _{k=1} x _k \to 0\\)

### Kolmogrovの大数の強法則
平均\\(\mu < \infty\\),分散\\(\sigma^2 < \infty\\)とし,互いに独立な確率変数\\(\\{X_i\\} \subset L^2\\)が\\((\mu,\sigma^2)\\)に従うとする.その時,
\\[
	\\overline{X} = \frac{1}{n}\sum^{n} _{i=1} X_i \xrightarrow{P \text{-a.s}} \mu
\\]

- 証明  
  まず,\\(\sum {\rm var}(X_i)\\)が収束するなら,Kolmogorovの定理から,題意は満たされる.

  次に,\\(\sum {\rm var}(X_i)\\)が発散する場合,\\(\sum _{i=1} ^{n} {\rm var}(X_i)\\)が有界かを考える.
  仮定で\\( {\rm var}(X_i) < \infty \\)であるので,\\({\rm var}(X_i)\\)には上界があり,\\( a = \sup {\rm var}(X_i) \\)とすると,
  \\(\sum _{i=1} ^{n} {\rm var}(X_i) \leq na \\).なので,
  \\[
	  \frac{\sum _{i=1} ^{n} X_i - E[\sum _{i=1} ^{n} X_i]}{\sum _{i=1} ^{n} {\rm var}(X_i)} = \frac{\sum _{i=1} ^{n} (X_i - E[X_i])}{\sum _{i=1} ^{n} {\rm var}(X_i)} \xrightarrow{P \text{-a.s}} 0 \tag{1}
  \\]
  であると,題意が満たされる.

  - 補題1  
    \\(\\{X_i\\} \subset L^2\\)を互いに独立な確率変数とし,\\(\\{b _i\\} _{1 \leq i \leq \infty}\\)を\\( \infty \\)に発散する増加正数列とする.
	\\[
		\sum ^{\infty} _{i=1} \frac{{\rm var}(X_i)}{{b _i}^2} < \infty
	\\]
	ならば,\\(n \to \infty\\)の時,
	\\[
		\frac{\sum _{i=1} ^{n} X _i - E[\sum _{i=1} ^{n} X _i]}{b_n} = \frac{\sum _{i=1} ^{n} (X _i - E[X _i])}{b_n} \xrightarrow{P \text{-a.s}} 0
	\\]
	  - 証明  
	    \\(Y _i = (X _i - E[X _i])/b _i \\)と置く.
		\\[
			E[Y _i] = E\left[\frac{X _i - E[X _i]}{b _i}\right] = \frac{E[X _i] - E[X _i]}{b _i} = 0
		\\]
		から,
		\\[
			\begin{align}
			\sum ^{\infty} _{i=1} {\rm var}(Y _i) &= \sum ^{\infty} _{i=1} {\rm var}\left(\frac{X _i - E[X _i]}{b _i}\right) \\\\
			&= \sum ^{\infty} _{i=1} E\left[ \left(\frac{X _i - E[X _i]}{b _i}\right)^2\right] \\\\
			&= \sum ^{\infty} _{i=1} \frac{1}{{b _i}^2} E[ (X _i - E[X _i])^2 ] \\\\
			&= \sum ^{\infty} _{i=1} \frac{{\rm var}(X _i)}{{b _i}^2}  \\\\
			\end{align}
		\\]
		仮定の\\(\sum ^{\infty} _{i=1} \frac{{\rm var}(X_i)}{{b _i}^2} < \infty\\)から,\\(\sum ^{\infty} _{i=1} {\rm var}(Y _i) < \infty\\).
		から,\\(\\{Y _i \\}\\)は,Kolmogrovの定理により\\(\sum ^{\infty} _{i=1} Y _i  = \sum ^{\infty} _{i=1} (X _i - E[X _i])/b _i \\)は概収束する.
		さらにKroneckerの補題により
		\\[
			\frac{1}{b _n} \sum ^{n} _{i=1} (X _i - E[X _i]) \xrightarrow{P \text{-a.s}} 0
		\\]

  - 補題2  
    \\(\\{X_i\\} \subset L^2\\)を互いに独立な確率変数とする.\\(\sum ^{\infty} _{i=1} {\rm var}(X _i)\\)が発散するならば,\\(\varepsilon > 0\\)に対して,
	\\[
		\frac{\sum ^{n} _{i=1} (X _i - E[X _i])}{(\sum^{n} _{i=1} {\rm var}(X _i))^{1/2+\varepsilon}} \xrightarrow{P \text{-a.s}} 0. \\;(n \to \infty)
	\\]
	- 証明  
	  補題1で\\(b _i = (\sum^{i} _{j=1} {\rm var}(X _j))^{1/2+\varepsilon} \\)とおくと,
	  \\[
			\sum ^{\infty} _{i=1} \frac{{\rm var}(X_i)}{{b _i}^2} = \sum ^{\infty} _{i=1} \frac{{\rm var}(X_i)}{((\sum^{i} _{j=1} {\rm var}(X _j))^{1/2+\varepsilon})^2}< \infty
	  \\]
	  ならば,
	  \\[
		  \frac{\sum _{i=1} ^{n} (X _i - E[X _i])}{b_n} = \frac{\sum _{i=1} ^{n} (X _i - E[X _i])}{(\sum^{n} _{i=1} {\rm var}(X _i))^{1/2+\varepsilon}}\xrightarrow{P \text{-a.s}} 0. \\; (n \to \infty)
	  \\]
	  なので,\\(\sum ^{\infty} _{i=1} \frac{{\rm var}(X_i)}{((\sum^{i} _{j=1} {\rm var}(X _j))^{1/2+\varepsilon})^2}< \infty\\)であることを確かめればよい.
	  \\( \{\rm var}(X _i) = \sum ^{i} _{j=1} {\rm var}(X _j) - \sum ^{i-1} _{j=1} {\rm var}(X _j),\\;i>1 \\)なので
	  \\[
		\begin{align}
		  \sum ^{\infty} _{i=2} \frac{{\rm var}(X_i)}{((\sum^{i} _{j=1} {\rm var}(X _j))^{1/2+\varepsilon})^2} &= 
			\sum ^{\infty} _{i=2} \frac{\sum ^{i} _{j=1} {\rm var}(X _j) - \sum ^{i-1} _{j=1} {\rm var}(X _j)}{(\sum^{i} _{j=1} {\rm var}(X _j))^{1+2\varepsilon}} \\\\
			&\leq \sum ^{\infty} _{i=2} \int^{\sum ^{i} _{j=1} {\rm var}(X _j)} _{\sum ^{i-1} _{j=1} {\rm var}(X _j)} \frac{dx}{x^{1+2\varepsilon}} \\\\
			&= \int ^{\infty} _{{\rm var}(X _1)} \frac{dx}{x^{1+2\varepsilon}} = \left[ \frac{1}{-2\varepsilon} \frac{1}{x^{2\varepsilon}}\right]^{\infty} _{{\rm var}(X _1)}< \infty
		\end{align}
	  \\]
	  証明終わり.
  式(1)は,補題2において,\\(\varepsilon=1/2\\)とすると成立し,よって大数の強法則が証明される.

### 同分布でのKolmogrovの大数の強法則
