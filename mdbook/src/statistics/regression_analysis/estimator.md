## 回帰係数の推定
もっとも都合が良い偏回帰係数は
\\[
	| \boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta} |
\\]
を最も小さくする\\(\boldsymbol{\beta}\\)である.
これは,
\\[
	\begin{align}
	h(\boldsymbol{\beta}) &= \sum^n_{i=1} (Y_i - (\beta_{0} + \beta_{1}x_{i1} + \beta_2x_{i2} + \cdots + \beta_{k}x_{ik}))^2 \\\\
	&= (\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta})^T(\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta})
	\end{align}
\\]
を最小にする\\(\boldsymbol{\beta}\\)を求めることであり,これを最小二乗推定量と言う.
\\(h(\boldsymbol{\beta}) \geq 0\\)なので,\\(\frac{\partial h(\boldsymbol{\beta})}{\partial \boldsymbol{\beta}} = 0\\)を満たす\\(\boldsymbol{\beta}\\)が,推定量\\(\hat{\boldsymbol{\beta}}\\)である.

\\[
	\begin{align}
	h(\boldsymbol{\beta}) &= (\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta})^T(\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta}) \\\\
	&= \boldsymbol{Y}^T\boldsymbol{Y}-(\mathbf{X}\boldsymbol{\beta})^T\boldsymbol{Y}-\boldsymbol{Y}^T(\mathbf{X}\boldsymbol{\beta})+(\mathbf{X}\boldsymbol{\beta})^T(\mathbf{X}\boldsymbol{\beta}) \\\\
	&= \boldsymbol{Y}^T\boldsymbol{Y}-2\boldsymbol{\beta}^T\mathbf{X}^T\boldsymbol{Y}+\boldsymbol{\beta}^T\mathbf{X}^T\mathbf{X}\boldsymbol{\beta}
	\end{align}
\\]

\\[
	\begin{align}
	\frac{\partial h(\boldsymbol{\beta})}{\partial \boldsymbol{\beta}} &= -2\mathbf{X}^T\boldsymbol{Y} + ((\mathbf{X}^T\mathbf{X})^T+\mathbf{X}^T\mathbf{X})\boldsymbol{\beta} \\\\
	&= -2\mathbf{X}^T\boldsymbol{Y} + 2(\mathbf{X}^T\mathbf{X})\boldsymbol{\beta} = 0
	\end{align}
\\]

\\(\mathbf{X}^T\mathbf{X}\\)は\\((\mathbf{X}^T\mathbf{X})^{-1}\\)が存在するとして,

\\[
	\begin{align}
	& -2\mathbf{X}^T\boldsymbol{Y} + 2(\mathbf{X}^T\mathbf{X})\boldsymbol{\beta} = 0 \\\\
	& (\mathbf{X}^T\mathbf{X})\boldsymbol{\beta} = \mathbf{X}^T\boldsymbol{Y} \\\\
	& (\mathbf{X}^T\mathbf{X})^{-1}(\mathbf{X}^T\mathbf{X})\boldsymbol{\beta} = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y} \\\\
	& \boldsymbol{\beta} = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y}
	\end{align}
\\]
となり,最小二乗推定量は改めて,
\\[
\hat{\boldsymbol{\beta}} = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y}
\\]
では,改めて\\(\boldsymbol{\beta}\\)の分布を考える.
\\[
	\begin{align}
\hat{\boldsymbol{\beta}} &= (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y} \\\\
&= (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T(\mathbf{X}\boldsymbol{\beta} + \boldsymbol{E}) \\\\
&= \boldsymbol{\beta} + (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{E}
\end{align}
\\]

\\(\boldsymbol{E} \sim N_n(0,\sigma^2\mathbf{I}) \\)なので,
\\[
	\begin{align}
   	\mathrm{E}[\hat{\boldsymbol{\beta}}] &= \mathrm{E}[\boldsymbol{\beta} + (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{E}] \\\\
	&= \boldsymbol{\beta} + (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathrm{E}[\boldsymbol{E}] \\\\
	&= \boldsymbol{\beta}
	\end{align}
\\]

\\[
	\begin{align}
	\mathrm{Cov}(\hat{\boldsymbol{\beta}}) &= \mathrm{E}[(\hat{\boldsymbol{\beta}} - \boldsymbol{\beta})(\hat{\boldsymbol{\beta}} - \boldsymbol{\beta})^T] \\\\
	&= \mathrm{E}[((\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{E} - \boldsymbol{\beta})((\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{E} - \boldsymbol{\beta})^T]
	\end{align}
\\]
