## 推定の方法
母集団として,&thinsp;\\(f(x|\boldsymbol{\theta}=(\theta_1,\dots,\theta_k))\\)を想定し,
そこから得られる無作為標本\\(\\{X_i\\} _{i \in \mathbb{N} _+,i \leq n}\\)から,
\\({\mathbf \theta}\\)を推定する方法を考える.\\(\\{X_i\\}\\)から\\(\boldsymbol{\theta}\\)を推定する関数を,
\\(\hat{\boldsymbol{\theta}}: \mathbb{R}^n \mapsto \mathbb{R}^k\\)を\\(\mathbf{\theta}\\)の推定量(estimator)という.
実際に\\({\mathbf X} = (X_1,\dots,X_n)\\)の実現値\\({\mathbf x} = (x_1,\dots,x_n)\\)を推定量に代入した,
\\(\hat{\boldsymbol{\theta}}({\mathbf x})\\)を推定値(estimate)と言う.

### モーメント法
\\(f(x;\boldsymbol{\theta})\\)なる確率変数\\(X\\)に対して,\\(E[X^k]={\mu_k}'(\boldsymbol{\theta})\\)と表されるとする.
\\(\\{X _i\\} _{i \in \mathbb{N} _+,i \leq n} i,i,d \sim f(x;\boldsymbol{\theta})\\)なる無作為標本について,
大数の弱法則より\\(\frac{1}{n} \sum ^{n} _{i=1} {X_i}^r \xrightarrow{p} E[X^r] \\)となることを利用して,

\\[
  \left\\{
	\begin{array}{ll}
	\frac{1}{n} \sum ^{n} _{i=1} {X_i} \xrightarrow{p} E[X] &= {\mu_1}'(\boldsymbol{\theta}) \\\\
	\frac{1}{n} \sum ^{n} _{i=1} {X_i} \xrightarrow{p} E[X^2] &= {\mu_2}'(\boldsymbol{\theta}) \\\\
	&\vdots \\\\
	\frac{1}{n} \sum ^{n} _{i=1} {X_i} \xrightarrow{p} E[X^k] &= {\mu_k}'(\boldsymbol{\theta})
	\end{array}
  \right.
\\]

### 最尤法


### ベイズ法
