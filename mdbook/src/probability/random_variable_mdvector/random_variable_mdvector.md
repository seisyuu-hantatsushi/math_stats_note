## 確率変数多次元ベクトル
\\(X_i, i \in \mathbb{N} _+,i \leq n \\)となるindex付きの確率変数を用意して,
\\[
\boldsymbol{X} = \begin{pmatrix} 
		X_1 \\\\
		X_2 \\\\
		\vdots \\\\
		X_n
	\end{pmatrix}
\\]
この,平均を \\(\mathrm{E}[X_i] = \mu_i\\) と分散,共分散を\\( \sigma\_{ij} = \mathrm{Cov}(X_i,X_j) \\)として,
\\[
\mathrm{E}[\boldsymbol{X}] = \boldsymbol{\mu} = \begin{pmatrix} 
		\mu_1 \\\\
		\mu_2 \\\\
		\vdots \\\\
		\mu_n
	\end{pmatrix} \\\\
\mathrm{V}[\boldsymbol{X}]	= \boldsymbol{\Sigma} = \begin{pmatrix} 
		\sigma\_{11} & \sigma\_{12} & \cdots & \sigma\_{1n} \\\\
		\sigma\_{21} & \sigma\_{22} & \cdots & \sigma\_{2n} \\\\
		\vdots & \vdots & \ddots & \vdots \\\\
		\sigma\_{n1} & \sigma\_{n2} & \cdots & \sigma\_{nn}
	\end{pmatrix} \\\\
\\]
表す.
\\(\mathbf{A} \in \mathbb{R}^{m \times n},\boldsymbol{b} \in \mathbb{R}^{n}\\)として,
\\[
	\boldsymbol{Z} = \mathbf{A}\boldsymbol{X} + \boldsymbol{\mu} 
\\]
という線形変換を行ったとき,
\\[
	\begin{align}
	\mathrm{E}[\boldsymbol{Z}] &= \mathrm{E}[\mathbf{A}\boldsymbol{X} + \boldsymbol{\mu}] \\\\
	&=\mathrm{E}[\mathbf{A}\boldsymbol{X}] + \boldsymbol{\mu} \\\\
	&= \mathbf{A}\mathrm{E}[\boldsymbol{X}] + \boldsymbol{\mu}
	\end{align}
\\]
\\[
	\begin{align}
	\mathrm{V}[\boldsymbol{Z}] &= \mathrm{V}[\mathbf{A}\boldsymbol{X} + \boldsymbol{\mu}] \\\\
	&= \mathrm{V}[\mathbf{A}\boldsymbol{X}] \\\\
	&=\mathrm{E}[(\mathbf{A}\boldsymbol{X} - \mathrm{E}[\mathbf{A}\boldsymbol{X}])(\mathbf{A}\boldsymbol{X} - \mathrm{E}[\mathbf{A}\boldsymbol{X}])^{\mathsf{T}}] \\\\
	&= \mathrm{E}[\mathbf{A}(\boldsymbol{X} - \mathrm{E}[\boldsymbol{X}])(\boldsymbol{X} - \mathrm{E}[\boldsymbol{X}])^{\mathsf{T}}\mathbf{A}^{\mathsf{T}}] \\\\
	&= \mathbf{A}\mathrm{E}[(\boldsymbol{X} - \mathrm{E}[\boldsymbol{X}])(\boldsymbol{X} - \mathrm{E}[\boldsymbol{X}])^{\mathsf{T}}]\mathbf{A}^{\mathsf{T}} \\\\
	&= \mathbf{A}\mathbf{\Sigma}\mathbf{A}^{\mathsf{T}} \\\\
	\end{align}
\\]
となる.
