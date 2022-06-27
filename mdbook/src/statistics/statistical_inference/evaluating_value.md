## 各種評価値

### 不偏性
任意の\\(\theta \in \Theta\\)に対して,推定量\\(\hat{\theta}\\)の平均値の\\(\theta\\)の近さを,
**不偏性**(unbiasedness)と言う.
\\[
	Bias(\hat{\theta}(\mathbf{X})) = E[\hat{\theta}(\mathbf{X})] - \theta
\\]
を**バイアス**(bias)といい,
\\[
	E[\hat{\theta}(\mathbf{X})] = \theta
\\]
が成り立つ時,\\(\hat{\theta}\\)を\\(\theta\\)の**不偏推定量**(unbiasedness estimator)と言う.

### 有効性
不偏推定量の分散の小ささを**有効性**(efficiency)と言う.
\\(\theta\\)の2つの不偏推定量\\(\hat{\theta}_1,\hat{\theta}_2\\)に対して,
\\[
	{\rm var}(\hat{\theta}_1(\mathbf{X})) < {\rm var}(\hat{\theta}_2(\mathbf{X}))
\\]
であるとき,\\(\hat{\theta}_1\\)は\\(\hat{\theta}_2\\)よりも**有効**(efficient)であると言う.

### 一致性
\\(\theta\\)の推定量\\(\\{\hat{\theta}_n\\} _{i \in \mathbb{N} _+,i \leq n}\\)が,
\\(\theta\\)に確率収束することを,**一致性**(consistency)という.
任意の\\(\varepsilon >0\\)に対して,
\\[
	\lim _{n \to \infty} P(|\hat{\theta}_n(\mathbf{X}) - \theta| > \varepsilon) = 0
\\]
が成立するとき,\\(\\{\hat{\theta}_n\\}\\)を\\(\theta\\)の**一致推定量**(consistent estimator)という.

### 平均2乗誤差
推定量の散らばりを評価するには,推定量の分散を取れば良い.分散が小さい推定量が良い推定量となる.
\\[
	{\rm var}(\hat{\theta}) = E[\\{\hat{\theta}(\mathbf{X}) - E[\hat{\theta}(\mathbf{X})]\\}^2]
\\]
バイアスと分散が両方が小さいほうが良いが,片方が大きいことがある.そこで,推定量と母数の距離の平均値で
推定量の良さを評価する.
\\[
	{\rm MSE}(\theta, \hat{\theta}) = E[(\hat{\theta}(\mathbf{X})-\theta)^2]
\\]
を
平均2乗誤差(mean squared error)という.
\\[
  \begin{align}
  {\rm MSE}(\theta, \hat{\theta}) &= E[(\hat{\theta}(\mathbf{X})-\theta)^2] \\\\
  =& E[((\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])-(\theta-E[\hat{\theta}(\mathbf{X})]))^2] \\\\
  =& E[(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])^2-2(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])(\theta-E[\hat{\theta}(\mathbf{X})])+(\theta-E[\hat{\theta}(\mathbf{X})])^2] \\\\
  =& E[(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])^2]+E[\theta^2-2 \theta E[\hat{\theta}(\mathbf{X})] + E[\hat{\theta}(\mathbf{X})]^2 - \\\\
   & 2(\theta \hat{\theta}(\mathbf{X}) - \theta E[\hat{\theta}(\mathbf{X})] - \hat{\theta}(\mathbf{X})E[\hat{\theta}(\mathbf{X})] + E[\hat{\theta}(\mathbf{X})]^2)] \\\\
  =& E[(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])^2] + E[\theta^2 - E[\hat{\theta}(\mathbf{X})]^2 - 2\theta \hat{\theta}(\mathbf{X}) + 2\hat{\theta}(\mathbf{X})E[\hat{\theta}(\mathbf{X})]] \\\\
  =& E[(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])^2] + \theta^2 - E[\hat{\theta}(\mathbf{X})]^2 - 2\theta E[\hat{\theta}(\mathbf{X})]+ 2E[\hat{\theta}(\mathbf{X})E[\hat{\theta}(\mathbf{X})]] \\\\
  =& E[(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])^2] + \theta^2 - E[\hat{\theta}(\mathbf{X})]^2 - 2\theta E[\hat{\theta}(\mathbf{X})]+ 2E[\hat{\theta}(\mathbf{X})]^2 \\\\
  =& E[(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])^2] + \theta^2 - 2\theta E[\hat{\theta}(\mathbf{X})] + E[\hat{\theta}(\mathbf{X})]^2 \\\\
  =& E[(\hat{\theta}(\mathbf{X})-E[\hat{\theta}(\mathbf{X})])^2] + (E[\hat{\theta}(\mathbf{X})] - \theta)^2\\\\
  =& {\rm var}(\hat{\theta}(\mathbf{X})) + Bias(\hat{\theta}(\mathbf{X}))^2
  \end{align}
\\]
 となり,MSEは分散とバイアスの両方を考慮している評価値となる.

### 線形推定量
とある平均\\(\mu\\),分散\\(\sigma^2\\)のとある分布を\\(F(\mu,\sigma^2)\\)と表した時,
この分布から得られる無作為標本を,
\\[
	\\{X_i\\}, {\scriptsize \mathit i.i.d.} \sim F(\mu,\sigma^2)
\\]
と表す.\\(\mu\\)の推定量として\\(\\{X_i\\}\\)の線形結合&thinsp;\\( \hat{\mu} _c = \sum ^{n} _{i=1} c _i X _i \\)
を考えて,\\(\\{X_i\\}\\)の線形推定量という.
その期待値は,
\\[
E[\hat{\mu} _c] = E\left[ \sum ^{n} _{i=1} c _i X _i \right] = \sum ^{n} _{i=1} c _i E[ X _i ] = \sum ^{n} _{i=1} c _i \mu
\\]
なので,
\\[
	Bias(\hat{\mu} _c) = E[\hat{\mu} _c] - \mu = \sum ^{n} _{i=1} c _i \mu - \mu = (\sum ^{n} _{i=1} c _i  - 1)\mu
\\]
ここで,線形推定量が不偏推定量であるためには,\\(Bias(\hat{\mu} _c) = 0\\)でないといけないので,
\\(\sum ^{n} _{i=1} c _i = 1\\)が要請される.
分散は,
\\[
  \begin{align}
  {\rm var}(\hat{\mu} _c) =& E[(\hat{\mu} _c - E[\hat{\mu} _c])^2)] \\\\
  =& E\left[\left(\sum ^{n} _{i=1} c _i X _i - E\left[\sum ^{n} _{i=1} c _i X _i\right]\right)^2\right] \\\\
  =& E\left[\left(\sum ^{n} _{i=1} c _i X _i - \sum ^{n} _{i=1} c _i E[ X _i ]\right)^2\right] \\\\
  =& E\left[\left(\sum ^{n} _{i=1} c _i (X _i - E[ X _i ])\right)^2\right] \\\\
  =& E\left[\left(\sum ^{n} _{i=1} c _i (X _i - \mu)\right)^2\right] \\\\
  =& \sum ^{n} _{i=1} {c _i}^2 \sigma^2
  \end{align}
\\]

### 最良線形不偏推定量
線形で不偏な推定量の中で分散を最小にする推定量を,**最良線形不偏推定量**(best linear unbiased estimator, BLUE)という.
前述の&thinsp;\\(\hat{\mu} _c\\)に置いて,不偏になる条件\\(\sum ^{n} _{i=1} c _i = 1\\)の下で,
\\({\rm var}(\hat{\mu} _c) = \sum ^{n} _{i=1} {c _i}^2 \sigma^2\\)が最小になる\\(c_i\\)は,ラグランジュの未定乗数法を用いると求められる.
\\(\mathbf{c}=(c_1,c_2,\dots,c_n)\\)と置き,ラグランジュ関数を,
\\[
	{\mathscr L}(\mathbf{c},\lambda) =  \sum ^{n} _{i=1} {c _i}^2 \sigma^2 - \lambda \left\\{ \sum ^{n} _{i=1} c _i - 1 \right\\}
\\]
とする.これを各変数について便微分すると,
\\[
	\left\\{
	\begin{array}{ll}
		\sum ^{n} _{i=1} c _i - 1 &= 0 \\\\
		\displaystyle \frac{\partial}{\partial c_i} \sum ^{n} _{i=1} {c _i}^2 \sigma^2 - \lambda \frac{\partial}{\partial c_i} \sum ^{n} _{i=1} c _i &= 2c_i - \lambda = 0
	\end{array}
	\right.
\\]
から,\\(c_i = \frac{\lambda}{2}\\)となる.これから,\\(\sum ^{n} _{i=1} c _i - 1 = 0\\)に代入すると,\\(c _i = \frac{1}{n}\\).
この結果より,
\\[
	\hat{\mu} _c = \sum ^{n} _{i=1} c _i X _i = \sum ^{n} _{i=1} \frac{1}{n} X _i = \overline{X}
\\]
となり,標本平均が最良線形不偏推定量となる.
