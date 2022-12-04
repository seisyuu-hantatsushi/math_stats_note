## 連続写像定理

### 連続写像定理
確率変数列\\(\\{X _i\\} _{i \in \overline{\mathbb{N} _+}}\\)と実数\\(x\\)に対して,
\\[
	X _n \xrightarrow{p} x
\\]
である時,\\(g: \mathbb{R} \mapsto \mathbb{R}\\)を連続関数とすると,
\\[
	g(X _n) \xrightarrow{p} g(x)
\\]
が成立する.

- 証明

確率変数列\\(X _n\\)は,確率収束するので,
\\[
	\lim _{n \to \infty} P(|X _n-x| < \delta) = 1
\\]

関数\\(g\\)が連続関数ということは,任意の正数\\(\varepsilon,\delta\\)に対して,

\\[
	|X _n - x| < \delta ならば, |g(X _n) - g(x)| < \varepsilon
\\]

であるので,

\\[
	P(|X _n - x| < \delta) < P(|g(X _n) - g(x)| < \varepsilon) <= 1
\\]

から,

\\[
	\lim_{n \to \infty} P(|g(X _n) - g(x)| < \varepsilon) = 1
\\]
が成立する.

### スラツキーの定理

