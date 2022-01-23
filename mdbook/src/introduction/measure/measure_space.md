# 測度空間
\\(X\\)を集合,&thinsp;\\(\emptyset \in \mathcal{X} \subset \mathfrak{B}(X)\\),&thinsp;\\(m:\mathcal{X} \to \overline{\mathbb{R}_{+}}\\)&thinsp;とする.
空間\\((X,\mathcal{X})\\)で,以下の性質を定義する.

#### 非負性
\\[
\forall X \in \mathcal{X},\\;0=m(\emptyset) \leq m(X) \leq \infty \tag{m.1}
\\]

#### 可算加法性
\\(\\{X_n\\} _{n \geq 0}\\)にて集合族の要素が互いに素であるとき,
\\[
\\{X_n\\} _{n \geq 0} \subset \mathcal{X},\\; A_0=\bigcup^{\infty} _{n \geq 1} X_n
\\]
ならば
\\[
m(X_0) = \sum^{\infty} _{n \geq 1} m(X_n) \tag{m.2}
\\]

\\(\mathcal{X}\\)が完全加法族なら関数\\(m\\)は**測度**といい,\\((X,\mathcal{X},m)\\)を**測度空間**という.

#### 単調増大列・単調減少列

\\(\\{X _n\\} _{n \geq 0}\\)にて,

\\[
	X_n \subset X_{n+1}
\\]

であるような集合列を**単調増大列**といい,

\\[
	X_n \supset X_{n+1}
\\]

であるような集合列を**単調減少列**という.
