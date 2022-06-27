## ラグランジュの未定乗数法
拘束条件がある関数の極値を調べるにはどうすればいいだろうか?
単純に考えれば,実数値関数の微分をとって0になる点を求めれば極値である.
しかし,拘束条件がある場合では単純ではない.
拘束条件のもと,調べたい関数の全微分を取って極値を調べる.

### 2変数の場合.
2つの微分可能な連続実数値関数\\(f(x,y),g(x,y)\\)とし,
以下のような微分可能な連続実数値関数を用意する.
\\[
	{\mathscr L}(x,y,\lambda) = f(x,y) - \lambda g(x,y)
\\]
上記の偏微分が\\((x,y,\lambda) = (a, b, l)\\)のとき,
\\[
\left.\frac{\partial {\mathscr L}(x,y,\lambda)}{\partial x}\right|_{(a,b,l)} = \left.\frac{\partial {\mathscr L}(x,y,\lambda)}{\partial y}\right| _{(a,b,l)} = \left. \frac{\partial {\mathscr L}(x,y,\lambda)}{\partial \lambda} \right| _{(a,b,l)} = 0
\\]
が成立する場合,\\((x,y,\lambda) = (a, b, l)\\)で\\(f(x,y)\\)は,\\(g(x,y) = 0\\)の拘束条件で極値を取る.

- 証明  
  連立方程式は,
  \\[
    \left\\{
	\begin{array}{ll}
		\left. \displaystyle \frac{\partial {\mathscr L}(x,y,\lambda)}{\partial \lambda} \right| _{(a,b,l)} &= g(a,b) = 0 \\\\
		\left. \displaystyle \frac{\partial {\mathscr L}(x,y,\lambda)}{\partial x} \right| _{(a,b,l)} &= \left. \displaystyle \frac{\partial f(x,y)}{\partial x} \right| _{(a,b,l)}  - \lambda \left. \displaystyle \frac{\partial g(x,y)}{\partial x} \right| _{(a,b,l)} = 0 \\\\
		\left. \displaystyle \frac{\partial {\mathscr L}(x,y,\lambda)}{\partial y} \right| _{(a,b,l)} &= \left. \displaystyle \frac{\partial f(x,y)}{\partial y} \right| _{(a,b,l)}  - \lambda \left. \displaystyle \frac{\partial g(x,y)}{\partial y} \right| _{(a,b,l)} = 0
	\end{array}
  \right.
  \\]
  拘束条件は,第1式が満たしている.\\((\frac{\partial g(x,y)}{\partial x},\frac{\partial g(x,y)}{\partial y}) = (0,0)\\)ならば,\\(g(x,y)\\)が定数を表しているので,\\(x,y\\)を拘束せず,
  拘束条件のない極値を求める問題となる.

  \\(\left(\left. \frac{\partial g(x,y)}{\partial x}\right|_{(a,b)}, \left.\frac{\partial g(x,y)}{\partial y}\right| _{(a,b)} \right) \not = (0,0)\\)の場合を考える.
  \\(\left.\frac{\partial g(x,y)}{\partial y}\right| _{(a,b)}  \not = 0\\)とする.
  前述の仮定と陰関数定理より,\\(a,b\\)の近傍で微分可能な連続関数\\(y=h(x)\\)が存在する.
  \\(h\\)は微分可能で,\\(g(x,y) = 0\\)なので,
  \\[
	  \frac{d g(x,y)}{d x} = \frac{d g(x,h(x))}{d x} = \frac{\partial g}{\partial x} + \frac{\partial g}{\partial y}\frac{d h}{d x} = 0
  \\]
  から,
  \\[
	  \frac{d h(x)}{d x} = -\frac{\frac{\partial g(x,y)}{\partial x}}{\frac{\partial g(x,y)}{\partial y}}
  \\]
  また,\\(f(x,y) = f(x,h(x))\\)と書くことができ,
  \\[
	  \frac{d f(x,y)}{d x} = \frac{d f(x,h(x))}{d x} = \frac{\partial f}{\partial x} + \frac{\partial f}{\partial y}\frac{d h}{d x}
  \\]
  これが,\\((x,y) = (a,b)\\)で極値を取るなら,
  \\[
  \left. \frac{\partial f(x,y)}{\partial x} \right| _{(a,b)} + \left. \frac{\partial f(x,y)}{\partial y} \frac{d h(x)}{d x} \right| _{(a,b)} = 0
  \\]
  \\(\displaystyle \frac{d h(x)}{d x} = -\frac{\frac{\partial g(x,y)}{\partial x}}{\frac{\partial g(x,y)}{\partial y}}\\)から,
  \\[
  \left. \frac{\partial f(x,y)}{\partial x} \right| _{(a,b)} - \left. \frac{\partial f(x,y)}{\partial y} \frac{\frac{\partial g(x,y)}{\partial x}}{\frac{\partial g(x,y)}{\partial y}} \right| _{(a,b)} = \left. \frac{\partial f(x,y)}{\partial x} \right| _{(a,b)} - \left. \frac{\frac{\partial f(x,y)}{\partial y}}{\frac{\partial g(x,y)}{\partial y}}\frac{\partial g(x,y)}{\partial x} \right| _{(a,b)} = 0
  \\]
  ここで,\\(\displaystyle l=\left. \frac{\frac{\partial f(x,y)}{\partial y}}{\frac{\partial g(x,y)}{\partial y}}\right| _{(a,b)}\\)とおくと,
  \\[
   \left. \frac{\partial f(x,y)}{\partial x} \right| _{(a,b)} - \left. l \frac{\partial g(x,y)}{\partial x} \right| _{(a,b)} = \left. \frac{\partial f(x,y)}{\partial x} \right| _{(a,b,l)} - \lambda \left. \frac{\partial g(x,y)}{\partial x} \right| _{(a,b,l)} = 0
  \\]
  第2式が成立し,第3式は,
  \\[
    \begin{align}
  \left. \frac{\partial f(x,y)}{\partial y} \right| _{(a,b,l)} - \lambda \left. \frac{\partial g(x,y)}{\partial y} \right| _{(a,b,l)} &= \left. \frac{\partial f(x,y)}{\partial y} \right| _{(a,b)} - l \left. \frac{\partial g(x,y)}{\partial y} \right| _{(a,b)} \\\\
    &= \left. \frac{\partial f(x,y)}{\partial y} \right| _{(a,b)} - \left. \frac{\frac{\partial f(x,y)}{\partial y}}{\frac{\partial g(x,y)}{\partial y}} \frac{\partial g(x,y)}{\partial y} \right| _{(a,b)} = 0
  \end{align}
  \\]
  となる. \\(\left.\frac{\partial g(x,y)}{\partial x}\right| _{(a,b)}  \not = 0\\)のときも同様.
