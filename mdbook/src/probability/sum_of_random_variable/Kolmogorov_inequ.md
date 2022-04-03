### Kolmogorovの不等式
\\(\\{X_i\\}_{1 \leq i \leq n}\\)を\\((\Omega,\mathcal{F},P)\\)上の独立な確率変数列とする.&nbsp;\\(E[X_i] = 0,{\rm var}(X_i)<\infty\\)とすると,任意の\\(\lambda > 0\\)に対して,
\\[
	P(\max _{1 \leq k \leq n}| \sum^{k} _{i=1} X _i| \geq \lambda) \leq \frac{1}{\lambda^2} \sum^{n} _{i=1} {\rm var}(X_i)
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
  \\[
	P(A _n) = \sum ^{n} _{k=1} P(A' _k)
  \\]
  ここで,\\(I _{A' _k}:\Omega \mapsto \\{0,1\\}\\)なる指示関数を用意する.
  \\(\\{A' _k\\}\\)は互いに排他なので,\\(I _{A' _j}(\omega)=1\\)ならば,\\(k \not = j\\)の\\(k\\)については,\\(I _{A' _k}(\omega)=0\\).  
  Markovの不等式から\\(A _k\\)は\\(|\sum ^{k} _{i=1} X _i| \geq \lambda\\)なので,
  \\[
	  P(A' _k) \leq \frac{1}{\lambda^2} E[ (\sum ^{k} _{i=1} X _i)^2 I _{A' _k}]
  \\]
  \\[
	  \sum ^{n} _{k=1} P(A' _k) \leq \sum ^{n} _{k=1} \frac{1}{\lambda^2} E[ (\sum ^{k} _{i=1} X _i)^2 I _{A' _k}]
  \\]
  \\(E[ (\sum ^{k} _{i=1} X _i)^2 I _{A' _k}]\\)は
  \\[
  \begin{align}
    E[(\sum ^{n} _{i=1} {X _i})^2 I _{A' _k}] &= \int _{\Omega} (\sum ^{n} _{i=1} X _i(\omega))^2 I _{A' _k}(\omega) P(d\omega) \\\\
	&= \int _{A' _k} (\sum ^{n} _{i=1} X _i(\omega))^2 P(d\omega) \\\\
	&= E[(\sum ^{n} _{i=1} X _i)^2:A'_k]
\end{align}
  \\]
  
  \\(E[(\sum ^{n} _{i=1} X _i(\omega))^2:A'_k]\\)は互いに排他な\\(\\{A' _k\\}\\)事象で制限された期待値で,\\( \Omega \supset A _n \supset A' _k \\)なので,
  \\[
	\begin{align}
    E[(\sum ^{n} _{i=1} X _i)^2] &= \int _{\Omega} (\sum ^{n} _{i=1} {X _i(\omega)})^2 P(d\omega)\\\\
	& \geq \int _{A_n} (\sum ^{n} _{i=1} {X _i(\omega)})^2 P(d\omega) \\\\
	& = \sum ^{n} _{k=1} \int _{A' _k} (\sum ^{n} _{i=1} {X _i(\omega)})^2 P(d\omega) \\\\
	& = \sum ^{n} _{k=1}E[(\sum ^{n} _{i=1} {X _i})^2:A' _k] \\\\
	& = \sum ^{n} _{k=1} E[(\sum ^{n} _{i=1} {X _i})^2 I _{A' _k}]
	\end{align}
  \\]
  \\[
  \begin{align}
  (\sum ^{n} _{i=1} {X _i})^2 &= (\sum ^{n} _{i=k+1} {X _i}+\sum ^{k} _{i=1} {X _i})^2 \\\\
  &= (\sum ^{n} _{i=k+1} {X _i})^2 + 2(\sum ^{n} _{i=k+1} {X _i})(\sum ^{k} _{i=1} {X _i}) + (\sum ^{k} _{i=1} {X _i})^2 \\\\
  &\geq 2(\sum ^{n} _{i=k+1} {X _i})(\sum ^{k} _{i=1} {X _i}) + (\sum ^{k} _{i=1} {X _i})^2
\end{align}
  \\]
  より,
\\[
	E[(\sum ^{n} _{i=1} {X _i})^2 I _{A' _k}] - E[(\sum ^{k} _{i=1} {X _i})^2 I _{A' _k}] \geq E[2(\sum ^{n} _{i=k+1} {X _i})(\sum ^{k} _{i=1} {X _i})I _{A' _k}]
\\]
 ここで,\\(\sum ^{n} _{i=k+1} {X _i}\\)と\\((\sum ^{k} _{i=1} {X _i})I _{A' _k}\\)は独立しているので
\\[
	E[(\sum ^{n} _{i=1} {X _i})^2 I _{A' _k}] - E[(\sum ^{k} _{i=1} {X _i})^2 I _{A' _k}] \geq 2E[(\sum ^{n} _{i=k+1} {X _i})]E[(\sum ^{k} _{i=1} {X _i})I _{A' _k}]
\\]
 \\(E[X _i]=0\\)なので,
 \\[
	E[(\sum ^{n} _{i=1} {X _i})^2 I _{A' _k}] - E[(\sum ^{k} _{i=1} {X _i})^2 I _{A' _k}] \geq 0
 \\]

 \\[
   \begin{align}
	P(A _n) &= \sum ^{n} _{k=1} P(A' _k) \\\\
	&\leq \sum ^{n} _{k=1} \frac{1}{\lambda^2} E[ (\sum ^{k} _{i=1} X _i)^2 I _{A' _k}] \\\\
	&\leq \sum ^{n} _{k=1} \frac{1}{\lambda^2} E[(\sum ^{n} _{i=1} {X _i})^2 I _{A' _k}] \\\\
	& = \frac{1}{\lambda^2} E[(\sum ^{n} _{i=1} {X _i})^2]
   \end{align}
 \\]
 \\(\\{X_i\\}\\)は互いに独立しているので
 \\[
 	P(\max _{1 \leq k \leq n}| \sum^{k} _{i=1} X _i| \geq \lambda) \leq \frac{1}{\lambda^2} \sum^{n} _{i=1} {\rm var}(X_i)
 \\]
 証明終わり.
