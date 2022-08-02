## 共分散と相関係数
2つの確率変数\\(X\\)と\\(Y\\)が独立でない時,その関係を捉えるために共分散と相関係数を使う.

### 共分散
\\[
	\sigma_{xy} = {\rm Cov}(X,Y) = E[(X-\mu_X)(Y-\mu_Y)]
\\]
を**共分散**(covariance)と言う.

### 相関係数
\\[
	\rho_{xy} = {\rm Corr}(X,Y) = \frac{{\rm Cov}(X,Y)}{\sqrt{{\rm Var}(X){\rm Var}(Y)}} = \frac{\sigma_{xy}}{\sigma_{x}\sigma_{y}}
\\]
を**相関係数**(correlation coefficient)と言う.


\\[
	{\rm Cov}(aX+b,cY+d) = E[(aX+b-(a\mu_X-b))(cY+d-(c\mu_Y+d))]=E[a(X-mu_X)c(Y-\mu_Y)]=ac{\rm Cov}(X,Y)
\\]
\\[
	{\rm Corr}(aX+b,cY+d) = \frac{ac{\rm Cov}(X,Y)}{\sqrt{{\rm Var}(aX+b){\rm Var}(bY+d)}} = \frac{ac{\rm Cov}(X,Y)}{|ac| \sqrt{{\rm Var}(X){\rm Var}(Y)}}
\\]
から,共分散は尺度に影響を受けるが,相関係数は尺度に影響を受けない.
