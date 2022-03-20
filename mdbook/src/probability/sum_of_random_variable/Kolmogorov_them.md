## Kolmogorovの定理
\\(\\{X_i\\}_{1 \leq i \leq \infty}\\)を\\((\Omega,\mathcal{F},P)\\)上の独立な確率変数列とする.
\\(\sum ^{\infty} _{i=1} E[X _i] < \infty,\sum ^{\infty} _{i=1} {\rm var}(X _i)< \infty\\)でともに収束するなら,
\\(\sum ^{\infty} _{i=1} X _i\\)は概収束する.
- 証明  
Kolmogorovの不等式
\\[
	P(\max _{1 \leq k \leq n}| \sum^{k} _{i=1} X _i| \geq \lambda) \leq \frac{1}{\lambda^2} \sum^{n} _{i=1} {\rm var}(X_i)
\\]
に,\\(\\{X _{n+i}\\} _{1 \leq i \leq \infty} \\)を適用する.
\\[
\begin{align}
P(\max _{1 \leq k \leq m}| \sum ^{k} _{i=1} X _{n+i}| \geq \lambda) &\leq \frac{1}{\lambda^2} \sum ^{m} _{i=1} {\rm var}(X _{n+i}) \\\\
P(\max _{1 \leq k \leq m}| \sum ^{k+n} _{i=1} X _{i} -  \sum ^{n} _{i=1} X _{i}| \geq \lambda) &\leq \frac{1}{\lambda^2} \sum ^{m} _{i=1} {\rm var}(X _{n+i})
\end{align}
\\]
\\[
| \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | \leq | \sum ^{k+n} _{i=1} X _{i} -  \sum ^{n} _{i=1} X _{i}| + |\sum ^{n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i}|
\\]
上式より,
\\[
 \max _{1 \leq k,l \leq m} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | \leq 2 \max _{1 \leq k \leq m} | \sum ^{k+n} _{i=1} X _{i} -  \sum ^{n} _{i=1} X _{i}|
\\]
から,
\\[
\begin{align}
 P( \max _{1 \leq k,l \leq m} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | > 2\lambda ) &\leq P(\max _{1 \leq k \leq m} | \sum ^{k+n} _{i=1} X _{i} -  \sum ^{n} _{i=1} X _{i}| > \lambda) \\\\
 & \leq \frac{1}{\lambda^2} \sum ^{m} _{i=1} {\rm var}(X _{n+i})
\end{align}
\\]
事象\\(\\{\omega| \max _{1 \leq k,l \leq m} | \sum ^{k+n} _{i=1} X _{i}(\omega) - \sum ^{l+n} _{i=1} X _{i}(\omega) | > 2 \lambda \\} \\)は\\(m\\)が増大すると
\\( \\{ \omega| \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i}(\omega) - \sum ^{l+n} _{i=1} X _{i}(\omega) | > 2 \lambda \\} \\)に近づくので,

\\[
\begin{align}
 \lim _{m \to \infty} P( \max _{1 \leq k,l \leq m} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | > 2\lambda ) &\leq  \lim _{m \to \infty} \frac{1}{\lambda^2} \sum ^{m} _{i=1} {\rm var}(X _{n+i}) \\\\
 P( \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | > 2 \lambda ) &\leq \frac{1}{\lambda^2} \sum ^{\infty} _{i=1} {\rm var}(X _{n+i})
\end{align}
\\]
事象\\(\\{\omega| \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | > 2 \lambda \\} \\)は\\(n\\)が増大すると,減少するので,

\\[
\begin{align}
 \lim _{n \to \infty} P( \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | > 2 \lambda ) &\leq  \lim _{n \to \infty} \frac{1}{\lambda^2} \sum ^{\infty} _{i=1} {\rm var}(X _{n+i}) \\\\
 P( \lim _{n \to \infty} \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | > 2 \lambda ) &\leq \lim _{n \to \infty} \frac{1}{\lambda^2} \left \\{ \sum ^{\infty} _{i=1} {\rm var}(X _{i}) -  \sum ^{n} _{i=1} {\rm var}(X _{i}) \\right\\} \\\\
\end{align}
\\]
仮定にて,\\(\sum ^{\infty} _{i=1} {\rm var}(X _i)\\)は収束するので,
\\[
 P( \lim _{n \to \infty} \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | > 2 \lambda ) = 0
\\]
ここで,\\(\lambda \to 0\\)とすると,
\\[
 P( \lim _{n \to \infty} \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | = 0 ) = 1
\\]
から,
\\[
\lim _{n \to \infty} \sup _{1 \leq k,l} | \sum ^{k+n} _{i=1} X _{i} - \sum ^{l+n} _{i=1} X _{i} | = 0 \\; P \text{-a.s}
\\]
となり,\\(\sum ^{\infty} _{i=1} X _i\\)が概収束することになる.
