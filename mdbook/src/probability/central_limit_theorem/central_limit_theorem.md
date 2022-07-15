## 中心極限定理
試行によって得られた事象の平均を得る作業を繰り返しおこなったとき,
その平均の分布は正規分布に近づくことを示したのが,**中心極限定理**(Central limit theorem)である.

### 中心極限定理
\\(\\{X _i\\} _{\overline{\mathbb{N} _+}},\\;  {\scriptsize \mathit i.i.d.} \sim (\mu,\sigma^2)\\)である確率変数列に対して,
\\[
\displaystyle \frac{\sqrt{n}}{\sigma} \left( \frac{\sum ^n _{i=1} X _i}{n} - \mu \right) \xrightarrow{d} \mathcal{N}(0, 1) = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}
\\]
が成立する.

- 証明  
\\(\displaystyle Z_n = \frac{\sqrt{n}}{\sigma} \left( \frac{\sum^n _{i=1} X_i}{n} -\mu \right)\\)とおく,
\\[
\begin{align}
	E[{Z _n}^2] &= E\left[ \left( \frac{\sqrt{n}}{\sigma} \left( \frac{\sum^n _{i=1} X_i}{n} -\mu \right) \right)^2 \right] \\\\
	&= \frac{1}{n \sigma^2 }E\left[(\sum^n _{i=1} X_i - n\mu )^2 \right] \\\\
	&= \frac{1}{n \sigma^2 }E\left[\left( \sum^n _{i=1} (X_i - \mu) \right)^2 \right] \\\\
	&= \frac{1}{n \sigma^2 } E\left[\sum ^n _{i=1}(X_i - \mu)^2  + \sum ^n _{i=1} \sum ^n _{j=1, i \not= j} (X_i - \mu) (X_j - \mu) \right] \\\\
	&= \frac{1}{n \sigma^2 } \sum ^n _{i=1} E\left[(X_i - \mu)^2  + \sum ^n _{j=1, i \not= j} (X_i - \mu) (X_j - \mu) \right] \\\\
	&= \frac{1}{n \sigma^2 } \sum ^n _{i=1} \left( E[(X_i - \mu)^2]  + E\left [\sum ^n _{j=1, i \not= j} (X_i - \mu) (X_j - \mu) \right] \right) \\\\
	&= \frac{1}{n \sigma^2 } \sum ^n _{i=1} \left( E[(X_i - \mu)^2]  + \sum ^n _{j=1, i \not= j} E[ (X_i - \mu) (X_j - \mu) ] \right) \\\\
	&= \frac{1}{n \sigma^2 } \sum ^n _{i=1} \left( E[(X_i - \mu)^2]  + \sum ^n _{j=1, i \not= j} E[ X_i X_j - \mu X_i - \mu X_j  + \mu^2 ] \right) \\\\
	&= \frac{1}{n \sigma^2 } \sum ^n _{i=1} \left( E[(X_i - \mu)^2]  + \sum ^n _{j=1, i \not= j} ( E[ X_i ] E[ X_j ] - \mu E[X_i] - \mu E[X_j]  + \mu^2  ) \right) \\\\
	&= \frac{1}{n \sigma^2 } \sum ^n _{i=1} \left( E[(X_i - \mu)^2]  + \sum ^n _{j=1, i \not= j} E[ X_i ] E[ X_j ] - \mu E[X_i] - \mu E[X_j]  + \mu^2  ) \right) \\\\
	&= \frac{1}{n \sigma^2 } \sum ^n _{i=1} E[(X_i - \mu)^2] \\; \\; ( E[ X_i ] = \mu より)\\\\
	&= \frac{1}{n \sigma^2 } n \sigma^2 = 1
\end{align}
\\]
\\(Z_n\\)の特性関数は,
\\[
\begin{align}
	\varphi _{Z _n}(t) &= E[\exp({it{Z_n}})] \\\\
	&= E\left[ \exp \left(it \frac{\sqrt{n}}{\sigma} \left( \frac{\sum^n _{i=1} X _i}{n} - \mu \right) \right) \right] \\\\
	&= E\left[ \exp \left(it \frac{\sqrt{n}}{\sigma} \frac{1}{n} \left( \\sum^n _{i=1} X _i - n \mu  \right) \right) \right] \\\\
	&= E\left[ \exp \left(it \frac{\sqrt{n}}{\sigma} \frac{1}{n}  \sum^n _{i=1} (X _i - \mu)  \right) \right] \\\\
	&= E\left[ \exp \left(it \frac{\sqrt{n}}{\sigma} \frac{1}{n}  \sum^n _{i=1} (X _i - \mu)  \right) \right] \\\\
	&= E\left[ \exp \left(\sum^n _{i=1} i \frac{t}{\sqrt{n}} \frac{(X _i - \mu)}{\sigma} \right) \right] \\\\
	&= \prod ^n _{i=1} E\left[ \exp \left( i \frac{t}{\sqrt{n}} \frac{(X _i - \mu)}{\sigma} \right) \right] \\\\
	&= \prod ^n _{i=1} \varphi _{Z_i} \left( \frac{t}{\sqrt{n}} \right)
\end{align}
\\]
ここで\\(\displaystyle Z_i = \frac{(X _i - \mu)}{\sigma}\\).

\\(\varphi _{Z_i} \left( \frac{t}{\sqrt{n}} \right)\\)をマクローリン展開すると,
\\[
\varphi _{Z _i} \left( \frac{t}{\sqrt{n}} \right) = \varphi _{Z _i}(0) + {\varphi _{Z _i}}'(0)\left(\frac{t}{\sqrt{n}}\right) + {\varphi _{Z _i}}''(0)\frac{1}{2!}\left(\frac{t}{\sqrt{n}}\right)^2 + {\varphi _{Z _i}}'''(0)\frac{1}{3!}\left(\frac{t}{\sqrt{n}}\right)^3 + \cdots
\\]
\\[
\begin{align}
\varphi _{Z _i}(0) &= \left. E\left[ \exp \left( i \frac{t}{\sqrt{n}} Z _i \right) \right] \right| _{\frac{t}{\sqrt{n}}=0} = \left. \int _{\Omega} \exp \left( i \frac{t}{\sqrt{n}} z _i \right) dP(z_i) \right| _{\frac{t}{\sqrt{n}}=0} = 1 \\\\
\varphi _{Z _i}'(0) &= \left. \frac{d}{d(\frac{t}{\sqrt{n}})} \left\\{ E\left[ \exp \left( i \frac{t}{\sqrt{n}} Z _i \right) \right] \right\\} \right| _{\frac{t}{\sqrt{n}}=0} \\\\
	&= \left. \frac{d}{d(\frac{t}{\sqrt{n}})} \int _{\Omega} \exp \left( i \frac{t}{\sqrt{n}} z _i \right) dP(z_i) \right| _{\frac{t}{\sqrt{n}}=0} \\\\
	&= \int _{\Omega} \left. \frac{\partial}{\partial (\frac{t}{\sqrt{n}})} \exp \left( i \frac{t}{\sqrt{n}} z _i \right) \right| _{\frac{t}{\sqrt{n}}=0} dP(z_i) \\\\
	&= \int _{\Omega} \left. i z_i  \exp \left( i \frac{t}{\sqrt{n}} z _i \right) \right| _{\frac{t}{\sqrt{n}}=0} dP(z_i) \\\\
	&= i \int _{\Omega} z_i dP(z_i) = i E[Z_i] = i E\left[\frac{X_i - \mu}{\sigma}\right] = \frac{i}{\sigma}(E[X_i] - \mu) = 0 \\\\
\varphi _{Z _i}''(0) &= \left. \frac{d^2}{d^2(\frac{t}{\sqrt{n}})} \left\\{ E\left[ \exp \left( i \frac{t}{\sqrt{n}} Z _i \right) \right] \right\\} \right| _{\frac{t}{\sqrt{n}}=0} \\\\
	&= \left. \frac{d}{d(\frac{t}{\sqrt{n}})} \int _{\Omega} \exp \left( i \frac{t}{\sqrt{n}} z _i \right) dP(z_i) \right| _{\frac{t}{\sqrt{n}}=0} \\\\
	&= \int _{\Omega} \left. \frac{\partial^2}{\partial^2 (\frac{t}{\sqrt{n}})} \exp \left( i \frac{t}{\sqrt{n}} z _i \right) \right| _{\frac{t}{\sqrt{n}}=0} dP(z_i) \\\\
	&= \int _{\Omega} \left. \frac{\partial}{\partial (\frac{t}{\sqrt{n}})} i z_i  \exp \left( i \frac{t}{\sqrt{n}} z _i \right) \right| _{\frac{t}{\sqrt{n}}=0} dP(z_i) \\\\
	&= -\int _{\Omega} \left. z_i^2  \exp \left( i \frac{t}{\sqrt{n}} z _i \right) \right| _{\frac{t}{\sqrt{n}}=0} dP(z_i) \\\\
	&= - \int _{\Omega} z_i^2 dP(z_i) = - E\left[\left(\frac{X_i - \mu}{\sigma}\right)^2\right] = - (\frac{1}{\sigma^2}E[(X_i - \mu)^2]) = - \frac{1}{\sigma^2} \sigma^2 = -1\\\\
\end{align}
\\]
から,
\\[
\begin{align}
\varphi _{Z _i} \left( \frac{t}{\sqrt{n}} \right) &= \varphi _{Z _i}(0) + {\varphi _{Z _i}}'(0)\left(\frac{t}{\sqrt{n}}\right) + {\varphi _{Z _i}}''(0)\frac{1}{2!}\left(\frac{t}{\sqrt{n}}\right)^2 + {\varphi _{Z _i}}'''(0)\frac{1}{3!}\left(\frac{t}{\sqrt{n}}\right)^3 + \cdots \\\\
&= 1 - \frac{t^2}{2n} + {\varphi _{Z _i}}'''(0) \frac{t^3}{6n^{\frac{3}{2}}} + \cdots
\end{align}
\\]
なので,\\(\varphi _{Z _n}(t)\\)は,
\\[
\varphi _{Z _n}(t) = \prod ^n _{i=1} \varphi _{Z_i} \left( \frac{t}{\sqrt{n}} \right) = \left(1 - \frac{t^2}{2n} + {\varphi _{Z _i}}'''(0) \frac{t^3}{6n^{\frac{3}{2}}} + \cdots \right)^n
\\]
\\(n \to \infty\\)とした時,第3項以降は,\\(\frac{1}{n}\\)より早く\\(0\\)に近づくので,
\\[
\begin{align}
	\lim _{n \to \infty} \varphi _{Z _n}(t) &= \lim _{n \to \infty} \left(1 - \frac{t^2}{2n} + {\varphi _{Z _i}}'''(0) \frac{t^3}{6n^{\frac{3}{2}}} + \cdots \right)^n \\\\
	&= \lim _{n \to \infty} \left(1 - \frac{t^2}{2n} \right)^n = e^{-\frac{t^2}{2}}
\end{align}
\\]
Levyの収束定理より,
\\[
\lim _{n \to \infty} E[\exp(itZ_n)] = E[\exp(itZ)] \Rightarrow Z_n \xrightarrow{d} Z
\\]
特性関数\\(\displaystyle e^{-\frac{t^2}{2}}\\)に対応する確率変数は正規分布\\(\mathcal{N}(0, 1)\\)なので
\\[
\displaystyle \frac{\sqrt{n}}{\sigma} \left( \frac{\sum ^n _{i=1} X _i}{n} - \mu \right) \xrightarrow{d} \mathcal{N}(0, 1)
\\]
となる.
