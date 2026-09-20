#### 回帰係数の推定量の分布
\\(\boldsymbol{E} \sim \mathcal{N}(0,\mathbf{I}_n \sigma^2)\\)とすると,\\(\hat{\boldsymbol{\beta}},\hat{\sigma^2}\\)の推定量の分布は以下のようになる,
\\[
	\hat{\boldsymbol{\beta}} \sim  \mathcal{N}\_{k+1}(\boldsymbol{\beta}, \sigma^2(\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}) \\\\
	\frac{(n-(k+1))\hat{\sigma^2}}{\sigma^2} \sim \chi^2\_{n-(k+1)} \\\\
	\hat{\boldsymbol{\beta}}と\hat{\sigma^2}が独立
\\]

- 証明  
\\(\hat{\boldsymbol{\beta}}(\boldsymbol{Y}) = (\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}}\boldsymbol{Y}\\)   
\\(\boldsymbol{Y} = \mathbf{X}\boldsymbol{\beta} + \boldsymbol{E} \sim \mathcal{N}\_{n}(\mathbf{X}\boldsymbol{\beta},\mathbf{I}_n \sigma^2)\\)から
\\[
\begin{align}
\hat{\boldsymbol{\beta}} = (\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}}\boldsymbol{Y} &\sim \mathcal{N}\_{k+1}((\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}}\mathbf{X}\boldsymbol{\beta}, ((\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}})(\mathbf{I}_n \sigma^2)((\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}})^{\mathsf{T}}) \\\\
&= \mathcal{N}\_{k+1}(\boldsymbol{\beta},\sigma^2(\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1})
\end{align} \\\\
\hat{\sigma}^2 = \frac{1}{n-k-1}RSS\_{k+1}= \frac{1}{n-k-1}(\boldsymbol{Y}-\mathbf{X}\hat{\boldsymbol{\beta}})^{\mathsf{T}}(\boldsymbol{Y}-\mathbf{X}\hat{\boldsymbol{\beta}})
\\]

\\[
\begin{align}
	\frac{(n-(k+1))\hat{\sigma^2}}{\sigma^2} &= \frac{(\boldsymbol{Y}-\mathbf{X}\hat{\boldsymbol{\beta}})^{\mathsf{T}}}{\sigma}\frac{(\boldsymbol{Y}-\mathbf{X}\hat{\boldsymbol{\beta}})}{\sigma}
\end{align}
\\]

\\[
	\mathbf{X}\hat{\boldsymbol{\beta}} \sim \mathcal{N}_n(\mathbf{X}\boldsymbol{\beta},\sigma^2\mathbf{X}(\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}}) \\\\
	\boldsymbol{Y} - \mathbf{X}\hat{\boldsymbol{\beta}} \sim \mathcal{N}_n(\mathbf{X}\boldsymbol{\beta}-\mathbf{X}\boldsymbol{\beta}, \sigma^2(\mathbf{X}(\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}}-\mathbf{I}_n)) =\mathcal{N}_n(\mathbf{0},\sigma^2(\mathbf{X}(\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}}-\mathbf{I}_n)) \\\\
	\frac{(\boldsymbol{Y}-\mathbf{X}\hat{\boldsymbol{\beta}})}{\sigma} \sim \mathcal{N}_n(\mathbf{0},\mathbf{X}(\mathbf{X}^{\mathsf{T}}\mathbf{X})^{-1}\mathbf{X}^{\mathsf{T}}-\mathbf{I}_n)
\\]
