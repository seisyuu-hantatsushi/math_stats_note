## 十分統計量
確率分布&thinsp;\\(f_X(x:\theta)\\)から得られた無作為標本\\(\\{X_i\\} _{i \in \mathbb{N} _+,i \leq n}\\)を値域にとる
関数\\(T:\mathbb{R}^d \mapsto \mathbb{R}\\)を統計量とする.この統計量から\\(f_X(x:\theta)\\)が再現できるのであれば,
使い勝手が良い.

### 十分統計量
統計量\\(T\\)がパラメータ\\(\theta\\)に関して**十分統計量**(sufficient statistics)とは,
\\(T({\mathbf x}) = t\\)を満たす\\({\mathbf x}\\)と\\(t\\)に対して\\(T({\mathbf X}) = t\\)を
与えたときの\\({\mathbf X} = {\mathbf x}\\)の条件付き確率\\(P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t)\\)
が\\(\theta\\)に依存しないことを言う.

以下の**因数分解定理**(Fisher-Neyman factorization theorem)により,
興味のある統計量が十分統計量であるかを判定できる.

### 因数分解定理
