### 多変量正規分布
\\(\boldsymbol{X}=(X_1, X_2, ..., X_n)^{\mathsf{T}}\\)が,以下の同時確率密度関数に従うとき,\\(\boldsymbol{X}\\)を**多変量正規分布**と言う.
\\[
	\boldsymbol{\mu} = (\mu_1, \mu_2, ..., \mu_n)^{\mathsf{T}} \\\\
	\sigma_{ij} = \mathrm{Cov}(X_i, X_j) \\\\
	\boldsymbol{\Sigma} = \begin{pmatrix}
		\sigma_{11} & \sigma_{12} & \cdots & \sigma_{1n} \\\\
		\sigma_{21} & \sigma_{22} & \cdots & \sigma_{2n} \\\\
		\vdots & \vdots & \ddots & \vdots \\\\
		\sigma_{n1} & \sigma_{n2} & \cdots & \sigma_{nn} \\\\
	\end{pmatrix} \\\\
\\]
として,

\\[
	f\_{\boldsymbol{X}}(\boldsymbol{x}|\boldsymbol{\mu},\boldsymbol{\Sigma})=\Bigr(\frac{1}{2\pi}\Bigl)^{n/2}\frac{1}{|\boldsymbol{\Sigma}|^{1/2}}\exp\Bigl\\{ -\frac{1}{2}(\boldsymbol{x}-\boldsymbol{\mu})^{\mathsf{T}\}\boldsymbol{\Sigma}^{-1}(\boldsymbol{x}-\boldsymbol{\mu}) \Bigr\\}
\\]
