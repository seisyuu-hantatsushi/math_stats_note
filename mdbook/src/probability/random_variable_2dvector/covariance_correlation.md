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
	{\rm Cov}(aX+b,cY+d) = E[(aX+b-(a\mu_X-b))(cY+d-(c\mu_Y+d))]=E[a(X-\mu_X)c(Y-\mu_Y)]=ac{\rm Cov}(X,Y)
\\]
\\[
	{\rm Corr}(aX+b,cY+d) = \frac{ac{\rm Cov}(X,Y)}{\sqrt{{\rm Var}(aX+b){\rm Var}(bY+d)}} = \frac{ac{\rm Cov}(X,Y)}{|ac| \sqrt{{\rm Var}(X){\rm Var}(Y)}}
\\]
から,共分散は尺度に影響を受けるが,相関係数は尺度に影響を受けない.

### コーシー・シュワルツの不等式
確率変数ベクトル\\(X,Y\\)の同時確率密度関数\\(f_{X,Y}(x,y) > 0\\)で与えられているとき,それに対応する実数値関数\\(g(x),h(x)\\)に対して,
\\(E^{X,Y}[g(X)^2]<\infty,E^{X,Y}[h(Y)^2]<\infty\\)であるならば,
\\[
	E^{X,Y}[g(X)h(Y)]^2 \leq E^{X,Y}[g(X)^2]E^{X,Y}[h(Y)^2]
\\]
が成立する. 等号は\\(g(X) = ah(Y)\\)が成立するときである.
ここで,\\(a\\)は定数である.

- 証明
  まず,
  \\[
   E^{X,Y}[(g(X)-ah(Y))^2] = \int \int (g(x)-ah(x))^2 f_{X,Y}(x,y) dx dy \geq 0
  \\]

  \\[
  \begin{align}
  E^{X,Y}[(g(X)-ah(Y))^2] &= E^{X,Y}[g(X)^2-2ag(X)h(Y)+a^2h(Y)^2] \\\\
  &= E^{X,Y}[g(X)^2]-2aE^{X,Y}[g(X)h(Y)]+a^2E^{X,Y}[h(Y)^2] \geq 0
  \end{align}
  \\]
  上式を\\(a\\)に関する2次関数と考えた時,
  \\[
  F(a) = a^2E^{X,Y}[h(Y)^2]-2aE^{X,Y}[g(X)h(Y)]+E^{X,Y}[g(X)^2]
  \\]
  \\(F(a) \geq 0\\)なので,\\(F(a) = 0\\)としたときの二次方程式の解の判別式は,重解,若しくは虚数解と持つことになるので,
  \\[
	  4E^{X,Y}[g(X)h(Y)]^2-4E^{X,Y}[h(Y)^2]E^{X,Y}[g(X)^2] \leq 0
  \\]
  となり,
  \\[
	  E^{X,Y}[g(X)h(Y)]^2 \leq E^{X,Y}[h(Y)^2]E^{X,Y}[g(X)^2]
  \\]
  となる.等号が成立する時は,\\(g(x)=ah(x)\\)であるときである.

### 相関係数の性質
\\({\rm Corr}(X,Y) > 0\\)のとき**正の相関**と言い,\\({\rm Corr}(X,Y) < 0\\)のとき**負の相関**と言い,\\({\rm Corr}(X,Y) = 0\\)を**無相関**という.

#### 無相関と独立
無相関の時は確率変数は独立とは限らないが,確率変数が独立ならば無相関である.
2つの確率変数\\(X\\)と\\(Y\\)が独立の時,
\\[
{\rm Cov}(X,Y) = E[(X-\mu_X)(Y-\mu_Y)] = E[XY]-E[X\mu_Y]-E[Y\mu_X]+\mu_X\mu_Y = 0
\\]
から,
\\[
	{\rm Corr}(X,Y) = \frac{{\rm Cov}(X,Y)}{\sqrt{{\rm Var}(X){\rm Var}(Y)}} = \frac{0}{\sqrt{{\rm Var}(X){\rm Var}(Y)}} = 0
\\]
であり,無相関になる.

