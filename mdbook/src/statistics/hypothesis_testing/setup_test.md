## 検定方式の立て方
### 単純仮説問題
帰無仮説\\(H_0\\)に対して,対立仮説\\(H_1\\)が一つの要素で構成されるものを単純仮説という
\\[
	H_0:\theta=\theta_0 \\; \mathrm{vs} \\; H_1:\theta=\theta_1
\\]
### 複合仮説問題
帰無仮説\\(H_0\\)に対して,対立仮説\\(H_1\\)が複数の要素で構成されるものを複合仮説という
\\[
	H_0:\theta=\theta_0 \\; \mathrm{vs} \\; H_1:\theta \neq \theta_0
\\]
上記の仮説を両側検定という.
\\[
	H_0:\theta=\theta_0 \\; \mathrm{vs} \\; H_1:\theta > \theta_0 \\\\
	H_0:\theta=\theta_0 \\; \mathrm{vs} \\; H_1:\theta < \theta_0
\\]
上記の仮説を片側検定といい前者を右片側検定,後者を左片側検定と言う.
検定統計量\\(T\\)として,有意水準\\(\alpha\\)としたとき,棄却域と受容域の境界値を棄却限界値いう.
棄却限界値\\(t_{\alpha}\\)は以下の条件を満たす値である.

\\[
\begin{align}
	& P(T \geq t_{\alpha}) = \alpha & \\; 右片側検定 \\\\
	& P(T \leq t_{\alpha}) = \alpha & \\; 左片側検定 \\\\
	& P(T \leq t_{\alpha_{lower}}) = \frac{\alpha}{2}, \\: P(T \geq t_{\alpha_{upper}}) = \frac{\alpha}{2} & \\; 両側検定
\end{align}
\\]
