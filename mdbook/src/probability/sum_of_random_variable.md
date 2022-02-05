# 独立確率変数の和
### Kolmogorovの不等式
\\(\\{X_i\\}_{1 \leq i \leq n}\\)を\\((\Omega,\mathcal{F},P)\\)上の独立な確率変数列とする.&nbsp;\\(E[X_i] = 0,{\rm var}(X_i)<\infty\\)とすると,任意の\\(\lambda > 0\\)に対して,
\\[
	P(\max _{1 \leq k \leq n}| \sum^{k} _{i=1} X _i| \geq \lambda) \leq \frac{1}{\lambda^2} \sum^{k} _{i=1} {\rm var}(X_i)
\\]
が成立する.
- 証明  
  \\(A_n=\\{\omega \in \Omega| \max _{1 \leq k \leq n} | \sum^{k} _{i=1} X _i| \geq \lambda \\} \\) とする.
  \\[
  \begin{align}
	  B _k &= \left\\{ \begin{array}{ll}
		\emptyset & (k = 0) \\\\
		\\{\omega \in \Omega| \max _{1 \leq j \leq k} | \sum^{j} _{i=1} X _i| \geq \lambda \\} & (k > 0)
		\end{array}\right. \\\\
	  B' _k &= \\{\omega \in \Omega| |\sum^{k} _{i=1} X _i| \geq \lambda \\}
  \end{align}
  \\]
  とし
  \\[
    \begin{align}
	  A' _k &= (\Omega \backslash B _{k-1} ) \cap B' _k\\\\
	       &= \\{\omega \in \Omega| \max _{1 \leq j \leq k-1} | \sum^{j} _{i=1} X _i| < \lambda \\} \cap \\{\omega \in \Omega| |\sum^{k} _{i=1} X _i| \geq \lambda \\} \\\\
		   &= \\{\omega \in \Omega| \max _{1 \leq j \leq k-1} | \sum^{j} _{i=1} X _i| < \lambda \land |\sum ^{k} _{i=1} X _i| \geq \lambda \\}
    \end{align}
  \\]
  構成すると,\\(A' _{k-1} \\)までで\\(\max _{1 \leq j \leq k-1} | \sum^{j} _{i=1} X _i| \geq \lambda\\)を満たさなかった見本点\\(\omega\\)の中から,
  \\(|\sum ^{k} _{i=1} X _i| \geq \lambda\\)を満たす\\(\omega\\)を集めて\\(A'_k\\)を作るので\\(A'_k\\)は互いに排他で,\\(A_n=\bigcup^{n} _{k=1} A'_k\\)となる.
まず,\\(X_i\\)互いに独立しているので,\\({\rm var}(\sum ^{n} _{i=0} X_i) = \sum^{k} _{i=0} {\rm var}(X_i) \\)
