### 正規分布に従う母集団の検定
標本が正規分布に従っているとする.正規分布のパラメータは平均と分散である.
なので,標本から得た平均と分散が帰無仮説で設定した正規分布からどれくらいの確率で違っているを検定する.
以降,\\(\\{X_i\\} _{i,n \in \mathbb{N} _+,i \leq n} .i.i.d \sim \mathcal{N}(\mu,\sigma^2)\\)であるとする.

#### 1標本の平均の検定
標本の平均を対象とする仮説は,

\\[
\begin{align}
	& H_0:\mu=\mu_0 \\; \mathrm{vs} \\; H_1:\mu \neq \mu_0 & \\; 両側検定 \\\\
	& H_0:\mu=\mu_0 \\; \mathrm{vs} \\; H_1:\mu > \mu_0 & \\; 右片側検定 \\\\
	& H_0:\mu=\mu_0 \\; \mathrm{vs} \\; H_1:\mu < \mu_0 & \\; 左片側検定
\end{align}
\\]

##### 分散が既知の場合
もし,帰無仮設に標本が従っているとするならば,\\(\bar{X} = \frac{1}{n}\sum^n_{i=1} X_i \sim \mathcal{N}(\mu_0,\sigma^2/n)\\)なので,
\\[
	Z = \frac{\bar{X} - \mu_0}{\sqrt{\sigma^2/n}} \sim \mathcal{N}(0,1)
\\]
\\(Z\\)を検定統計量とする.有意水準を\\(\alpha\\)とし,棄却域と受容域の境界値を棄却限界値いう.
片側検定の場合,有意水準\\(\alpha\\)の棄却限界値を\\(z_{\alpha}\\)は,
\\[
\begin{align}
	& P(Z \geq z_{\alpha}) = \alpha & \\; 右側検定 \\\\
	& P(Z \leq -z_{\alpha}) = \alpha & \\; 左側検定
\end{align}
\\]
となり,両側検定の場合は,
\\[
 P(Z \geq z_{\alpha/2}) + P(Z \leq -z_{\alpha/2}) = \alpha
\\]
となる.
なので,\\(\bar{X}\\)の観測値を\\(\bar{x}\\)とし
\\[
z = \frac{\bar{x} - \mu_0}{\sqrt{\sigma^2/n}}
\\]
で得られて値が,片側検定ならば\\(z \geq z_{\alpha}, z \leq z_{\alpha}\\), 両側検定ならば\\(z \geq -z_{\alpha/2} または z \leq z_{\alpha/2} \\)の場合,帰無仮説を棄却する.

##### 分散が未知の場合
分散の推定量として不偏分散\\(V^2 = \frac{1}{n-1}\sum^n_{i=1}(X_i-\bar{X})^2\\)を使用する.   
\\(\frac{(n-1)V^2}{\sigma^2} \sim \chi^2_{n-1} \\)なので,
\\[
	Z = \frac{\bar{X} - \mu_0}{\sqrt{\sigma^2/n}} \sim \mathcal{N}(0,1) \\\\
	\begin{align}
	\frac{Z}{\sqrt{\frac{\frac{(n-1)V^2}{\sigma^2}}{n-1}}} &= \frac{Z}{\sqrt{\frac{V^2}{\sigma^2}}} \\\\
	&= \frac{\sqrt{\sigma^2}\frac{\bar{X} - \mu_0}{\sqrt{\sigma^2/n}}}{\sqrt{V^2}} \\\\
	&= \frac{\sqrt{n}(\bar{X} - \mu_0)}{\sqrt{V^2}} \sim T_{n-1} 
	\end{align}
\\]
改めて
\\[
	T_{n-1} = \frac{\sqrt{n}(\bar{X} - \mu_0)}{\sqrt{V^2}}
\\]
を検定推定量とする.検定推定値は,
\\[
	v^2 = \frac{1}{n-1}\sum^n_{i=1}(x_i-\bar{x})^2 \\\\
	t_{n-1} = \frac{\sqrt{n}(\bar{x} - \mu_0)}{\sqrt{v^2}}
\\]
有意水準\\(\alpha\\)とすると,それぞれの棄却域は,
\\[
P(T_{n-1} \geq t_{n-1,\alpha}) = \alpha \\\\
P(T_{n-1} \leq t_{n-1,\alpha}) = \alpha \\\\
 P(T_{n-1} \leq -t_{n-1,\alpha/2}) + P(T_{n-1} \geq t_{n-1,\alpha/2}) = \alpha
\\]
を見みたす,\\( t_{n-1,\alpha}, t_{n-1,\alpha/2}\\)片側検定ならば\\(t_{n-1} \leq -t_{n-1,\alpha}, t_{n-1} \geq t_{n-1,\alpha}\\), 両側検定ならば\\(t_{n-1} \geq -t_{n-1, \alpha/2} または t_{n-1} \leq t_{n-1,\alpha/2} \\)の場合,帰無仮説を棄却する.


#### 1標本の分散の検定
標本の平均を対象とする仮説は,
\\[
\begin{align}
	& H_0:\sigma^2=\sigma_0^2 \\; \mathrm{vs} \\; H_1:\sigma^2 \neq \sigma_0^2 & \\; 両側検定 \\\\
	& H_0:\sigma^2=\sigma_0^2 \\; \mathrm{vs} \\; H_1:\sigma^2 > \sigma_0^2 & \\; 右片側検定 \\\\
	& H_0:\sigma^2=\sigma_0^2 \\; \mathrm{vs} \\; H_1:\sigma^2 < \sigma_0^2 & \\; 左片側検定
\end{align}
\\]
##### 平均が既知の場合
\\(H_0:\sigma^2=\sigma_0^2\\)の\\(\bar{X}\\)分布は,\\( X_i \sim \mathcal{N}(\mu,\sigma_0^2)\\)なので,
\\[
	Z_i = \frac{X_i-\mu}{\sigma_0} \sim \mathcal{N}(0, 1)
\\]
\\(Z_i^2 \sim \chi^2_1\\)
\\[
	Z_i^2 = \frac{(\bar{X} - \mu)^2}{\sigma_0^2}
\\]
より,
\\[
	Q_{n} = \sum^n_{i=1} Z_i^2 = \sum^n_{i=1}\frac{(X_i - \mu)^2}{\sigma_0^2} \sim \chi^2_n
\\]
これを検定推定量とする.
観測値から検定推定値は
\\[
	q_{n} = \sum^n_{i=1}\frac{(x_i - \mu)^2}{\sigma_0^2}
\\]
有意水準\\(\alpha\\)とすると,それぞれの棄却域は,
\\[
P(Q_n \geq q_{n,\alpha}) = \alpha \\\\
P(Q_n \leq q_{n,\alpha}) = \alpha \\\\
 P(Q_n \leq q_{n,\alpha_{lower}}) + P(Q_n \geq q_{n,\alpha_{upper}}) = \alpha
\\]

##### 平均が未知の場合
平均の推定量として,標本平均\\( \bar{X}=\frac{1}{n} \sum^n_{i=1} X_i \\)を利用する.
検定推定量として,分散の不偏推定量の不偏分散を使う.
\\[
	V^2 = \frac{1}{n-1} \sum^n_{i=1} (X_i - \bar{X})^2 \\\\
	Q_{n-1} = \frac{(n-1)V^2}{\sigma_0^2} = \sum^n_{i=1} \frac{(X_i - \bar{X})^2}{\sigma_0^2} \sim \chi^2_{n-1}
\\]
観測値から検定推定値は
\\[
	q_{n-1} = \sum^n_{i=1} \frac{(x_i - \bar{x})^2}{\sigma_0^2}
\\]
有意水準\\(\alpha\\)とすると,それぞれの棄却域は,
\\[
P(Q_{n-1} \geq q_{n-1,\alpha}) = \alpha \\\\
P(Q_{n-1} \leq q_{n-1,\alpha}) = \alpha \\\\
P(Q_{n-1} \leq q_{n-1,\alpha_{lower}}) + P(Q_{n-1} \geq q_{n-1,\alpha_{upper}}) = \alpha
\\]

#### 2標本の平均の検定
2標本の平均がどれくらい違うかの検定を考える.標本\\(A,B\\)を用意して,それぞれの標本が
\\[
 \\{{X_A}_i\\} _{i,n_A \in \mathbb{N} _+,i \leq n_A} .i.i.d \sim \mathcal{N}(\mu_A,\sigma_A^2) \\\\
 \\{{X_B}_i\\} _{i,n_B \in \mathbb{N} _+,i \leq n_B} .i.i.d \sim \mathcal{N}(\mu_B,\sigma_B^2)
\\]
に従うとする.仮説は,
\\[
\begin{align}
	& H_0:\mu_A=\mu_B \\; \mathrm{vs} \\; H_1:\mu_A \neq \mu_B & \\; 両側検定 \\\\
	& H_0:\mu_A=\mu_B \\; \mathrm{vs} \\; H_1:\mu_A > \mu_B & \\; 右片側検定 \\\\
	& H_0:\mu_A=\mu_B \\; \mathrm{vs} \\; H_1:\mu_A < \mu_B & \\; 左片側検定
\end{align}
\\]
\\(\delta = \mu_A-\mu_B\\)とすると,
\begin{align}
	& H_0:\delta=\delta_0 \\; \mathrm{vs} \\; H_1:\delta \neq \delta_0 & \\; 両側検定 \\\\
	& H_0:\delta=\delta_0 \\; \mathrm{vs} \\; H_1:\delta > \delta_0 & \\; 右片側検定 \\\\
	& H_0:\delta=\delta_0 \\; \mathrm{vs} \\; H_1:\delta < \delta_0 & \\; 左片側検定
\end{align}
##### 分散既知で,標本\\(A,B\\)の分散が等しい場合
\\[
 \\{{X_A}_i\\} _{i,n_A \in \mathbb{N} _+,i \leq n_A} .i.i.d \sim \mathcal{N}(\mu_A,\sigma^2) \\\\
 \\{{X_B}_i\\} _{i,n_B \in \mathbb{N} _+,i \leq n_B} .i.i.d \sim \mathcal{N}(\mu_B,\sigma^2)
\\]

から

\\[
\bar{X_A} = \frac{1}{n} \sum^{n_A}_{i=1} {X_A}_i \sim \mathcal{N}(\mu_A,\frac{\sigma^2}{n_A}) \\\\
\bar{X_B} = \frac{1}{n} \sum^{n_B}\_{i=1} {X_B}_i \sim \mathcal{N}(\mu_B,\frac{\sigma^2}{n_B}) \\\\
\bar{X_A} - \bar{X_B} \sim \mathcal{N}(\mu_A-\mu_B, \frac{\sigma^2}{n_A} + \frac{\sigma^2}{n_B})
\\]

より

\\[
	Z = \frac{\bar{X_A} - \bar{X_B} - \delta}{\sqrt{\frac{\sigma^2}{n_A} + \frac{\sigma^2}{n_B}}} \sim \mathcal{N}(0,1)
\\]
を統計検定量とする.
