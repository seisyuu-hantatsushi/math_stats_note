# 測度空間
\\(X\\)を集合,&thinsp;\\(\emptyset \in \mathcal{X} \subset \mathfrak{B}(X)\\),&thinsp;\\(m:\mathcal{X} \to \overline{\mathbb{R}_{+}}\\)&thinsp;とする.
空間\\((X,\mathcal{X})\\)で,以下の性質を定義する.

#### 非負性
\\[
\forall A \in \mathcal{X},\\;0=m(\emptyset) \leq m(A) \leq \infty \tag{m.1}
\\]

#### 可算加法性
\\(\\{A_n\\} _{n \geq 0}\\)にて集合族の要素が互いに素であるとき,
\\[
\\{A_n\\} _{n \geq 0} \subset \mathcal{X},\\; A_0=\bigcup^{\infty} _{n \geq 1} A_n
\\]
ならば
\\[
m(A_0) = \sum^{\infty} _{n \geq 1} m(A_n) \tag{m.2}
\\]

\\(\mathcal{X}\\)が完全加法族なら関数\\(m\\)は**測度**といい,\\((X,\mathcal{X},m)\\)を**測度空間**という.

空間\\((X,\mathcal{X})\\)は以下の性質を持つ.

#### 有限加法性
\\(i,n \in \mathbb{N},\\;\\{X_i\\}_{0 \leq i \leq n} \subset \mathcal{X}\\)としたとき,
\\[
m(\bigcup^{n} _{i=0} X_i) = m(\coprod^{n} _{i=0} X_i) = \sum^{n} _{i=0} m(X_i) \tag{m.3}
\\]

- 証明  
  \\(X_n = \emptyset, n > i \\)としたとき,
  \\[
  \bigcup^{\infty} _{i=0} X_i = \left(\bigcup^{n} _{i=0} X_i\right) \cup \left( \bigcup^{\infty} _{i = n} \emptyset \right) = \coprod^{n} _{i=0} X_i
  \\]
  可算加法性より
  \\[
  m(\bigcup^{n} _{i=0} X_i) = \sum^{n} _{i=0} m(X_i)
  \\]

### 単調性
