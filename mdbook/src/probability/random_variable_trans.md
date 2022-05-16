## 変数変換
関数&thinsp;\\(g:{\mathbb R} \mapsto {\mathbb R}\\)にて,確率変数\\(X\\)が\\(Y=g(X)\\)と確率変数\\(Y\\)に
変換されたときの\\(Y\\)の確率分布を確率変数\\(X\\)から得る方法を考える.

### 変数変換
確率変数\\(X\\)の確率密度関数を\\(f_X(x)\\)とし,関数\\(g\\)が単調増加関数で逆関数を持つとした時,
確率変数\\(Y\\)が,\\(Y=g(X)\\)と確率変数\\(X\\)の変換により得られる時,\\(Y\\)の確率密度関数は,
\\[
	f_Y(g(x)) = \frac{f_X(x)}{g'(x)}
\\]

- 証明  
  \\(Y=g(X)\\)とした時,\\(P(\\{X \leq x\\}) = P(\\{Y \leq g(x)\\})\\)であるので,
  \\(P(\\{X \leq x\\}) = F_X(x), P(\\{Y \leq g(x)\\}) = F_Y(g(x))\\)とした時,
  \\[
  \begin{align}
  F _X(x) &= \int^{x} _{-\infty} f_X(x) dx \\\\
  F _Y(g(x)) &= \int^{g(x)} _{-\infty} f_Y(g(x)) dy \\\\
  \end{align}
  \\]
  から,
  \\[
  \int^{x} _{-\infty} f_X(x) dx = \int^{g(x)} _{-\infty} f_Y(g(x)) dy
  \\]
  \\(y=g(x)\\)として右辺の置換積分を行うと,
  \\[
  \int^{x} _{-\infty} f_X(x) dx = \int^{g(x)} _{-\infty} f_Y(g(x)) g'(x) dx
  \\]
  両辺を\\(x\\)について微分すると,
  \\[
  f_X(x) = f_Y(g(x)) g'(x)
  \\]
  確率変数\\(X\\)から,確率変数\\(Y\\)の分布を求めたいので,
  \\[
  \begin{align}
  f_Y(g(x)) &= \frac{f_X(x)}{g'(x)} \\\\
  f_Y(y) &= \frac{f_X(x)}{g'(x)} = \frac{f_X(g^{-1}(y))}{g'(g^{-1}(y))}
  \end{align}
  \\]
