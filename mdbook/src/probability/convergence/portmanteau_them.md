## Portmanteau定理
分布収束と同値な定義を示した定理を**Portmanteau(両開き旅行かばん語)定理**という.

### Portmanteau定理
確率変数\\(X\\),確率変数列 \\( \\{X _n \\} _{n \in \mathbb{N} _+} \\)を用意し,
それそれに対応する分布関数を,\\(F _X,F _{X_n}\\)とすると,
以下の定義は同値である.

1. \\(X_n \xrightarrow{d} X\\)
1. 任意の有界連続関数&thinsp;\\(f:\mathbb{R} \mapsto \mathbb{R}\\)対して
   \\[
	   E[f(X _n)] \to E[f(X)]
   \\]
1. 任意の有界一様連続関数&thinsp;\\(f:\mathbb{R} \mapsto \mathbb{R}\\)対して
   \\[
	   E[f(X _n)] \to E[f(X)]
   \\]
1. 任意の開集合Aに対して,&thinsp;\\(\limsup_{n \to \infty} P_{n}(A) \leq P_{n}(A)\\)
1. 任意の閉集合Aに対して,&thinsp;\\(\liminf_{n \to \infty} P_{n}(A) \geq P_{n}(A)\\)
