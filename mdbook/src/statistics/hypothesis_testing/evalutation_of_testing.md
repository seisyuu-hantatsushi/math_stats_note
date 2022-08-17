## 検定の評価
設定された検定を評価する方法を考える.
その際検出力関数\\(\beta(\theta)\\)を使って評価を行う.
\\(\Theta_0\\)を帰無仮説\\(H_0\\)の母数の集合,\\(\Theta_1=\Theta_0^c\\)を対立仮説\\(H_1\\)の母数の集合とすると,
検出力関数の定義から,
\\[
	\alpha = \beta(\theta \in \Theta_0), \beta = 1 - \beta(\theta \in \Theta_0^c)
\\]
と第一種の誤りと第二種の誤りとなる.
\\[
	\sup_{\theta \in \Theta_0} \beta(\theta) = \alpha
\\]
は**検定の大きさ**(the size of a test)と言い,帰無仮説\\(H_0\\)に属する母数から計算される第一種の誤りの確率の上限となる.

**有意水準\\(\alpha\\)の検定**(test at the significance level \\(\alpha\\))とは,
\\[
	\sup_{\theta \in \Theta_0} \beta(\theta) = \sup_{\theta \in \Theta_0} P(X \in R:\theta) \leq \alpha
\\]
となるように,棄却域\\(R\\)を設定した検定である.

2つの検定手法\\(T_1\\)と\\(T_2\\)に対して,それぞれ検出力関数を\\(\beta_1(\theta),\beta_2(\theta)\\)とする.
以下を満たす時,\\(T_1\\)は\\(T_2\\)**より強力**という.
1. \\(\forall \theta \in \Theta_0\\)に対して,\\(\beta_1(\theta) \leq \alpha,\beta_2(\theta) \leq \alpha\\)である.
1. \\(\forall \theta \in \Theta_0^c\\)に対して,\\(\beta_1(\theta) \geq \beta_2(\theta)\\)であり,少なくとも1点で不等式が成り立つ.

では,有意水準\\(\alpha\\)の検定内で,もっとも強力な検定を探すことを考える.

### 最強力検定
有意水準\\(\alpha\\)の検定の全体を\\(\mathcal{T} _{\alpha}\\)と表す.
この時検定\\(T \in \mathcal{T} _{\alpha}\\)が**一様最強力検定**とは
1. \\(\beta _T (\theta)\\)を\\(T\\)の検出力関数とすると,\\(\forall \theta \in \Theta_0\\)に対して,\\(\\; \beta _T (\theta) < \alpha \\).
1. \\(\forall S \in \mathcal{T} _{\alpha}\\)の検出力関数\\(\beta _{S}(\theta)\\)とすると,すべての\\(\theta \in \Theta ^{c} _{0}\\)に対して,\\(\beta _{T}(\theta) \geq \beta _{S}(\theta)\\).

