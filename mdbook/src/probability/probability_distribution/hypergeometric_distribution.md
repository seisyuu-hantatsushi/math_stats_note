## 超幾何分布
\\(N\\)個の要素からなる母集団の内,\\(M\\)個(\\(M \leq N\\))が\\(1\\)で,他が\\(0\\)だとする.
これから,\\(K\\)個(\\(K \leq N\\))を**非復元抽出**(sampling without replacement)した時,
その合計が\\(X\\)(\\(K\\)個取り出した内\\(1\\)が\\(X\\)個である)の確率を考える.

まず,\\(N\\)個の要素から\\(K\\)個取り出したときの組み合わせは,\\(_N C _K\\).
\\(1\\)の\\(M\\)個内\\(X\\)を取り出す組み合わせは,\\( _M C _X\\).
\\(0\\)の\\(N-M\\)個内\\(K-X\\)を取り出す組み合わせは,\\( _{N-M} C _{K-X}\\).
から,
\\[
	P(X=x:N,M,K) = \frac{\left(\begin{array}{c} M \\\\ x \end{array}\right)\left(\begin{array}{c} N-M \\\\ K-x \end{array}\right)}{\left( \begin{array}{c} N \\\\ K \end{array} \right)}, x=0,1,...,K
\\]
となりこれを**超幾何分布**(hypergeometric distribution)と言う.

まず,\\(\sum^{K} _{x=0} P(X=x:N,M,K) = 1\\)を確かめる.

\\[
(a+b)^N = (a+b)^{N-M}(a+b)^M
\\]

から

\\[
\begin{align}
\sum_{x=0}^N \left(\begin{array}{c} N \\\\ x \end{array}\right) a^xb^{x-N} &= \sum_{y=0}^{N-M} \left(\begin{array}{c} N-M-y \\\\ y \end{array}\right) a^y b^{N-M-y} \sum_{z=0}^{M} \left(\begin{array}{c} M \\\\ z \end{array}\right) a^z b^{M-z} \\\\
\sum_{y=0}^{N-M} \left(\begin{array}{c} N-M-y \\\\ y \end{array}\right) a^y b^{N-M-y} \sum_{z=0}^{M} \left(\begin{array}{c} M \\\\ z \end{array}\right) a^z b^{M-z} &=
\left(\left(\begin{array}{c} N-M \\\\ 0 \end{array}\right)a^0 b^{N-M-0} +
\left(\begin{array}{c} N-M \\\\ 1 \end{array}\right)a^1 b^{N-M-1} +
\left(\begin{array}{c} N-M \\\\ 2 \end{array}\right)a^2 b^{N-M-2} +
... +
\left(\begin{array}{c} N-M \\\\ N-(M-2) \end{array}\right)a^{N-(M-2)} b^{2} +
\left(\begin{array}{c} N-M \\\\ N-(M-1) \end{array}\right)a^{N-(M-1)} b^{1} +
\left(\begin{array}{c} N-M \\\\ N-M \end{array}\right)a^{N-M} b^{0} \right)
\left( \left(\begin{array}{c} M \\\\ 0 \end{array}\right)a^0 b^{M-0} +
\left(\begin{array}{c} M \\\\ 1 \end{array}\right)a^1 b^{M-1} +
\left(\begin{array}{c} M \\\\ 2 \end{array}\right)a^2 b^{M-2} +
... +
\left(\begin{array}{c} M \\\\ M-2 \end{array}\right)a^{M-2} b^{2} +
\left(\begin{array}{c} M \\\\ M-1 \end{array}\right)a^{M-1} b^{1} +
\left(\begin{array}{c} M \\\\ M \end{array}\right)a^{M} b^{0} \right) \\\\
&=\left(\left(\begin{array}{c} N-M \\\\ 0 \end{array}\right)a^0 b^{N-M-0}\right)\left( \left(\begin{array}{c} M \\\\ 0 \end{array}\right)a^0 b^{M-0} \right)
+\left(\left(\begin{array}{c} N-M \\\\ 1 \end{array}\right)a^1 b^{N-M-1} \right)\left( \left(\begin{array}{c} M \\\\ 0 \end{array}\right)a^0 b^{M-0} \right)
+\left(\left(\begin{array}{c} N-M \\\\ 0 \end{array}\right)a^0 b^{N-M-0}\right)\left(\left(\begin{array}{c} M \\\\ 1 \end{array}\right)a^1 b^{M-1} \right)
+\left(\left(\begin{array}{c} N-M \\\\ 0 \end{array}\right)a^0 b^{N-M-0}\right)\left(\left(\begin{array}{c} M \\\\ 2 \end{array}\right)a^2 b^{M-2}\right)
+\left(\left(\begin{array}{c} N-M \\\\ 1 \end{array}\right)a^1 b^{N-M-1}\right)\left(\left(\begin{array}{c} M \\\\ 1 \end{array}\right)a^1 b^{M-1}\right)
+\left(\left(\begin{array}{c} N-M \\\\ 2 \end{array}\right)a^2 b^{N-M-2}\right)\left(\left(\begin{array}{c} M \\\\ 0 \end{array}\right)a^0 b^{M-0}\right)+...\\\\
&=\left(\left(\begin{array}{c} N-M \\\\ 0 \end{array}\right)\left(\begin{array}{c} M \\\\ 0 \end{array}\right)\right)a^0 b^{N-0}+
\left(\left(\begin{array}{c} N-M \\\\ 1 \end{array}\right)\left(\begin{array}{c} M \\\\ 0 \end{array}\right)+\left(\begin{array}{c} N-M \\\\ 0 \end{array}\right)\left(\begin{array}{c} M \\\\ 1 \end{array}\right)\right)a^1 b^{N-1}+
\left(\left(\begin{array}{c} N-M \\\\ 2 \end{array}\right)\left(\begin{array}{c} M \\\\ 0 \end{array}\right)+\left(\begin{array}{c} N-M \\\\ 1 \end{array}\right)\left(\begin{array}{c} M \\\\ 1 \end{array}\right)+\left(\begin{array}{c} N-M \\\\ 0 \end{array}\right)\left(\begin{array}{c} M \\\\ 1 \end{array}\right)\right)a^2 b^{N-2} +
...+
\left(\left(\begin{array}{c} N-M \\\\ N-(M-1) \end{array}\right)\left(\begin{array}{c} M \\\\ M \end{array}\right)+\left(\begin{array}{c} N-M \\\\ N-M \end{array}\right)\left(\begin{array}{c} M \\\\ M-1 \end{array}\right)\right)a^{N-1} b^1+
\left(\left(\begin{array}{c} N-M \\\\ N-M \end{array}\right)\left(\begin{array}{c} M \\\\ M \end{array}\right)\right)a^N b^0 \\\\
&= \left(\sum^0_{x=0}\left(\begin{array}{c} N-M \\\\ 0-x \end{array}\right)\left(\begin{array}{c} M \\\\ x \end{array}\right)\right)a^0b^{N-0}+
\left(\sum^1_{x=0}\left(\begin{array}{c} N-M \\\\ 1-x \end{array}\right)\left(\begin{array}{c} M \\\\ x \end{array}\right)\right)a^1b^{N-1}+
\left(\sum^2_{x=0}\left(\begin{array}{c} N-M \\\\ 2-x \end{array}\right)\left(\begin{array}{c} M \\\\ x \end{array}\right)\right)a^2b^{N-2}+
...+
\left(\sum^M_{x=0}\left(\begin{array}{c} N-M \\\\ M-x \end{array}\right)\left(\begin{array}{c} M \\\\ x \end{array}\right)\right)a^Nb^{N-N}
\end{align}
\\]

項の係数を比較して,

\\[
 \left(\begin{array}{c} N \\\\ x \end{array}\right) = \sum^x_{k=0}\left(\begin{array}{c} N-M \\\\ x-k \end{array}\right)\left(\begin{array}{c} M \\\\ k \end{array}\right)
\\]

改めて\\(x=K,k=x\\)とおいて

\\[
 \left(\begin{array}{c} N \\\\ K \end{array}\right) = \sum^K_{k=0}\left(\begin{array}{c} N-M \\\\ K-x \end{array}\right)\left(\begin{array}{c} M \\\\ x \end{array}\right) \\\\
1 = \frac{\sum^K_{k=0}\left(\begin{array}{c} N-M \\\\ K-x \end{array}\right)\left(\begin{array}{c} M \\\\ x \end{array}\right)}{ \left(\begin{array}{c} N \\\\ K \end{array}\right)}
\\]
より,\\(\sum^{K} _{x=0} P(X=x:N,M,K) = 1\\)
