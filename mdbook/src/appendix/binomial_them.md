## 二項定理
\\[
	(a+b)^n
\\]
を展開したときの各項\\(a^k b^{n-k},k=0,1,\cdots,n\\)の係数を考える.
この係数は,\\(n\\)個の内,\\(k\\)個の\\(a\\)を取り,残りを\\(b\\)に取るような,組み合わせになるので,\\({}_n C _k\\)で表すことができる.
であるので,
\\[
	(a+b)^n = \sum ^{n} _{k=0} \left(  \begin{array}{l}
		n \\\\
		k
	\end{array} \right) a^k b^{n-k}
\\]
と表すことができる.

- 証明
  \\[
  \begin{align}
	  \left(  \begin{array}{c}
		n \\\\
		k
	\end{array} \right) +
	  \left(  \begin{array}{c}
		n \\\\
		k-1
	\end{array} \right) &= \frac{n!}{(n-k)!k!} + \frac{n!}{(n-(k-1))!(k-1)!} \\\\
	&= \frac{n!}{(n-k)!k!} + \frac{n!}{(n-k+1)!(k-1)!} \\\\
	&= (n-k+1)\frac{n!}{(n-k+1)!k!} + k \frac{n!}{(n-k+1)!k!} \\\\
	&= (n+1)\frac{n!}{(n+1-k)!k!} \\\\
	&= \frac{(n+1)!}{(n+1-k)!k!} = 
	  \left(  \begin{array}{c}
		n+1 \\\\
		k
	\end{array} \right)
  \end{align}
  \\]
  であるので,帰納法により証明する.
  まず,\\(n=0\\)のときは,
  \\[
	  (a+b)^0 = \sum ^{0} _{k=0} \left(  \begin{array}{l}
		0 \\\\
		0
	\end{array} \right) a^0 b^0 = 1
  \\]
  \\(n=1\\)のときは,
  \\[
	  (a+b)^1 = \sum ^{1} _{k=0} \left(  \begin{array}{l}
		1 \\\\
		k
	\end{array} \right) a^k b^{1-k} = \left(  \begin{array}{l}
		1 \\\\
		0
	\end{array} \right)a^0 b^1 + 
	 \left(  \begin{array}{l}
		1 \\\\
		1
	\end{array} \right)a^1 b^0 = a + b
  \\]
  \\(n=2\\)のときは,
  \\[
	  (a+b)^2 = \sum ^{2} _{k=0} \left(  \begin{array}{l}
		2 \\\\
		k
	\end{array} \right) a^k b^{1-k} = \left(  \begin{array}{l}
		2 \\\\
		0
	\end{array} \right)a^0 b^2 +
	 \left(  \begin{array}{l}
		2 \\\\
		1
	\end{array} \right)a^1 b^1 +
	\left(  \begin{array}{l}
		2 \\\\
		2
	\end{array} \right) a^2 b^0 = a^2 + 2ab + b^2
  \\]
  \\(n=l\\)のときに以下が成立するとする,
  \\[
	(a+b)^l = \sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^k b^{l-k}
  \\]
  \\(n=l+1\\)のとき,
  \\[
    \begin{align}
	(a+b)^l(a+b) &= (a+b) \\left\\{ \sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^k b^{l-k} \right\\} \\\\
	&= a \sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^k b^{l-k} + b \sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^k b^{l-k} \\\\
	&= \sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^{k+1} b^{l-k} + \sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^k b^{l-k+1} \\\\
	&= \sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^{k+1} b^{l-k} +
	\sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^k b^{l-k+1} \\\\
	&= \sum ^{l+1} _{k'=1} \left(  \begin{array}{c}
		l \\\\
		k'-1
	\end{array} \right) a^{k'} b^{l-(k'-1)} +
	\sum ^{l} _{k=0} \left(  \begin{array}{c}
		l \\\\
		k
	\end{array} \right) a^k b^{l+1-k} +
	\left(  \begin{array}{c}
		l+1 \\\\
		l+1
	\end{array} \right) a^{l+1} b^{l+1-(l+1)} -
	\left(  \begin{array}{c}
		l+1 \\\\
		l+1
	\end{array} \right) a^{l+1} b^{l+1-(l+1)}
	\\\\
	\end{align}
  \\]

