# 確率変数
全事象に属する単一事象は,実数値とは限らない.
であるので,単一事象から実数値に対応付ける関数を用意する.これを**確率変数**という.
(関数なのに変数という...)

\\[
X : \Omega \mapsto \mathbb{R}
\\]

単一事象\\(\forall \omega \in \Omega \\)を確率変数に入れた値\\(X(\omega)\\)をここでは**データ**と名付ける.
データは実際には観測値,測定値などに当たる.
例えば,\\(\\{\omega \in \Omega | X(\omega) \in A \\}\\)とデータがとある条件で定める集合\\(A\\)に属する事象を定めたとき,
それが起こる確率は\\(P(\\{\omega \in \Omega | X(\omega) \in A\\})\\)で得られるが,\\(P(\cdot)\\)が引き取れる集合は,可測集合でなくては行けない.なので,\\(\\{\omega \in \Omega | X(\omega) \in A\\}\\)は完全加法族\\(\mathcal{F}\\)に属するという制約がつけられる.
一般に,
\\[
\begin{align}
& P(X \in A)  := P(\\{\omega \in \Omega | X(\omega) \in A\\}) \\\\
& P(X \leq x) := P(\\{\omega \in \Omega | X(\omega) \leq x \\}) \\\\
& P(a \leq X < b) := P(\\{\omega \in \Omega | a \leq X(\omega) < b\\})
\end{align}
\\]
と略記する.

また,微小事象\\(d\omega\\)とすると,
\\[
\begin{align}
P(d\omega) &:= \lim _{dx \to 0} P(\\{\omega \in \Omega | x < X(\omega) \leq x+dx\\}) \\\\
&= \lim _{dx \to 0} \\{ P(X  \leq x+dx) - P(X \leq x) \\}
\end{align}
\\]
と表記し,微小事象の確率と表す.

