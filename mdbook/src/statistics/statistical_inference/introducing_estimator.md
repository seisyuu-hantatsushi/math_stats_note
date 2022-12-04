## 推定量の導出

### モーメント法
\\(f(x;\boldsymbol{\theta})\\)なる確率変数\\(X\\)に対して,\\(E[X^k]={\mu_k}'(\boldsymbol{\theta})\\)と表されるとする.
\\(\\{X _i\\} _{i \in \mathbb{N} _+,i \leq n} &thinsp; i,i,d \sim f(x;\boldsymbol{\theta})\\)なる無作為標本について,
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
となる同時方程式を,\\(\theta_1,\dots,\theta_k\\)について解くことにより,推定量\\(\hat{\boldsymbol{\theta}}\\)を得る.
これを**モーメント推定量**(moment estimator)という.

### 最尤法
確率変数ベクトル\\(\mathbf{X}=(X_1,\dots,X_n)\\)を同時確率密度関数\\(f_{X}(x:\boldsymbol{\theta})\\)からの無作為標本とする.
\\[
	L(\boldsymbol{\theta}:\mathbf{x}) = \prod^{n} _{i=1} f _{X}(x_i:\boldsymbol{\theta})
\\]
とおく.関数\\(L\\)は\\(\mathbf{x}\\)が特徴を決める(依存する)\\(\boldsymbol{\theta}\\)の関数となる.
この関数を**尤度関数**(likelihood function),**尤度**(likelihood)という.
この関数の対数をとった関数を対数尤度関数と言う.
\\[
	l(\boldsymbol{\theta}:\mathbf{x}) = \sum^{n} _{i=1} \log f _{X}(x_i:\boldsymbol{\theta})
\\]

#### 最尤推定量
尤度関数を最大にする\\(\boldsymbol{\theta}\\)の解\\(\hat{\boldsymbol{\theta}} = \hat{\boldsymbol{\theta}}(\mathbf{X})\\)を**最尤推定量**(maximum likelihood estimator)といい,**MLE**と略す.

\\(\hat{\boldsymbol{\theta}}\\)が最尤推定量とは,
\\[
	\hat{\boldsymbol{\theta}} = \sup _{\boldsymbol{\theta}} L(\boldsymbol{\theta}:\mathbf{x})
\\]
であることである. 尤度関数は確率密度関数なので,最尤推定量\\(\hat{\boldsymbol{\theta}}\\)は,
この母数をとる確率分布が一番母集団に尤もらしい(一番高い確率で似ている)確率分布となる推定量ということである.
尤度関数は確率密度関数なので,
\\[
	\frac{\partial}{\partial \theta _i} L(\boldsymbol{\theta}:\mathbf{x}) = 0 , i=1,\dots,k
\\]
を満たす,\\(\boldsymbol{\theta}\\)がMLEの候補であり,これを**尤度方程式**(likelihood equation)という.
もし,対数尤度関数が各\\(\boldsymbol{\theta}\\)の成分で偏微分可能なら,
\\[
	\frac{\partial}{\partial \theta _i} l(\boldsymbol{\theta}:\mathbf{x}) = \sum ^k _{i=1} \frac{\partial}{\partial \theta _i} \log f _{X}(x_i:\boldsymbol{\theta})
\\]
となり扱いやすい.これを数値計算により解いて,最尤推定量を得る.

### ベイズ法
同時確率密度関数\\(f(\boldsymbol{x}|\boldsymbol{\theta})\\)にて\\(\boldsymbol{\theta}\\)を確率変数とみなして,確率分布を仮定する.
この確率分布を\\(\pi(\boldsymbol{\theta}|\boldsymbol{\xi})\\)と書いて,\\(\boldsymbol{\theta}\\)の事前分布(priordistribution)という.
\\(\boldsymbol{\xi}\\)は事前分布の母数\\(\boldsymbol{\theta}\\)の母数なので,**超母数**(hyper parameter)という.
確率変数\\(\boldsymbol{X}|\boldsymbol{\Theta},\boldsymbol{\Theta}\\)は上述の確率分布に従うので,
\\[
	\left\\{
	\begin{array}{ll}
	\boldsymbol{X}|\boldsymbol{\Theta} &\sim f(\boldsymbol{x}|\boldsymbol{\theta}) \\\\
	\boldsymbol{\Theta} &\sim \pi(\boldsymbol{\theta}|\boldsymbol{\xi})
	\end{array}
	\right.
\\]
と表現できる.このとき,\\(\boldsymbol{X}=\boldsymbol{x}\\)を与えたときの\\(\boldsymbol{\theta}\\)の条件付き分布を\\(\boldsymbol{\theta}\\)の**事後分布**(posterior distribution)といい,
\\[
	\pi(\boldsymbol{\theta}|\boldsymbol{x},\boldsymbol{\xi})=f(\boldsymbol{\theta}|\boldsymbol{x})\pi(\boldsymbol{\theta}|\boldsymbol{\xi})/f_{\Pi}(\boldsymbol{x}|\boldsymbol{\xi})
\\]
で与えられる.ここで,\\(f_{\Pi}(\boldsymbol{x}|\boldsymbol{\xi})\\)は\\(\boldsymbol{X}\\)の周辺分布を表し,
\\[
  f_{\Pi}(\boldsymbol{x}|\boldsymbol{\xi}) = \int f(\boldsymbol{x}|\boldsymbol{\theta})\pi(\boldsymbol{\theta}|\boldsymbol{\xi})d\boldsymbol{\theta}
\\]
で与えられる.すなわち,\\((\boldsymbol{X},\boldsymbol{\Theta})\\)の同時確率密度関数は,
\\[
	f(\boldsymbol{\theta}|\boldsymbol{x})\pi(\boldsymbol{\theta}|\boldsymbol{\xi}) = \pi(\boldsymbol{\theta}|\boldsymbol{x},\boldsymbol{\xi})f_{\Pi}(\boldsymbol{x}|\boldsymbol{\xi})
\\]

ベイズ法は事後分布をから推定量を導く方法で,ここでは事後分布の平均\\(E[\boldsymbol{\Theta}|\boldsymbol{X}]\\)を**ベイズ推定量**(Bayes estimator)という.
事後分布\\(\pi(\boldsymbol{\theta}|\boldsymbol{x},\boldsymbol{\xi})\\)のモードを**ベイズ的最尤推定量**(Bayesian maximun likelihood estimator)という.
\\(\theta\\)に対する十分統計量を\\(T(\boldsymbol{X})\\)とすると,
\\(f(\boldsymbol{x}|\boldsymbol{\theta})=h(\boldsymbol{x})g(T(\boldsymbol{x}|\boldsymbol{\theta}))\\)と書けるので,
\\[
\pi(\boldsymbol{\theta}|\boldsymbol{x},\boldsymbol{\xi}) =\frac{h(\boldsymbol{x})g(T(\boldsymbol{x}|\boldsymbol{\theta}))\pi(\boldsymbol{\theta}|\boldsymbol{\xi})}{\int h(\boldsymbol{x})g(T(\boldsymbol{x}|\boldsymbol{\theta}))\pi(\boldsymbol{\theta}|\boldsymbol{\xi})d\boldsymbol{\theta}} = \frac{g(T(\boldsymbol{x}|\boldsymbol{\theta}))\pi(\boldsymbol{\theta}|\boldsymbol{\xi})}{\int g(T(\boldsymbol{x}|\boldsymbol{\theta}))\pi(\boldsymbol{\theta}|\boldsymbol{\xi})d\boldsymbol{\theta}}
\\]
となる