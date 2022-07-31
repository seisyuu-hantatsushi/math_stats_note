## 超幾何分布
\\(N\\)個の要素からなる母集団の内,\\(M\\)個(\\(M \leq N\\))が\\(1\\)で,他が\\(0\\)だとする.
これから,\\(K\\)個(\\(K \leq N\\))を**非復元抽出**(sampling without replacement)した時,
その合計が\\(X\\)(\(K\\)個取り出した内\\(1\\)が\\(X\\)個である)の確率を考える.

まず,\\(N\\)個の要素から\\(K\\)個取り出したときの組み合わせは,\\(_N C _K\\).
\\(1\\)の\\(M\\)個内\\(X\\)を取り出す組み合わせは,\\( _M C _X\\).
\\(0\\)の\\(N-M\\)個内\\(K-X\\)を取り出す組み合わせは,\\( _{N-M} C _{K-X}\\).
から,
\\[
	P(X=x:N,M,K) = \frac{\left(\begin{array}{c} M \\\\ x \end{array}\right)\left(\begin{array}{c} N-M \\\\ K-x \end{array}\right)}{\left( \begin{array}{c} N \\\\ K \end{array} \right)}, x=0,1,...,K
\\]
となりこれを**超幾何分布**(hypergeometric distribution)と言う.

まず,\\(\sum^{K} _{x=0} P(X=x:N,M,K) = 1\\)を確かめる.
