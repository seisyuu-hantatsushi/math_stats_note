## Portmanteau定理
分布収束と同値な定義を示した定理を**Portmanteau(両開き旅行かばん語)定理**という.

### Portmanteau定理
確率変数\\(X\\),確率変数列 \\( \\{X _n \\} _{n \in \mathbb{N} _+} \\)を用意し,
それそれに対応する分布関数を,\\(F _X,F _{X_n}\\)とする.  
\\(F _X\\)に対応する確率測度を\\(P\\),\\(F _{X_n}\\)に対応する確率測度を\\(P_n\\)とする.  
以下の定義は同値である.

1. \\(X_n \xrightarrow{d} X\\)
1. 任意の有界連続関数&thinsp;\\(f:\mathbb{R} \mapsto \mathbb{R}\\)に対して
   \\[
	   E[f(X _n)] \to E[f(X)]
   \\]
1. 任意の有界一様連続関数&thinsp;\\(f:\mathbb{R} \mapsto \mathbb{R}\\)に対して
   \\[
	   E[f(X _n)] \to E[f(X)]
   \\]
1. 任意の閉集合Aに対して,&thinsp;\\(\limsup_{n \to \infty} P_{n}(A) \leq P(A)\\)
1. 任意の開集合Aに対して,&thinsp;\\(\liminf_{n \to \infty} P_{n}(A) \geq P(A)\\)

- 証明  
  \\(2 \Rightarrow 3\\)は,関数\\(f\\)が有界連続関数なら,有界一様連続関数なので成立.  
  \\(4 \Leftrightarrow 5\\)を示す. 任意の開集合\\(A\\)の補集合\\(A^c\\)は閉集合.  
  \\[
  \begin{align}
  \limsup_{n \to \infty} P_{n}(A^c) \leq P(A^c) &\Leftrightarrow \\\\
  \limsup_{n \to \infty} (1-P_{n}(A)) \leq 1-P(A) &\Leftrightarrow \\\\
  \limsup_{n \to \infty} (-P_{n}(A)) \leq -P(A) &\Leftrightarrow \\\\
  \liminf_{n \to \infty} (P_{n}(A)) \geq P(A)
  \end{align}
  \\]
  から,\\(4 \Rightarrow 5\\)が成立.\\(5 \Rightarrow 4\\)も同様.  
  \\(4,5 \Rightarrow 1\\)を示す. \\(A = \\{\omega| X(\omega) \leq x \\}\\)は閉集合で,
  \\[
  	  \limsup _{n \to \infty} F _{X _n}(x) = \limsup _{n \to \infty} P _n(A) \leq P(A) = F _X(x)
  \\]
  
  任意の正数\\(\varepsilon > 0\\)を用意して,\\(\overline{A'} = \\{\omega| X(\omega) \leq x-\varepsilon \\}\\)と,\\(A' = \\{\omega| X(\omega) < x-\varepsilon/2 \\}\\)
  を作ることができる. \\(\overline{A'} \subset A'\\)から
  \\[
  F_X(x-\varepsilon) = P(\overline{A'}) \leq P(A') \leq \liminf _{n \to \infty} P _n(A')
  \\]
  \\(A' \subset A\\)から
  \\[
  \liminf _{n \to \infty} P _n(A') \leq \liminf _{n \to \infty} P _n(A) = \liminf _{n \to \infty} F _{X_n}(x) \leq \limsup _{n \to \infty} F _{X_n}(x)
  \\]
  なので,
  \\[
  F_X(x-\varepsilon) \leq \liminf _{n \to \infty} F _{X_n}(x) \leq \limsup _{n \to \infty} F _{X_n}(x) \leq F_X(x)
  \\]
  \\(F_X\\)は連続関数なので,\\(\forall \delta, \exists \varepsilon |F_X(x)-F_X(x-\varepsilon)| < \delta\\)から,
  \\(\varepsilon \to 0\\)としても収束し,
  \\[
  \liminf _{n \to \infty} F _{X_n}(x) = \limsup _{n \to \infty} F _{X_n}(x) = F_X(x) \\\\
  \lim _{n \to \infty} F _{X_n}(x) = F_X(x) \\\\
  \\]
  
  \\(1 \Rightarrow 2\\)を示す.任意の正数\\(\delta\\)と\\(M\\)を用意する.
  \\[
	  F_X(-M) < \delta, 1-F_X(M) < \delta
  \\]
  として,\\(M\\)を十分大きくすると,\\(\delta\\)は十分小さくできる.
  \\(F\\)の不連続点は可算なので,\\(-M,M\\)は\\(F\\)の連続点に取ることができる.  
  閉区間\\([-M,M]\\)で,\\(-M=m_0 < m_1 < \cdots < m_{k-1} < m_k = M\\)なる分点\\(\\{m_i\\} _{0 \leq i \leq k}\\)を取る.
  分点\\(\\{m_i\\} _{0 \leq i \leq k}\\)も\\(F\\)の連続点に取ることができ,数列\\(\\{m_i\\} _{0 \leq i \leq k}\\)は\\(\forall i \geq 1, |m _i - m _{i-1}| < \delta\\)となるように取ることができる.  
  
  仮定で\\(F_n\\)が分布収束から,\\(\lim _{n \to \infty} F_n(x) = F(x)\\).なので,十分大きな\\(N\\)を取ってきて,
  \\[
  \forall n > N, | F _n(m _j) - F(m _j) | < \delta
  \\]
  とすることができる. \\(-M=m _0, M=m _k\\)なので,
  \\[
  \forall n > N, F _{X _n}(-M) < 2 \delta, 1 - F _{X _n}(M) < 2 \delta
  \\]

  これから,
  \\[
  \forall n > N, F _{X _n}(-M) + 1 - F _{X _n}(M) + F _{X}(-M) + 1 - F _{X}(M) < 6 \delta \\\\
  \forall n > N, F _{X _n}(-M) + 1 - F _{X _n}(M) - (F _{X}(-M) +  1 - F _{X}(M)) \leq F _{X _n}(-M) + 1 - F _{X _n}(M) + F _{X}(-M) + 1 - F _{X}(M)
  \\]

  \\[
    \begin{align}
   & \left| \int^{\infty} _{M} f(x) dF _{X_n}(x) - \int^{\infty} _{M} f(x) dF _{X}(x) + \int^{-M} _{-\infty} f(x) dF _{X_n}(x) - \int^{-M} _{-\infty} f(x) dF _{X}(x) \right|\\\\
   = & \left| \int^{\infty} _{-\infty} f(x) dF _{X_n}(x) - \int^{\infty} _{-\infty} f(x) dF _{X}(x) - \left( \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right) \right|\\\\
      = &  \left| \int _{\Omega} f(x) P(d\omega) - \int _{\Omega} f(x) P(d\omega) - \left( \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right) \right|\\\\
   = &  \left| E[f(X_n)] - E[f(X)] - \left( \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right) \right|
	\end{align}
  \\]
  \\(f(x)\\)は有界関数なので,\\(\sup _{-\infty \leq x \leq \infty} f(x) = a\\)と置くと,
  \\[
  \left| \int^{\infty} _{M} f(x) dF _{X_n}(x) - \int^{\infty} _{M} f(x) dF _{X}(x) + \int^{-M} _{-\infty} f(x) dF _{X_n}(x) - \int^{-M} _{-\infty} f(x) dF _{X}(x) \right| < a \cdot 6 \delta
  \\]
  \\[
  \left| E[f(X_n)] - E[f(X)] - \left( \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right) \right| < a \cdot 6 \delta
  \\]

  \\(\left| \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right|\\)の区間を評価する.
  \\(f\\)は連続関数なので,閉区間\\([-M,M]\\)にて一様連続関数で, 
  \\[
  \exists \delta |y - x| < \delta \Rightarrow \forall \varepsilon |f(y) - f(x)| < \varepsilon
  \\]
  なので,閉区間\\([-M,M]\\)の分点,\\(\\{m_i\\} _{0 \leq i \leq k}\\)で,
  \\[
  \exists \delta |m_i - x| < \delta \Rightarrow \forall \varepsilon |f(m_i) - f(x)| < \varepsilon
  \\]
  とすることができる,\\(m _{i-1} < x \leq m _i\\)なる\\(x\\)と\\(\varepsilon\\)が用意できる.
  ここで,&thinsp;\\(a_i = f(m _i)\\)として以下の単関数を用意する.

  \\[
      \begin{align}
	  g _{\varepsilon}(x) &= \sum ^{k-1} _{i=0} a _i I _{m _{i} \leq x < m _{i+1}}(x) \\\\
	  	  &= \sum ^{k-1} _{i=0} a _i (I _{-\infty < x \leq m _{i+1}}(x) - I _{ -\infty < x \leq m _{i}}(x))
	  \end{align}
  \\]

ここで,\\(g _{\varepsilon}(x)-f(x) < \varepsilon\\)
  \\[
    \left| \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} g _{\varepsilon}(x) dF _{X_n}(x) \right| = \left| \int^{M} _{-M} (f(x) - g _{\varepsilon}(x)) dF _{X_n}(x) \right| < \varepsilon \left| \int^{M} _{-M} dF _{X_n}(x) \right| < \varepsilon
  \\]
  \\[
    \left| \int^{M} _{-M} f(x) dF _X(x) - \int^{M} _{-M} g _{\varepsilon}(x) dF _X (x) \right| = \left| \int^{M} _{-M} (f(x) - g _{\varepsilon}(x)) dF _X(x) \right| < \varepsilon \left| \int^{M} _{-M} dF _X(x)\right| < \varepsilon
  \\]

\\[
    \begin{align}
	& \left| \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right| = \\\\
	& \left| \int^{M} _{-M} f(x) dF _{X_n}(x) + \int^{M} _{-M} g _{\varepsilon}(x) dF _{X_n}(x) - \int^{M} _{-M} g _{\varepsilon}(x) dF _{X_n}(x) + \int^{M} _{-M} g _{\varepsilon}(x) dF _X(x) - \int^{M} _{-M} g _{\varepsilon}(x) dF _X(x)  - \int^{M} _{-M} f(x) dF _{X}(x)\right| = \\\\
	&  \left| \int^{M} _{-M} (f(x) - g _{\varepsilon}(x)) dF _{X_n}(x) + \int^{M} _{-M} g _{\varepsilon}(x) dF _{X_n}(x) - \int^{M} _{-M} g _{\varepsilon}(x) dF _X(x)  - \int^{M} _{-M} (f(x)-g _{\varepsilon}(x)) dF _{X}(x)\right|
	\end{align}
  \\]
  \\(g _{\varepsilon}(x)-f(x) > 0\\),分布関数は単調増加関数なので,
\\[
    \begin{align}
	&  \left| \int^{M} _{-M} (f(x) - g _{\varepsilon}(x)) dF _{X_n}(x) + \int^{M} _{-M} g _{\varepsilon}(x) dF _{X_n}(x) - \int^{M} _{-M} g _{\varepsilon}(x) dF _X(x)  - \int^{M} _{-M} (f(x)-g _{\varepsilon}(x)) dF _{X}(x)\right| \leq \\\\
	& \left| \int^{M} _{-M} (f(x) - g _{\varepsilon}(x)) dF _{X_n}(x)\right| + \left| \int^{M} _{-M} g _{\varepsilon}(x) dF _{X_n}(x) - \int^{M} _{-M} g _{\varepsilon}(x) dF _X(x) \right| + \left|  \int^{M} _{-M} (f(x)-g _{\varepsilon}(x)) dF _{X}(x)\right| < 2\varepsilon
	\end{align}
  \\]
  ここで,\\(n \to \infty\\)を取ると分布収束と\\(\varepsilon \to 0\\)から\\(\left| \int^{M} _{-M} f(x) dF _{X _n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right| \to 0 \\)
  なので,\\(n \to \infty\\)とすると
  \\[
     \left| E[f(X_n)] - E[f(X)] - \left( \int^{M} _{-M} f(x) dF _{X_n}(x) - \int^{M} _{-M} f(x) dF _{X}(x)\right) \right| \to 0
  \\]
  となり,\\(n \to \infty\\)とすると \\(E[f(X_n)] \to E[f(X)]\\).

  \\(3 \Rightarrow 4\\)を示す.  
  \\(A \subset A_\varepsilon, P(A_\varepsilon)-P(A) \leq \varepsilon\\)であるような,
  事象\\(A,A_\varepsilon\\)を用意する. それに対して,次のような有界一様連続関数を用意する.
  \\[
  f(x) = \left\\{
	\begin{array}{ll}
	1 & x \in A \\\\
	1 - \frac{\inf_{y \in A} |x - y|}{\varepsilon} & x \in A_\varepsilon \backslash \\; A \\\\
	0 & x \not \in A \cup A_\varepsilon
	\end{array}
  \right.
  \\]
  仮定の&thinsp;\\(\lim_{n \to \infty} E[f(X_n)] = E[f(X)]\\)から,
  \\[
  \limsup_{n \to \infty} P_{n}(A) \leq \limsup_{n \to \infty} E[f(X_n)] = E[f(X)] \leq P(A_\varepsilon)
  \\]
  ここで,\\(\varepsilon \to 0\\)とすると,\\(A_\varepsilon\\)が閉集合なので,\\(P(\bigcap_{\varepsilon \to 0} A_\varepsilon)=P(A)\\)から,
  \\[
  \limsup_{n \to \infty} P_{n}(A) = P(A)
  \\]
  証明おわり.
