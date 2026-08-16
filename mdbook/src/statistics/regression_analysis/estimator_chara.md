## 回帰係数の推定値の性質
### 残差平方和
測定値と予測値の差を**残差**という.
\\[
	r_i = y_i - \boldsymbol{x}_i^T\hat{\boldsymbol{\beta}}
\\]

残差は確率変数の実現値である.
\\[
	R_i = Y_i - \boldsymbol{x}_i^T\hat{\boldsymbol{\beta}}
\\]

\\(\boldsymbol{R}=(R_0,R_1,\cdots,R_n)^T\\)の平均と分散は

\\[
\begin{align}
	\mathrm{E}[\boldsymbol{R}] &= \mathrm{E}[\boldsymbol{Y} - \mathbf{X}\hat{\boldsymbol{\beta}}] \\\\
		&= \mathrm{E}[\mathbf{X}\boldsymbol{\beta} + \boldsymbol{E}] - \mathbf{X}\mathrm{E}[\hat{\boldsymbol{\beta}}] \\\\
		&= \mathbf{X}\boldsymbol{\beta} + \mathrm{E}[\boldsymbol{E}] - \mathbf{X}\boldsymbol{\beta} \\\\
		&= \boldsymbol{0}
\end{align}
\\]

\\[
\begin{align}
	\mathrm{V}[\boldsymbol{R}] &= \mathrm{E}[(\boldsymbol{R} - \mathrm{E}[\boldsymbol{R}])^2] \\\\
		&= \mathrm{E}[\boldsymbol{R}^2] \\\\
		&= \mathrm{E}[(\boldsymbol{Y} - \mathbf{X}\hat{\boldsymbol{\beta}})^T(\boldsymbol{Y} - \mathbf{X}\hat{\boldsymbol{\beta}})] \\\\
		&= \mathrm{E}[(\boldsymbol{Y} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y})^T(\boldsymbol{Y} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y})]
\end{align}
\\]

\\[
	(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)^T = \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T \\\\
	(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T) = \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T \\\\
\\]
\\[
\begin{align}
(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T) &= \mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T  +  \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T  \\\\
	&= \mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T
\end{align}
\\]
を利用して,
\\[
\begin{align}
(\boldsymbol{Y} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y})^T(\boldsymbol{Y} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y}) &= \boldsymbol{Y}^T\boldsymbol{Y} - \boldsymbol{Y}^T(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{Y} - \boldsymbol{Y}^T(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{Y} + \boldsymbol{Y}^T\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y} \\\\
	&= \boldsymbol{Y}^T\boldsymbol{Y} - \boldsymbol{Y}^T(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{Y} \\\\
	&= \boldsymbol{Y}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T + \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{Y} - \boldsymbol{Y}^T(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{Y} \\\\
	&= \boldsymbol{Y}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T) \boldsymbol{Y}
\end{align}
\\]

\\[
\begin{align}
\boldsymbol{Y}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T) \boldsymbol{Y} &= (\mathbf{X}\boldsymbol{\beta}+\boldsymbol{E})^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T) (\mathbf{X}\boldsymbol{\beta}+\boldsymbol{E}) \\\\
	&= (\boldsymbol{\beta}^T\mathbf{X}^T)(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\mathbf{X}\boldsymbol{\beta} + \boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\mathbf{X}\boldsymbol{\beta} + (\mathbf{X}\boldsymbol{\beta})^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E} + \boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E} \\\\
	&= \boldsymbol{\beta}^T(\mathbf{X}^T - \mathbf{X}^T\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\mathbf{X}\boldsymbol{\beta} + \boldsymbol{E}^T(\mathbf{X} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{X})\boldsymbol{\beta}+\boldsymbol{\beta}^T(\mathbf{X}^T - \mathbf{X}^T\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E} + \boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E} \\\\
	&= \boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E}
\end{align}
\\]

から
\\[
\begin{align}
	\mathrm{V}[\boldsymbol{R}] &= \mathrm{E}[\boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E}] \\\\
\end{align}
\\]

\\(\boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E}\\)はスカラ値である. 実際\\(\boldsymbol{E} \in \mathbb{R}^{n \times 1}, \mathbf{X} \in \mathbb{R}^{n \times k+1} \\)から
\\[
(\underbrace{\mathbf{X}}_{n \times k+1}
	(\underbrace{\mathbf{X}^T}\_{k+1 \times n}
	\underbrace{\mathbf{X}}\_{n \times k+1})^{-1}\underbrace{\mathbf{X}^T}\_{k+1 \times n}) = \underbrace{\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T}\_{n \times n} \\\\
	\underbrace{\boldsymbol{E}^T}\_{1 \times n} \underbrace{\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T}\_{n \times n} \underbrace{\boldsymbol{E}}\_{n \times 1} \in \mathbb{R}^{1 \times 1}
\\]
なので,
\\[
\begin{align}
	\boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E} = \mathrm{tr}(\boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E})
\end{align}
\\]
トレースの巡回性
\\[
\mathrm{tr}(\mathbf{ABC}) = \mathrm{tr}(\mathbf{BCA}) = \mathrm{tr}(\mathbf{CAB})
\\]
から

\\[
\mathrm{tr}(\boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E}) = \mathrm{tr}((\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{EE}^T)
\\]

また,とある確率変数行列を\\(\mathbf{X} = (X_{ij}), i,j,n \in \mathbb{N}^{+}, i,j \leq n\\)として,
\\[
	\mathrm{E}[\mathrm{tr}(\mathbf{X})] = \mathrm{tr}(\mathrm{E}[\mathbf{X}])
\\]

となるので,
\\[
\begin{align}
\mathrm{E}[\boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E}] &= \mathrm{E}[ \mathrm{tr}(\boldsymbol{E}^T(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{E})]\\\\
&= \mathrm{E}[ \mathrm{tr}((\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{EE}^{\mathsf{T}})] \\\\
&= \mathrm{tr}(\mathrm{E}[(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\boldsymbol{EE}^{\mathsf{T}}]) \\\\
&= \mathrm{tr}((\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\mathrm{E}[\boldsymbol{EE}^{\mathsf{T}}]) \\\\
&= \mathrm{tr}((\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\sigma^2\mathbf{I}) \\\\
&= \mathrm{tr}(\mathbf{I} - \mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T) \sigma^2 \\\\
&= \\{\mathrm{tr}(\mathbf{I}_n) - \mathrm{tr}(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T)\\} \sigma^2 \\\\
\end{align}
\\]

\\[
\begin{align}
	\mathrm{tr}(\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T) &= \mathrm{tr}((\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{X}) \\\\
	&= \mathrm{tr}(\mathbf{I}_{k+1}) = k+1
\end{align}
\\]

なので,
\\[
	\mathrm{V}[\boldsymbol{R}] = (n - (k+1))\sigma^2
\\]

改めて,
\\[
	RSS_{k+1} = \boldsymbol{R}^2 = (\boldsymbol{Y} - \mathbf{X}\hat{\boldsymbol{\beta}})^{\mathsf{T}}(\boldsymbol{Y} - \mathbf{X}\hat{\boldsymbol{\beta}})
\\]
を残差平方和といい,
\\[
	\mathrm{E}[RSS_{k+1}] = (n - k - 1)\sigma^2
\\]
から,\\(\sigma^2\\)の不偏推定量は,
\\[
	\hat{\sigma}^2 = \frac{1}{n-k-1}RSS
\\]
