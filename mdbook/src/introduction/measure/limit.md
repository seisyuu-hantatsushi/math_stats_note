## 極限

### 上極限集合・下極限集合
\\(\forall i \in \mathbb{N},\\; X_i \in \mathcal{X}\\)としたとき,
\\[
	\limsup _{i \to \infty} X_i = \bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} X_j
\\]
を**上極限集合**,
\\[
	\liminf _{i \to \infty} X_i = \bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} X_j
\\]
を**下極限集合**と言う.
\\[
	\liminf _{i \to \infty} X_i = \limsup _{i \to \infty} X_i
\\]
が成立するとき,\\(\lim _{i \to \infty} X_i\\)と書く.

上極限集合,下極限集合は以下のような性質を持つ.
- \\(\liminf _{i \to \infty} X_i \subset \limsup _{i \to \infty} X_i\\)
   - 証明  
   \\[
\begin{align}
   \liminf _{i \to \infty} X_i & \subset \limsup _{i \to \infty} X_i \\\\
   \bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} X_j & \subset \bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} X_j \\\\
   \forall x, (x \in \bigcup ^{\infty} _{i=0} \bigcap^{\infty} _{j=i} X_j &\to x \in \bigcap ^{\infty} _{i=0} \bigcup^{\infty} _{j=i} X_j) \\\\
   x \in \bigcup ^{\infty} _{i=0} \\{x|\forall j \geq i (x \in X_j)\\} &\to x \in \bigcap ^{\infty} _{i=0} \\{x|\exists j \geq i (x \in X_j)\\} \\\\
   x \in \\{x|\exists i \geq 0 \\{x|\forall j \geq i (x \in X_j)\\} \\} &\to x \in \\{x| \forall i \geq 0 \\{x|\exists j \geq i (x \in X_j)\\}\\} \\\\
   x \in \\{x|\forall j \geq i (x \in X_j)\\} &\to x \in \\{x|\exists j \geq i (x \in X_j)\\} \\\\
   x \in \bigcap^{\infty} _{j=i} X_j &\to x \in \bigcup^{\infty} _{j=i} X_j \\\\
\end{align}
   \\]
- \\(X_i\\)が単調増大列のとき,\\(\lim _{i \to \infty} X_i = \bigcup ^{\infty} _{i=0} X_i\\),&thinsp;\\(X_i\\)が単調減少列のとき,\\(\lim _{i \to \infty} X_i = \bigcap ^{\infty} _{i=0} X_i\\).

  - 証明  
     \\(X_i\\)が単調増大列のとき,
 \\[
 \limsup _{i \to \infty} X _i = \bigcup ^{\infty} _{i=0} X_i
 \\]
 が成立する.なぜならば,\\(X_i\\)が単調増大列なので,
 \\[
 \begin{align}
 \limsup _{i \to \infty} X _i &= \lim _{n \to \infty} \left( \left( \bigcup^{\infty} _{j=0} X_j \right) \cap \left( \bigcup^{\infty} _{j=1} X_j \right) \cap \dots \cap \left( \bigcup^{\infty} _{j=n} X_j \right) \right) \\\\
	 &= \bigcup ^{\infty} _{i=0} X_i
 \end{align}
 \\]
 また,
 \\[
 \liminf _{i \to \infty} X _i = \bigcup ^{\infty} _{i=0} X_i
 \\]
 が成立する.
 \begin{align}
 \liminf _{i \to \infty} X _i &= \lim _{n \to \infty} \left( \left( \bigcap^{\infty} _{j=0} X_j \right) \cup \left( \bigcap^{\infty} _{j=1} X_j \right) \cup \dots \cup \left( \bigcap^{\infty} _{j=n} X_j \right) \right) \\\\
	 &= \lim _{n \to \infty} \left( X_0 \cup X_1 \cup \dots \cup X_n \right) \\\\
	 &= \bigcup ^{\infty} _{i=0} X_i
 \end{align}
 から,\\(X_i\\)が単調増大列のとき,\\(\lim _{i \to \infty} X_i = \bigcup ^{\infty} _{i=0} X_i\\)

     \\(X_i\\)が単調減少列のとき,
	 \\[
	  \limsup _{i \to \infty} X _i = \bigcap ^{\infty} _{i=0} X_i
	 \\]
	  が成立する.なぜならば,\\(X_i\\)が単調減少列なので,
	   \begin{align}
 \limsup _{i \to \infty} X _i &= \lim _{n \to \infty} \left( \left( \bigcup^{\infty} _{j=0} X_j \right) \cap \left( \bigcup^{\infty} _{j=1} X_j \right) \cap \dots \cap \left( \bigcup^{\infty} _{j=n} X_j \right) \right) \\\\
	 &= \lim _{n \to \infty} \left( X_0 \cap X_1 \cap \dots \cap X_n \right) \\\\
     &= \bigcap ^{\infty} _{i=0} X_i \\\\
	 \end{align}
	  また,
     \\[
	 \liminf _{i \to \infty} X _i = \bigcap ^{\infty} _{i=0} X_i
	 \\]
	 が成立する.
	 \\[
	  \begin{align}
 \liminf _{i \to \infty} X _i &= \lim _{n \to \infty} \left( \left( \bigcap^{\infty} _{j=0} X_j \right) \cup \left( \bigcap^{\infty} _{j=1} X_j \right) \cup \dots \cup \left( \bigcap^{\infty} _{j=n} X_j \right) \right) \\\\
	 &= \bigcap ^{\infty} _{i=0} X_i
 \end{align}
	 \\]
	 から,\\(X_i\\)が単調減少列のとき\\(\lim _{i \to \infty} X_i = \bigcap ^{\infty} _{i=0} X_i\\)

### Borel-Cantelliの定理
- \\(\mathcal{X}\\)を完全加法族とする.\\(\\{X_i\\}_{i \geq 0} \subset \mathcal{X}\\),&thinsp;
\\( i _0 \in \mathbb{N} \\),&thinsp;
\\( \sum _{i \geq i _0} m(X _i) < \infty \\)なら,&thinsp;
\\(m(\limsup _{i \to \infty} X_i)=0\\)
  - 証明  
    劣加法性より,
	\\[
		m(\bigcup^{\infty}_{i = i_0} X_i) \leq \sum _{i \geq i_0} m(X_i)
	\\]
	\\[
		m(\limsup _{i \to \infty} X_i) = m(\bigcap^{\infty} _{i=0} \bigcup^{\infty} _{j=i} X_j)
	\\]
	\\(Y_i = \bigcup^{\infty} _{j=i} X_j\\)と置くと,\\(Y_i\\)は単調減少列である.よって,下方連続性と
	\\( \sum _{i \geq i _0} m(X _i) < \infty \\)の仮定により,
	\\[
	  \begin{align}
	  m(\bigcap ^{\infty} _{i=0} \bigcup ^{\infty} _{j=i} X_j) &= m(\bigcap ^{\infty} _{i=0} Y _i) \\\\
	  &= \lim _{i \to \infty} m(Y _i) \\\\
	  &= \lim _{i \to \infty} m(\bigcup ^{\infty} _{j=i} X _j) \\\\
	  &\leq \lim _{i \to \infty} \sum ^{\infty} _{j=i} m(X _j) = 0 \\\\
\end{align}
	\\]
