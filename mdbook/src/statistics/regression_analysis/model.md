## モデルの行列表現
真の値が,以下のようなモデルであったとする.\\(y\\)を応答変数,\\(x_i\\)を説明変数という.
\\[
	y = \beta_{0} + \beta_{1}x_1 + \beta_{2}x_2 + \cdots + \beta_{k}x_k
\\]
しかし,実際の観測値には誤差が伴う.n個の標本を取得したとし,その時伴う誤差を\\(\epsilon_i\\)として,
\\[
	y_i = \beta_{0} + \beta_{1}x_{i1} + \beta_2x_{i2} + \cdots + \beta_{k}x_{ik} + \varepsilon_i 
\\]
と表現する.
\\(\varepsilon_i\\)は正規性を仮定し,\\(\\{E_i\\} _{i \in \mathbb{N} _+,i \leq n} \sim N(0,\sigma^2) \\)の実現値とすると,確率変数

\\[
	Y_i = \beta_{0} + \beta_{1}x_{i1} + \beta_2x_{i2} + \cdots + \beta_{k}x_{ik} + E_i 
\\]
と表現できる. \\(\beta_i\\)は偏回帰係数という.
各実現値や誤差,偏回帰係数をベクトルと行列で表現すると.
\\[
\begin{pmatrix}Y_1 \\\\ Y_2 \\\\ \vdots \\\\ Y_n \end{pmatrix} = \begin{pmatrix} 1 & x_{11} & x_{12} & \cdots & x_{1k}  \\\\
                                  1 & x_{21} & x_{22} & \cdots & x_{2k}  \\\\
                                  \vdots & \vdots & \vdots & \ddots & \vdots  \\\\
                                  1 & x_{n1} & x_{n2} & \cdots & x_{nk} \end{pmatrix} 
								  \begin{pmatrix}\beta_0 \\\\ \beta_1 \\\\ \beta_2 \\\\ \vdots \\\\ \beta_k \end{pmatrix} + \begin{pmatrix}E_1 \\\\ E_2 \\\\ \vdots \\\\ E_n \end{pmatrix}
\\]
それぞれを対応するベクトルと行列を,\\(\boldsymbol{y},\mathbf{X},\boldsymbol{\beta},\boldsymbol{E}\\)とし,
\\[
\boldsymbol{y}=\mathbf{X}\boldsymbol{\beta}+\boldsymbol{E}
\\]
と表現する.
