## Borel-Cantelliの定理

\\(\\{A_i\\} _{i \in \overline{\mathbb{N}}} \\)を\\((\Omega,\mathcal{F},P)\\)上の事象とする.

### Borel-Cantelliの定理 1
\\[
	\sum _{i \in \overline{\mathbb{N}}} P(A_i) < \infty \to P(\limsup _{i \to \infty} A_i) = 0 \land P(\liminf _{i \to \infty} (\Omega \backslash A_i)) = 1
\\]

- 証明

  \\(P(\limsup _{i \to \infty} A_i) = P(\bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} A_j)\\)なので,
  \\[
  \begin{align}
  P(\bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} A_j) &= \lim _{i \to \infty} P(\bigcup ^{\infty} _{j=0} A_j \cap \bigcup ^{\infty} _{j=1} A_j \cap \cdots \cap \bigcup ^{\infty} _{j=i} A_j) \\\\
  &= \lim _{i \to \infty} P(\bigcup ^{\infty} _{j=i} A_j) \leq \lim _{i \to \infty} \sum ^{\infty} _{j=i} P(A_j) = 0
  \end{align}
  \\]
  より,
  \\(P(\limsup _{i \to \infty} A_i) = 0\\)

  \\(P(\liminf _{i \to \infty} A_i) = P(\bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} (\Omega \backslash A_i))\\)なので,
  \\[
  \begin{align}
  P(\bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} (\Omega \backslash A_i)) &= P(\bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} {A_i}^c) \\\\
  &= P((\bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} {A_i})^c) \\\\
  &= P(\Omega \backslash (\bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} {A_i})) \\\\
  &= P(\Omega) - P(\bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} {A_i}) = 1
  \end{align}
  \\]
  より,\\(P(\liminf _{i \to \infty} A_i) = 1\\).

  証明終わり.

Borel-Cantelliの定理 1は\\(\sum _{i \in \overline{\mathbb{N}}} P(A_i) < \infty\\)である時,

- 無限回の試行で,事象\\(A_i\\)が無限回発生する確率は0である.
- 無限回の試行で,事象\\(A_i\\)以外の事象が有限回発生する確率は1である.

ということを保証する.

### Borel-Cantelliの定理 2
\\(\\{A_i\\} _{i \in \overline{\mathbb{N}}} \\)が互いに独立な事象のとき,

\\[
	\sum _{i \in \overline{\mathbb{N}}} P(A_i) = \infty \to P(\limsup _{i \to \infty} A_i) = 1 \land P(\liminf _{i \to \infty} (\Omega \backslash A_i)) = 0
\\]

- 証明
  \\[
  P(\liminf _{i \to \infty} (\Omega \backslash A _i)) = P(\bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} {A _j}^c) = \lim _{i \to \infty} P(\bigcap ^{\infty} _{j=i} {A _j}^c)
  \\]
  ここで,
  \\[
  \begin{align}
  P(\bigcap ^{\infty} _{j=i} {A _i}^c) &= \lim _{k \to \infty} \prod ^{k} _{j=i} P({A _j}^c) \\\\
  &= \prod ^{\infty} _{j=i} (1 - P(A _j)) \\\\
  \end{align}
  \\]
  \\(x \in [0,1]\\)のとき,\\(\log(1-x) \leq -x\\)から\\((1-x) \leq \exp(-x)\\).
  \\[
  \begin{align}
  \prod ^{\infty} _{j=i} (1 - P(A _j)) &\leq \prod ^{\infty} _{j=i} \exp(-P(A _j)) \\\\
  &= \exp(-\sum ^{\infty} _{j=i} P(A _j)) = 0 \\: (\because \sum _{i \in \overline{\mathbb{N}}} P(A_i) = \infty)
  \end{align}
  \\]
  から,\\(P(\bigcap ^{\infty} _{j=i} {A _i}^c) = 0\\)より,\\(P(\liminf _{i \to \infty} (\Omega \backslash A _i)) = 0\\).
  \\[
  \begin{align}
  P(\limsup _{i \to \infty} A_i) &= P(((\limsup _{i \to \infty} A_i)^c)^c) \\\\
  &= P(((\bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} A_j)^c)^c) \\\\
  &= P((\bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} {A_j}^c)^c) \\\\
  &= P(\Omega \backslash (\bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} {A_j}^c)) \\\\
  &= P(\Omega \backslash (\liminf _{i \to \infty} {A_j}^c)) \\\\
  &= 1 - P(\liminf _{i \to \infty} {A_j}^c) = 1
  \end{align}
  \\]
  証明終わり.

Borel-Cantelliの定理 2は事象が独立していて\\(\sum _{i \in \overline{\mathbb{N}}} P(A_i) = \infty\\)である時,

- 無限回の試行で,事象\\(A_i\\)が無限回発生する確率は1である.
- 無限回の試行で,事象\\(A_i\\)以外の事象が有限回発生する確率は0である.

ということを保証する.
