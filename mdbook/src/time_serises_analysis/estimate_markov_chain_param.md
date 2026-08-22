### マルコフ連鎖のパラメータ推定
以下のような状態が\\(n \in \mathbb{N}^+\\)ある推移確率行列を持つ,マルコフ連鎖を考える.

\\[
	\mathbf{Q} = \begin{pmatrix}
		\theta\_{11} & \theta\_{12} & \cdots & \theta_{1n} \\\\
		\theta\_{21} & \theta\_{22} & \cdots & \theta_{2n} \\\\
		\vdots & \vdots & \ddots & \vdots \\\\
		\theta\_{n1} & \theta\_{n2} & \cdots & \theta_{nn} \\\\
	\end{pmatrix}, \sum^n\_{j=1} \theta\_{ij} = 1
\\]

この行列に従う確率変数を\\(X_t, t \geq 0, t \in \mathbb{N}\\)として,\\(t\\)に関しての実現値を観察できたとする.   
では,実現値が状態\\(i\\)から状態\\(j\\)に変わった回数をそれぞれ数えてそこから\\(\theta\_{ij}\\)を推定する.  
例えば状態\\(i\\)からの変化の回数を\\(N_{i}\\)として,状態\\(i\\)から状態\\(j\\)に変わった回数を\\(N_{ij}\\)とする.
\\(\sum^n\_{j=1} N\_{ij} = N_{i} \\)である.   
状態\\(i\\)からの変化が何回起こるかの確率分布\\(\mathrm{P}(N_{i1}=n_{i1},N_{i2}=n_{i2},...,N_{in}=n_{in})\\)は多項分布\\(Multi(N_i,\theta_{i1},\theta_{i2},...,\theta_{in})\\)に従う.
\\[
	\mathrm{P}(N_{i1}=n_{i1},N_{i2}=n_{i2},...,N_{in}=n_{in}) = \frac{N_i!}{n_{i1}!n_{i2}!\cdots n_{in}!} \prod^n_{j=1} \theta\_{ij}^{n_{ij}}
\\]

から,\\(\boldsymbol{\theta} = (\theta\_{11}, \theta\_{12}, ..., \theta\_{nn})\\)として,尤度関数は,
\\[
	\mathrm{L}(\boldsymbol{\theta}|\boldsymbol{N})=\prod^n_{i=1}\mathrm{P}(N_{i1}=n_{i1},N_{i2}=n_{i2},...,N_{in}=n_{in})
\\]
\\(\mathrm{L}(\boldsymbol{\theta}|\boldsymbol{N})\\)を最大にする\\(\theta\_{ij}\\)が,\\(\theta\_{ij}\\)の最尤推定量\\(\hat{\theta}\_{ij}\\).
\\[
\begin{align}
\mathrm{l}(\boldsymbol{\theta}|\boldsymbol{N})&=\log\mathrm{L}(\boldsymbol{\theta}|\boldsymbol{N}) \\\\
&=\sum^n_{i=1}\log \Bigl(\frac{N_i!}{n_{i1}!n_{i2}!\cdots n_{in}!} \prod^n_{j=1} \theta\_{ij}^{n_{ij}} \Bigr)
\end{align}
\\]


\\(\sum^n\_{j=1} \theta\_{ij} = 1\\)という制約があり,それが\\(i\\)列のみの制約なので,ラグランジュの未定乗数法を使い,
\\[
	\mathrm{H}(\theta_{i1},\theta_{i2},...,\theta_{in},\lambda |\boldsymbol{N}) = \log \Bigl(\frac{N_i!}{n_{i1}!n_{i2}!\cdots n_{in}!} \prod^n_{j=1} \theta\_{ij}^{n_{ij}} \Bigr) - \lambda( 1 - \sum^n\_{j=1} \theta\_{ij} ) \\\\
\\]
として,
\\[
	\frac{\partial \mathrm{H}}{\partial \theta_{ij}} = 0
\\]
を満たす,\\(\theta_{ij}\\)が\\(\mathrm{L}\\)を最大化する\\(\theta_{ij}\\).

\\[
\begin{align}
	\frac{\partial \mathrm{H}}{\partial \theta_{ij}} &= \frac{n_{ij}}{\theta_{ij}} + \lambda \\\\
	&=0
\end{align}
\\]
から,

\\[
	\lambda = - \frac{n_{ij}}{\theta_{ij}}
\\]

制約条件に当てはめて,
\\[
\begin{align}
	\sum^n_{j=1} {\theta_{ij}} &= \sum^n_{j=1} - \frac{\lambda}{n_{ij}} = 1 \\\\
	\lambda &= - \sum^n_{j=1} {n_{ij}} = -N_i
\end{align}
\\]

より,
\\[
	\theta_{ij} = -\frac{n_{ij}}{\lambda} = \frac{n_{ij}}{N_i}
\\]

となり,最尤推定量は
\\[
	\hat{\theta}\_{ij} = \frac{n\_{ij}}{N_i}
\\]
