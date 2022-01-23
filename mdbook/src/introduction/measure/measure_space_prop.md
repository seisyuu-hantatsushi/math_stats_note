## 測度空間の性質

空間\\((X,\mathcal{X})\\)は以下の性質を持つ.ここでは,\\(\mathcal{X}\\)を完全加法族と制約しない.

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

#### 単調性
\\[
X_1,X_2 \in \mathcal{X}かつ X_1 \subset X_2 なら, m(X_1) \leq m(X_2)
\\]
- 証明  
  \\(X_1 \subset X_2\\)なら,
  \\[
  X_2 = (X_2 \backslash X_1) \cup X_1
  \\]
  有限加法性より,
  \\[
  \begin{align}
  m(X_2) &= m((X_2 \backslash X_1) \cup X_1) \\\\
  &= m(X_2 \backslash X_1) + m(X_1) \geq m(X_1)
  \end{align}
  \\]

#### 劣加法性
\\(\forall i \in \mathbb{N},\\; X_i \in \mathcal{X}\\)としたとき,
\\[
	m(\bigcup^{\infty}_{i=0}X_i) \leq \sum^{\infty} _{i=0} m(X_i) \tag{m.3}
\\]
- 証明
  \\[
	  Y_0 = X_0,\\;Y_i = X_i \backslash (\bigcup^{i-1} _{k=0} X_k),\\;i\geq1
  \\]
  のように,\\(Y_i\\)を構成する.\\(i \not= j\\)なら,\\(Y_i \cap Y_j = \emptyset\\)
  \\[
	  \forall n \in \mathbb{N}, Y_i \subset X_i, \bigcup^{n} _{i=0} Y_i = \bigcup^{n} _{i=0} X_i
  \\]
  なぜならば,\\(\bigcup^{n} _{i=0} Y_i = \bigcup^{n} _{i=0} X_i\\)に関して,\\(n=0\\)のときは自明,  
  \\(n=1\\)のとき
  \\[
  \begin{align}
  \bigcup^{1} _{i=0} Y_i &= \left( X_1 \backslash (\bigcup^{i-1} _{k=0} X_k) \right) \cup X_0 \\\\
  &= (X_1 \cap X_0^c) \cup X_0 = X_1 \cup X_0 = \bigcup^{1} _{i=0} X_i\\\\
  \end{align}
  \\]
  \\(n=k\\)のとき
  \\[
  \begin{align}
  \bigcup^{k} _{i=0} Y_i &= \bigcup^{k} _{i=0} X_i \\\\
  \end{align}
  \\]
  と仮定する. \\(n=k+1\\)のとき,
  \\[
  \begin{align}
  \bigcup^{k+1} _{i=0} Y_i &= Y _{k+1} \cup \left( \bigcup^{k} _{i=0} Y_i \right) \\\\
                           &= X _{k+1} \backslash (\bigcup^{k} _{i=0} X_i) \cup \left( \bigcup^{k} _{i=0} X_i \backslash (\bigcup^{i-1} _{j=0} X_j) \right) \\\\
						   &= \left( X _{k+1} \cap (\bigcup^{k} _{i=0} X_i)^c \right) \cup (\bigcup^{k} _{i=0} X_i) \\\\
						   &= \bigcup^{k+1} _{i=0} X_i
  \end{align}
  \\]
  となり,\\(n=k+1\\)で成立するので,任意の\\(n\\)で成立する.\\(Y_i \subset X_i\\)から,単調性により,
  \\[
	  m(\bigcup ^{\infty} _{i=0} X_i) = m(\bigcup^{\infty} _{i=0} Y_i) = \sum^{\infty} _{i=0} m(Y_i) \leq \sum^{\infty} _{i=0} m(X_i)
  \\]

#### 上方連続性
\\(\forall i \in \mathbb{N},\\; X_i \in \mathcal{X}, X_i \subset X_{i+1}\\)としたとき,
\\[
	\lim_{i \to \infty} m(X_i) = m(\bigcup^{\infty} _{i=1} X_i) \tag{m.4}
\\]
- 証明
  \\[
	  Y_0 = X_0,\\;Y_i = X_i \backslash (\bigcup^{i-1} _{k=0} X_k),\\;i\geq1
  \\]
  のように,\\(Y_i\\)を構成する.\\(i \not= j\\)なら,\\(Y_i \cap Y_j = \emptyset\\).
  有限加法性より,
  \\[
    \begin{align}
    m(\bigcup^{n} _{i=0} Y_i) &= \sum^{n} _{i=0} m(Y _i) \\\\
                                   &= m(Y_0) + \sum^{n} _{i=1} m(Y _i) \\\\
                                   &= m(Y_0) + \sum^{n} _{i=1} m(X _i \backslash (\bigcup^{i-1} _{k=0} X_k)) \\\\
                                   &= m(Y_0) + \sum^{n} _{i=1} m(X _i \cap (\bigcup^{i-1} _{k=0} X_k)^c)
    \end{align}
  \\]

\\(X_i \subset X_{i+1}\\)であるので,

\\[
    \begin{align}
	m(Y_0) + \sum^{n} _{i=1} m(X_i \cap (\bigcup^{i-1} _{k=0} X_k)^c) &=  m(Y_0) + \sum^{n} _{i=1} m(X _i \cap {X _{i-1}}^c) \\\\
	&= m(X_0) + \sum^{n} _{i=1} \\{ m(X _i) - m({X _{i-1}}) \\} = m(X_n)
    \end{align}
\\]

\\(\bigcup^{n} _{i=0} Y_i = \bigcup^{n} _{i=0} X_i\\)なので,

\\[
m(\bigcup^{n} _{i=0} Y_i) = m(\bigcup^{n} _{i=0} X_i) = m(X_n)
\\]

から\\(n \to \infty\\)としても,\\(	\lim_{n \to \infty} m(X_n) = m(\bigcup^{\infty} _{i=1} X_i)\\)が成立する.

#### 下方連続性
\\(\forall i \in \mathbb{N},\\; X_i \in \mathcal{X}, X_i \supset X_{i+1}, m(X_i) < \infty\\)としたとき,
\\[
	\lim_{i \to \infty} m(X_i) = m(\bigcap^{\infty} _{i=1} X_i) \tag{m.4}
\\]
- 証明  
  \\[
	  Y_0 = X_0,\\;Y_i = (\bigcup^{i-1} _{k=0} X_k) \backslash X_i,\\;i\geq1 (m.5)
  \\]

のように,\\(Y_i\\)を構成する.\\(i \not= j\\)なら,\\(Y_i \cap Y_j = \emptyset\\).  

\\( X_i \supset X_{i+1} \\)なので,\\(Y_i = X_0 \backslash X_i\\).  
さらに,\\( X_{i+1} \subset X_{i} \subset X_0 \\)なので,\\(Y_{i+1} = X_0 \backslash X_{i+1} \supset  X_0 \backslash X_{i} = Y_{i} \\)
から,上方連続性より
\\[
    \begin{align}
	m(\bigcup ^{\infty} _{i=0} Y _i) &= \lim _{i \to \infty} m(Y _i) \\\\
	&= \lim _{i \to \infty} m(X_0 \backslash X_i) \\\\
	&= m(X_0) - \lim _{i \to \infty} m(X_i) \\\\
	&= m(X_0) - \lim _{i \to \infty} m(\bigcap^{i} _{j=0} X _j) \\\\
    &= m(X_0) - m(\bigcap^{\infty} _{i=0} X _i)
	\\end{align}
\\]
より,

\\[
m(\bigcap^{\infty} _{i=0} X _i) = \lim _{i \to \infty} m(X_i)
\\]
