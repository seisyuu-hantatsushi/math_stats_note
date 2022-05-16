## 十分統計量
確率分布&thinsp;\\(f_X(x:\theta)\\)から得られた無作為標本\\(\\{X_i\\} _{i \in \mathbb{N} _+,i \leq n}\\)を値域にとる
関数\\(T:\mathbb{R}^d \mapsto \mathbb{R}\\)を統計量とする.この統計量から\\(f_X(x:\theta)\\)が再現できるのであれば,
使い勝手が良い.

### 十分統計量
統計量\\(T\\)がパラメータ\\(\theta\\)に関して**十分統計量**(sufficient statistics)とは,
\\(T({\mathbf x}) = t\\)を満たす\\({\mathbf x}\\)と\\(t\\)に対して\\(T({\mathbf X}) = t\\)を
与えたときの\\({\mathbf X} = {\mathbf x}\\)の条件付き確率\\(P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t)\\)
が\\(\theta\\)に依存しないことを言う.つまり,
\\[
P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t:\theta) = P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t)
\\]


以下の**因数分解定理**(Fisher-Neyman factorization theorem)により,
興味のある統計量が十分統計量であるかを判定できる.
十分統計量が当てはまる事象とパラメータに依存している事象が独立していることを示す.

### 因数分解定理
統計量\\(T\\)がパラメータ\\(\theta\\)の十分統計量であるための,
必要十分条件は,無作為標本\\(\\{X_i\\} _{i \in \mathbb{N} _+,i \leq n}\\)の
同時確率密度関数&thinsp;\\(f _{\mathbf{X}}(\mathbf{x}:\theta)\\)が以下のように
パラメータ\\(\theta\\)に依存しない部分と依存する部分に因数分解できることである.
\\[
f _{\mathbf{X}}(\mathbf{x}:\theta) = h(\mathbf{x}) g(T({\mathbf x}) = t:\theta)
\\]

- 証明
1. 統計量\\(T\\)がパラメータ\\(\theta\\)の十分統計量ならば,&thinsp;\\(f _{\mathbf{X}}(\mathbf{x}:\theta) = h(\mathbf{x}) g(T({\mathbf x}) = t:\theta)\\)  
  まず定義より,
  \\[
  \begin{align}
  P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t:\theta) &= \frac{P({\mathbf X} = {\mathbf x},T({\mathbf X}) = t:\theta)}{P(T({\mathbf X}) = t:\theta)} \\\\
  & =  P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t)
  \end{align}
  \\]
  から,
  \\[
  P({\mathbf X} = {\mathbf x},T({\mathbf X}) = t:\theta) = P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t)P(T({\mathbf X}) = t:\theta)
  \\]
  ここで,十分統計量の定義より,\\(T({\mathbf x}) = t\\)&thinsp;から,
  \\(\\{{\mathbf X} = {\mathbf x}\\} \cap \\{T({\mathbf X}) = t\\} = \\{{\mathbf X} = {\mathbf x}\\}\\)でなので,
  \\[
  P({\mathbf X} = {\mathbf x},T({\mathbf X}) = t:\theta) =  P(\\{{\mathbf X} = {\mathbf x}\\} \cap \\{T({\mathbf X}) = t\\} :\theta) = P({\mathbf X} = {\mathbf x}:\theta)
  \\]
  確率密度関数で表すと,
  \\[
	  f _X({\mathbf x}:\theta) = f _{{\mathbf X}|T} ({\mathbf x}) f _{T}(T({\mathbf x}) = t:\theta)
  \\]
  となり,
  \\[
	 h({\mathbf x}) = f _{{\mathbf X}|T} ({\mathbf x}), g(T({\mathbf x}) = t:\theta) =  f _{T}(T({\mathbf x}) = t:\theta)
  \\]
  となる.
  
1. \\(f _{\mathbf{X}}(\mathbf{x}:\theta) = h(\mathbf{x}) g(T({\mathbf x}) = t:\theta)\\)ならば,統計量\\(T\\)がパラメータ\\(\theta\\)の十分統計量である
  \\[
  \begin{align}
	P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t:\theta) &= \frac{P({\mathbf X} = {\mathbf x},T({\mathbf X}) = t:\theta)}{P(T({\mathbf X}) = t:\theta)} \\\\
  \end{align}
  \\]
  ここで,十分統計量の定義より,\\(T({\mathbf x}) = t\\)&thinsp;から,確率を得たい事象は,
  \\(\\{{\mathbf X} = {\mathbf x}\\} \cap \\{T({\mathbf X}) = t\\} = \\{{\mathbf X} = {\mathbf x}\\}\\)でなので,
  \\[
  \begin{align}
  \frac{P({\mathbf X} = {\mathbf x},T({\mathbf X}) = t:\theta)}{P(T({\mathbf X}) = t:\theta)} &= \frac{P({\mathbf X} = {\mathbf x}:\theta)}{P(T({\mathbf X}) = t:\theta)} \\\\
  \end{align}
  \\]
  \\[
    \begin{align}
	P(T({\mathbf X}) = t:\theta) &= f _T(t:\theta) \\\\
	&= \int _{T({\mathbf x}) = t} f _{{\mathbf X}}({\mathbf x}\:\theta) d{\mathbf x} \\\\
	&= \int _{T({\mathbf x}) = t} h(\mathbf{x}) g(T({\mathbf x}) = t:\theta) d{\mathbf x}
    \end{align}
  \\]
  積分範囲の指定が\\(T({\mathbf x}) = t\\)となる事象であるので,\\(g(T({\mathbf x}) = t:\theta)\\)に代入する\\({\mathbf x}\\)は\\(T({\mathbf x}) = t\\)
  であることが保証され,定数と見なすことができ,
    \\[
    \begin{align}
	P(T({\mathbf X}) = t:\theta) &= g(T({\mathbf x}) = t:\theta) \int _{T({\mathbf x}) = t} h(\mathbf{x})d{\mathbf x}
    \end{align}
  \\]
  から,
  \\[
  \begin{align}
	P({\mathbf X} = {\mathbf x}|T({\mathbf X}) = t:\theta) &= \frac{P({\mathbf X} = {\mathbf x}:\theta)}{P(T({\mathbf X}) = t:\theta)} \\\\
	&= \frac{f _{{\mathbf X}} ({\mathbf x}:\theta)}{g(T({\mathbf x}) = t:\theta) \int _{T({\mathbf x}) = t} h(\mathbf{x})d{\mathbf x}} \\\\
	&= \frac{h(\mathbf{x}) g(T({\mathbf x}) = t:\theta)}{g(T({\mathbf x}) = t:\theta) \int _{T({\mathbf x}) = t} h(\mathbf{x})d{\mathbf x}} \\\\
	&= \frac{h(\mathbf{x})}{\int _{T({\mathbf x}) = t} h(\mathbf{x})d{\mathbf x}}
  \end{align}
  \\]
  となり,\\(\theta\\)に依存しない形になり,\\(T({\mathbf X})\\)が十分統計量となる.
