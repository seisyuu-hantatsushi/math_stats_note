# 期待値
## 期待値
確率変数を引数に取る関数を考える.\\(X=\\{x | x = X(\omega) \land \omega \in \Omega \\}\\)と定義する.
\\(X\\)は確率変数の取りうる値の集合となる.
\\[
	g: X \mapsto \mathbb{R}
\\]
を用いて,
\\[
\begin{align}
E[g(X)] &= \int_{\Omega} g(X(\omega))P(d\omega) \\\\
 &=\int^{\infty} _{-\infty} g(x)dP(x) \\\\
 &= \int^{\infty} _{-\infty} g(x)\\, f_X(x) dx
\end{align}
\\]
を\\(g(X)\\)の期待値と言う.
期待値は実測値と実測値が発生する確率の積分を事象全体で行ったもので,
一回の試行で得られる見込みの値となる.

事象を制限した期待値は
\\[
E[X:A] = \int _{A} X(\omega) P(d\omega)
\\]

と表し,\\(I _{A} : \Omega \mapsto \\{0,1\\}\\)なる集合\\(A\\)の指示関数を用意すると
\\[
E[X:A] = E[X \cdot I _{A}] = \int _{\Omega} X(\omega) I _A(\omega) P(d\omega) = \int _{A} X(\omega) P(d\omega)
\\]
と書くことができる.

### 期待値の性質
期待値は線形性を持つ.\\(a,b,c\\)を定数とし,\\(g(X),h(X)\\)を確率変数をとる関数とすると,以下が成立する.
\\[
E[ag(X)+bh(X)+c] = aE[g(X)]+bE[h(X)]+c
\\]
- 証明
\\[
\begin{align}
E[ag(X)+bh(X)+c] &= \int^{\infty} _{-\infty} (ag(x)+bh(x)+c)f_X(x) dx \\\\
&= a \int^{\infty} _{-\infty} g(x) f_X(x)dx + b \int^{\infty} _{-\infty} h(x) f_X(x) dx + c \int^{\infty} _{-\infty} f_X(x) dx \\\\
&= aE[g(X)] + bE[h(X)] + c
\end{align}
\\]
証明終わり.  

任意の定数と\\(g(x) \geq 0\\)に対して,
\\[
	\forall a > 0, E[g(x)] \geq a \int _ {g(x) \geq a} f_X(x) dx = aP(g(x) \geq a) \tag{2.3.2.1}
\\]

- 証明  
\\(\forall a > 0\\)に対して,
\\[
\begin{align}
	 E[g(x)] &= \int ^{\infty} _ {-\infty} g(x) f _ X(x) dx \\\\
	 &= \int_{g(x) \geq a} g(x)\\, f _ X(x) dx + \int_{g(x) < a} g(x)\\, f _ X(x) dx
\end{align}
\\]
積分範囲が\\(g(x) \geq a\\)となる\\(x\\)なので,
\\[
\begin{align}
\int_{g(x) \geq a} g(x)\\, f _ X(x) dx &\geq a \int_{g(x) \geq a} f _ X(x) dx
\end{align}
\\]
から
\\[
\begin{align}
	 E[g(x)] &= \int ^{\infty} _ {-\infty} g(x) f _ X(x) dx \\\\
	 &= \int_{g(x) \geq a} g(x)\\, f _ X(x) dx + \int_{g(x) < a} g(x)\\, f _ X(x) dx \\\\
	 &\geq \int_{g(x) \geq a} g(x)\\, f _ X(x) dx \\\\
	 &\geq a \int_{g(x) \geq a} f _ X(x) dx = aP(g(x) \geq a)
\end{align}
\\]
証明終わり.  
(2.3.2.1)式を**Markovの不等式**と言う.
