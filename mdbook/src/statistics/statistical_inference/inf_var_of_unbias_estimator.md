## 不偏推定量の分散の下限
不偏推定量は分散が小さい程良い.なので,その下限を調べる.

\\(\\{X_i\\}\\)を確率密度関数&thinsp;\\(f(x:\theta)\\)に従う,無作為標本とする.
まず,母数が1次元の場合を考える.

\\(\mathbf{X}=(X_0,X_1,\dots,X_n)\\)と表現し,同時確率密度関数を\\(f _{\mathbf{X}}(\mathbf{x}:\theta)\\)と書く.
無作為標本は独立な確率変数なので,
\\[
	f _{\mathbf{X}}(\mathbf{x};\theta) = \prod^n _{i=1} f_X(x _i:\theta)
\\]
となる.

\\(\hat{\theta}(\mathbf{X})\\)を\\(\theta\\)の不偏推定量とする.この分散は,
\\[
	{\rm var}(\hat{\theta}) = E[(\hat{\theta}(\mathbf{X})-\theta)^2]
\\]
とある実数値関数,\\(g(\mathbf{X})\\)を用意すると,Cauchy-Schwarzの不等式より,
\\[
	E[(\hat{\theta}(\mathbf{X})-\theta)^2]E[(g(\mathbf{X}))^2] \geq E[(\hat{\theta}(\mathbf{X})-\theta) \cdot g(\mathbf{X})]^2 \\\\
	E[(\hat{\theta}(\mathbf{X})-\theta)^2] \geq \frac{E[(\hat{\theta}(\mathbf{X})-\theta) \cdot g(\mathbf{X})]^2}{E[(g(\mathbf{X}))^2]}
\\]
となり,下限が得られる.であるので,この\\(g(\mathbf{X})\\)を得たい.
この下限を得るための定理が**クラメール-ラオの不等式**(Cramer-Rao's inequality)である.

### クラメール-ラオの不等式
以下を仮定する.
1. \\(f_{\mathbf{X}}(\mathbf{x}:\theta)\\)の台\\(\\{\mathbf{x}|f_{\mathbf{X}}(\mathbf{x};\theta) > 0\\}\\)は\\(\theta\\)に依存しない.
1. \\(f_{\mathbf{X}}(\mathbf{x}:\theta)\\)は\\(\theta\\)に関して2階まで微分可能で,\\(k=1,2\\)に対して,
   \\[
   \frac{d^k}{d\theta^k} \int _{\mathbf{\Omega}} f _{\mathbf{X}}(\mathbf{x}:\theta) d\mathbf{x} = \int _{\mathbf{\Omega}} \frac{\partial^k}{\partial \theta^k} f _{\mathbf{X}}(\mathbf{x}:\theta) d\mathbf{x}
   \\]
   が成立する.
1. すべての\\(\theta\\)に対して,
   \\[
   0 < E \left[\left\\{\frac{\partial}{\partial \theta} \log f _{X}(x:\theta)\right\\}^2 \right] < \infty
   \\]

1. 以下が成立する.
   \\[
   \frac{d}{d \theta} \int _{\mathbf{\Omega}} \hat{\theta} f _{\mathbf{X}}(\mathbf{x}:\theta) d\mathbf{x} = \int _{\mathbf{\Omega}} \hat{\theta} \frac{\partial}{\partial \theta} f _{\mathbf{X}}(\mathbf{x}:\theta) d\mathbf{x}
   \\]
上記の仮定の下で,以下が成立する.
\\[
	{\rm var}(\hat{\theta}) \geq \frac{1}{n E \left[ \left(\displaystyle \frac{\partial \log f _{\mathbf{X}}(\mathbf{x}:\theta)}{\partial \theta} \right)^2 \right]}
\\]
  上記,不等式をクラメール-ラオの不等式という.

- 証明
  \\[
  \begin{align}
  E\left[\left(\frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)^2\right] &= E\left[\left(\frac{\partial}{\partial \theta} \log \prod^n _{i=1} f_X(x _i:\theta)\right)^2\right] \\\\
  &= E\left[\left(\sum^n _{i=1} \frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right)^2\right] \\\\
  &= E\left[\sum^n _{i=1} \left(\frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right)^2 + \sum^n _{i=1} \sum^n _{j=1,i \not= j} \left( \frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right)\left(\frac{\partial}{\partial \theta} \log f_X(x _j:\theta)\right) \right] \\\\
  &= E\left[\sum^n _{i=1} \left(\frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right)^2 \right] + \sum^n _{i=1} \sum^n _{j=1,i \not= j} E\left[\left( \frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right)\left(\frac{\partial}{\partial \theta} \log f_X(x _j:\theta)\right) \right] \\\\
  &= E\left[\sum^n _{i=1} \left(\frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right)^2 \right] + \sum^n _{i=1} \sum^n _{j=1,i \not= j} E\left[\left( \frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right) \right] E\left[\left(\frac{\partial}{\partial \theta} \log f_X(x _j:\theta)\right) \right]
  \end{align}
  \\]
  最後は,確率変数の独立であることと確率変数の変数変換後も独立を保つから得られる.

  \\[
  \begin{align}
  E\left[\left( \frac{\partial}{\partial \theta} \log f_X(x:\theta)\right) \right] &= \int_{\Omega} \left( \frac{\partial}{\partial \theta} \log f_X(x:\theta)\right) f_X(x:\theta) dx \\\\
  &= \int_{\Omega} \left(\frac{\partial}{\partial \theta} f_X(x:\theta) \right) \frac{1}{f_X(x:\theta)} f_X(x:\theta) dx \\\\
  &= \frac{\partial}{\partial \theta} \int_{\Omega} f_X(x:\theta) dx \\\\
  &= \frac{\partial}{\partial \theta} 1 = 0
  \end{align}
  \\]
  から,
  \\[
  \begin{align}
  E\left[\left(\frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)^2\right] &= E\left[\sum^n _{i=1} \left(\frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right)^2 \right] \\\\
  &= n E\left[\left(\frac{\partial}{\partial \theta} \log f_X(x:\theta)\right)^2 \right]
  \end{align}
  \\]

  Cauchy-Schwarzの不等式より,
  \\[
  	E[(\hat{\theta}(\mathbf{X})-\theta)^2] \geq \frac{E\left[(\hat{\theta}(\mathbf{X})-\theta) \cdot \left(\displaystyle \frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)\right]^2}{E\left[\left(\displaystyle \frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)^2 \right]}
  \\]
  \\[
  \begin{align}
  E\left[(\hat{\theta}(\mathbf{X})-\theta) \cdot \left(\displaystyle \frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)\right] &= E\left[\hat{\theta}(\mathbf{X})\left(\displaystyle \frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)\right]-\theta E\left[\displaystyle \frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right] \\\\
  &= E\left[\hat{\theta}(\mathbf{X})\left(\displaystyle \frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)\right] - \theta E\left[ \sum ^n _{i=1} \left(\frac{\partial}{\partial \theta} \log f_X(x _i:\theta)\right) \right] \\\\
  &= E\left[\hat{\theta}(\mathbf{X})\left(\displaystyle \frac{\partial}{\partial \theta} \log f _{\mathbf{X}}(\mathbf{x}:\theta)\right)\right] - n \theta E\left[\frac{\partial}{\partial \theta} \log f _X (x:\theta) \right] \\\\
  &= E\left[\hat{\theta}(\mathbf{X})\left(\displaystyle \frac{\partial}{\partial \theta} \log f _{\mathbf{X}}(\mathbf{x}:\theta)\right)\right] \\\\
  &= \int _{\mathbf{\Omega}} \hat{\theta}(\mathbf{x}) \left(\displaystyle \frac{\partial}{\partial \theta} \log f _{\mathbf{X}}(\mathbf{x}:\theta)\right) f _{\mathbf{X}}(\mathbf{x}:\theta)  d\mathbf{x} \\\\
  &= \int _{\mathbf{\Omega}} \hat{\theta}(\mathbf{x}) \displaystyle \frac{1}{f _{\mathbf{X}}(\mathbf{x}:\theta)} \left(\frac{\partial}{\partial \theta} f _{\mathbf{X}}(\mathbf{x}:\theta)  \right)  f _{\mathbf{X}}(\mathbf{x}:\theta) d\mathbf{x} \\\\
  &= \int _{\mathbf{\Omega}} \hat{\theta}(\mathbf{x}) \displaystyle \left(\frac{\partial}{\partial \theta} f _{\mathbf{X}}(\mathbf{x}:\theta)  \right) d\mathbf{x} \\\\
  &= \frac{\partial}{\partial \theta} \int _{\mathbf{\Omega}} \hat{\theta}(\mathbf{x}) f _{\mathbf{X}}(\mathbf{x}:\theta) d\mathbf{x} \\\\
  &= \frac{\partial}{\partial \theta} \theta = 1
  \end{align}
  \\]
  から,

  \\[
  E[(\hat{\theta}(\mathbf{X})-\theta)^2] \geq \frac{1}{E\left[\left(\displaystyle \frac{\partial}{\partial \theta} \log f_{\mathbf{X}}(\mathbf{x}:\theta)\right)^2 \right]} = \frac{1}{n E\left[\left(\displaystyle \frac{\partial}{\partial \theta} \log f_{X}(x:\theta)\right)^2 \right]}
  \\]

### スコア関数とフィッシャー情報量
\\[
	{\mathscr S} _{\mathbf{X}}(\theta,\mathbf{X}) = \frac{\partial}{\partial \theta} \log f _{\mathbf{X}}(\mathbf{x}:\theta)
\\]
これを**スコア関数**(score function)という.このスコア関数の2乗の期待値
\\[
	{\mathscr I} _{\mathbf{X}}(\theta) = E[\\{{\mathscr S}  _{\mathbf{X}}(\theta,\mathbf{X})\\}^2] = E\left[\left(\frac{\partial }{\partial \theta} \log f _{\mathbf{X}} (\mathbf{X}:\theta) \right)^2 \right]
\\]
を**フィッシャー情報量**(Fisher information)という.

### フィッシャー情報量の性質
フィッシャー情報量の性質は,以下の性質が成り立つ.

1. \\( E[{\mathscr S}_{X}(\theta,X)] = 0 \\)
1. \\({\mathscr I} _{\mathbf{X}}(\theta) = n {\mathscr I} _{X}(\theta) \\)
1. \\(\displaystyle {\mathscr I} _{X}(\theta) = -E\left[ \frac{\partial^2}{\partial \theta^2} \log f_X (X : \theta) \right] \\)

- 証明  
  1,2はクラメール-ラオの不等式の証明で得られる.

  3は,
  \\[
  \begin{align}
  \frac{\partial^2}{\partial \theta^2} \log f_X (x : \theta) &= \frac{\partial}{\partial \theta}\left(\frac{1}{f _X(x:\theta)} \left(\frac{\partial}{\partial \theta} f_X(x:\theta) \right) \right) \\\\
  &= -\left(\frac{1}{f _X(x:\theta)^2} \right) \left(\frac{\partial}{\partial \theta} f _X(x:\theta) \right)^2 + \frac{1}{f _X(x:\theta)} \left( \frac{\partial ^2}{\partial \theta ^2} f _X(x:\theta) \right) \\\\
  &= - \left(\frac{\partial}{\partial \theta} \log f_X(x:\theta) \right)^2 + \frac{1}{f _X(x:\theta)} \left( \frac{\partial ^2}{\partial \theta ^2} f _X(x:\theta) \right)
  \end{align}
  \\]
  から,
  \\[
  \begin{align}
  E\left[ \frac{\partial^2}{\partial \theta^2} \log f_X (X : \theta) \right] &= - E\left[ \left(\frac{\partial}{\partial \theta} \log f_X(X:\theta) \right)^2 \right] + E \left[ \frac{1}{f _X(X:\theta)} \left( \frac{\partial ^2}{\partial \theta ^2} f _X(X:\theta) \right) \right] \\\\
  \end{align}
  \\]
  \\[
  \begin{align}
  E \left[ \frac{1}{f _X(X:\theta)} \left( \frac{\partial ^2}{\partial \theta ^2} f _X(X:\theta) \right) \right] &= \int _{\Omega} \frac{1}{f _X(X:\theta)} \left( \frac{\partial ^2}{\partial \theta ^2} f _X(X:\theta) \right) f _X(X:\theta) dx \\\\
  &= \int _{\Omega} \frac{\partial ^2}{\partial \theta ^2} f _X(X:\theta) dx \\\\
  &= \frac{\partial ^2}{\partial \theta ^2} \int _{\Omega} f _X(X:\theta) dx = 0
  \end{align}
  \\]
  より,
  \\[
  E\left[ \left(\frac{\partial}{\partial \theta} \log f_X(X:\theta) \right)^2 \right] = {\mathscr I} _{X}(\theta) = -E\left[ \frac{\partial^2}{\partial \theta^2} \log f_X (X : \theta) \right]
  \\]
