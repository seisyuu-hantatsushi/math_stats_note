## 回帰係数の推定
### 最小二乗推定量
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

\\(\boldsymbol{E} \sim \mathcal{N}_n(0,\sigma^2\mathbf{I}_n) \\)なので,
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
	&= \mathrm{E}[((\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{E})((\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{E})^T]\\\\
	&= \mathrm{E}[(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{E}\boldsymbol{E}^T\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}] \\\\
	&= (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathrm{E}[\boldsymbol{E}\boldsymbol{E}^T]\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1}\\\\
	& = (\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\sigma^2\mathbf{I}\mathbf{X}(\mathbf{X}^T\mathbf{X})^{-1} \\\\
	& = \sigma^2(\mathbf{X}^T\mathbf{X})^{-1}
	\end{align}
\\]
### 最尤推定量
\\(\boldsymbol{x}_i=(1,x\_{i1},x\_{i2},\cdots,x\_{ik})^T\\)とする,

\\[
	\mathbf{X} =\begin{pmatrix}
	\boldsymbol{x}_1^T \\\\
	\boldsymbol{x}_2^T \\\\
	\vdots \\\\
	\boldsymbol{x}_n^T
	\end{pmatrix}
\\]

\\(Y_i \sim \mathcal{N}(\boldsymbol{x}\_i^T \boldsymbol{\beta}, \sigma^2)\\)より,
\\[
	f_{Y_i}(y_i|\boldsymbol{\beta}) = \frac{1}{\sqrt{2\pi\sigma^2}}\exp(-\frac{1}{2\sigma^2}(y_i-\boldsymbol{x}\_i^T \boldsymbol{\beta})^2)
\\]
同時確率密度関数は,

\\[
\begin{align}
	f_{\boldsymbol{Y}}(\boldsymbol{y}|\boldsymbol{\beta}) &= \prod^n_{i=1} \Bigl\lbrace \frac{1}{\sqrt{2\pi\sigma^2}}\exp(-\frac{1}{2\sigma^2}(y_i-\boldsymbol{x}\_i^T \boldsymbol{\beta})^2) \Bigr\rbrace \\\\
	&= \Biggl(\frac{1}{\sqrt{2\pi\sigma^2}}\Biggr)^n\exp(-\frac{1}{2\sigma^2}\sum^n_{i=1}(y_i-\boldsymbol{x}\_i^T \boldsymbol{\beta})^2) \\\\
	&= \Biggl(\frac{1}{\sqrt{2\pi\sigma^2}}\Biggr)^n\exp(-\frac{1}{2\sigma^2}\sum^n_{i=1}(y_i-\boldsymbol{x}\_i^T \boldsymbol{\beta})^2) \\\\
	&= \Biggl(\frac{1}{\sqrt{2\pi\sigma^2}}\Biggr)^n\exp\Bigl(-\frac{1}{2\sigma^2}(\boldsymbol{y} - \mathbf{X}\boldsymbol{\beta})^T(\boldsymbol{y} - \mathbf{X}\boldsymbol{\beta})\Bigr)
\end{align}
\\]

尤度関数は,
\\[
	L(\boldsymbol{\beta}|\boldsymbol{Y}) = f\_{\boldsymbol{Y}}(\boldsymbol{Y}|\boldsymbol{\beta})
\\]

最尤推定量\\(\hat{\boldsymbol{\beta}}^{MLE}\\)は\\(L\\)を最大にする,\\(\boldsymbol{\beta}\\)
なので,
\\[
	\begin{align}
	l(\boldsymbol{\beta}|\boldsymbol{Y})&=\log L(\boldsymbol{\beta}|\boldsymbol{Y}) \\\\
		&=-\frac{n}{2}(\log 2\pi + \log \sigma^2) -\frac{1}{2\sigma^2} (\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta})^T(\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta})
	\end{align}
\\]
\\(\hat{\boldsymbol{\beta}}^{MLE}\\)は\\(\frac{\partial}{\partial \boldsymbol{\beta}}l(\boldsymbol{\beta}|\boldsymbol{Y}) = 0\\)をみたす\\(\boldsymbol{\beta}\\)

\\[
\begin{align}
	\frac{\partial}{\partial \boldsymbol{\beta}}l(\boldsymbol{\beta}|\boldsymbol{Y}) &= -\frac{1}{2\sigma^2}\frac{\partial}{\partial \boldsymbol{\beta}}(\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta})^T(\boldsymbol{Y} - \mathbf{X}\boldsymbol{\beta}) \\\\
	&= -\frac{1}{2\sigma^2}(-2\mathbf{X}^T\boldsymbol{Y} + 2(\mathbf{X}^T\mathbf{X})\boldsymbol{\beta}) = 0
\end{align}
\\]

から,

\\[
\hat{\boldsymbol{\beta}}=(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\boldsymbol{Y}
\\]

となり,最小二乗推定量と同じになる.
