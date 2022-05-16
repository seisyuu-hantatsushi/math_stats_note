# 確率変数列の収束
確率変数列が確率変数に近づくという定義を考える.

## 確率収束
確率測度はルベーグ測度なので,ルベーグ測度の収束の考えに当てはめることができる.

### 概収束
**概収束**,P-a.s.収束とはルベーグ測度の概収束と同じである.
まず,とある事象\\(A \subset \Omega\\)の確率が\\(P(A)=1\\)なら,**ほとんど確実に成立する**という.
\\[
P(X \in A) := P(\\{\omega | X(\omega) \in A \\}) = 1
\\]
ならば,
\\[
	X \in A \\; P \text{-a.s}
\\]
と表記する.
確率変数の数列\\( \\{X_n\\} _ {n=0,1,\dots} \\)が確率変数\\(X\\)に概収束するとは,
\\[
P(\\{\omega | \lim_{n \to \infty} | X_n(\omega) - X(\omega) | = 0 \\}) = 1
\\]
となることである.
\\[
	X_n \to X \\; P \text{-a.s}
\\]
\\[
	X_n \xrightarrow{P \text{-a.s}} X
\\]
と表す.
概収束する確率変数の数列が見つかり,収束先の確率変数より扱いやすいなら,確率変数の数列を扱い,
概収束する確率変数が見つかっているなら,\\(n\\)を大きくすることで,収束先の確率変数を近似する.

### 確率収束
確率変数の数列\\( \\{X_n\\} _ {n=0,1,\dots} \\)が確率変数\\(X\\)に**確率収束**するとは,
ルベーグ測度の測度収束の確率への適用であり
\\[
\forall \varepsilon > 0,\\; \lim_{n \to \infty} P(|X_n-X| \geq \varepsilon) = \lim_{n \to \infty} P(\\{\omega|X_n(\omega) - X(\omega) | \geq \varepsilon \\}) = 0
\\]
となることで,
\\[
	X_n \xrightarrow{p} X
\\]
と表す.
確率収束は概収束より弱い条件である,
\\[
\begin{align}
& & \lim_{n \to \infty} P(|X_n-X| \geq \varepsilon) = 0 \\\\
&\leftrightarrow & \lim_{n \to \infty} P(|X_n-X| < \varepsilon) = 1
\end{align}
\\]
となり,\\(n \to \infty\\)のとき \\(|X_n-X| < \varepsilon\\)をみたす事象全体で,確率1を満たすなら
\\(X_n\\)が\\(X\\)に近づくと見なすということである.

### 平均2乗収束
確率変数の数列\\( \\{X_n\\} _ {n=0,1,\dots} \\)が確率変数\\(X\\)に**平均2乗収束**するとは,
\\(L^2\\)空間での収束を確率変数に適用したものである.
\\[
\lim_{n \to \infty} E[(X_n-X)^2] = \lim_{n \to \infty} \left(\int_{\Omega} (X_n(\omega)-X(\omega))^2 P(X(d\omega))\right)^2 = 0
\\]
平均2乗収束は確率収束より弱い条件である.
- 定理
  平均2乗収束ならば確率収束である.
  - 証明
  Chebyshevの不等式より,
  \\[
	  P(|X_n-X| > \varepsilon) \leq \frac{E[(X_n-X)^2]}{\varepsilon^2}
  \\]
  から\\(n \to \infty\\)としたとき
  \\[
  \begin{align}
  \lim_{n \to \infty} P(|X_n-X| > \varepsilon) &\leq \lim_{n \to \infty} \frac{E[(X_n-X)^2]}{\varepsilon^2} \\\\
  &\leq 0
  \end{align}
  \\]
  より,平均2乗収束ならば確率収束する.

### 分布収束
確率変数列\\( \\{X_n\\} _ {n=0,1,\dots} \\)の分布関数を\\( \\{ {F_{X_n}}(x) = P(X_n \leq x)\\} _ {n=0,1,\dots} \\)とする.
確率変数\\(X\\)の分布関数\\(F_X(x)\\)にすべての連続点\\(x\\)で,
\\[
 \lim _{n \to \infty} {F _{X _n}}(x) = F_X(x)
\\]
のとき,\\(X _n\\)は\\(X\\)に**分布収束**するという.**弱収束**,**法則収束**とも言う.
\\[
	X_n \xrightarrow{d} X
\\]
と表記する.
