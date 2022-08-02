## 確率変数の独立性
確率の独立性から確率変数の独立性が得られる.
事象\\(A,B\\)とその事象をとる確率変数\\(X,Y\\)とすると,
\\[
	P(X \in A, Y \in B) = \int_B \int_A f_{X,Y}(x,y) dx dy
\\]
事象\\(A,B\\)が独立であると,
\\[
	P(X \in A, Y \in B) = P(\\{\omega|X(\omega) \in A\\} \cap \\{\omega|X(\omega) \in B\\}) = P(\\{\omega|X(\omega) \in A\\})P(\\{\omega|X(\omega) \in B\\})
\\]
となるので,
\\[
	P(X \in A, Y \in B) = \int_B \int_A f_{X}(x) f_{Y}(y) dx dy
\\]
となり,
\\(f_{X,Y}(x,y) = f_{X}(x) f_{Y}(y)\\)であるとき,確率変数\\(X,Y\\)が**独立**(independent)であるという.

確率変数\\(X,Y\\)が独立であるとき,
\\[
E[g(X)h(Y)] = E[g(X)] \cdot E[h(X)]
\\]
が成立する.

- 証明
  \\[
  \begin{align}
  E^{X,Y}[g(X)h(Y)] &= \int \int g(x)h(y)f_{X,Y}(x,y) d\mu_X(x) d\mu_Y(y) \\\\
  &= \int \int g(x) h(y) f _X(x)f _Y(y) d\mu_X(x) d\mu_Y(y) \\\\
  &= \int g(x) f _X(x) d\mu_X(x) \int h(y) f _Y(y)  d\mu_Y(y) \\\\
  &= E^{X}[g(X)] \cdot E^{Y}[h(Y)]
  \end{align}
  \\]

確率変数\\(X,Y\\)が独立でないとき,\\(X,Y\\)は従属しているという.
