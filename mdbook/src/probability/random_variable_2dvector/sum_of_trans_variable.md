## 確率変数の和の分布
2つの確率変数\\(X\\)と\\(Y\\)が独立で,それぞれの確率密度関数を\\(f _X(x),f _Y(y)\\)とする.
このときの,\\(S=X+Y\\)の分布を求める場合,畳み込みを行う,確率母関数,特性関数を利用する方法がある.

### 畳み込み

連続確率変数の場合,\\(S=X+Y,T=Y\\)なる変数変換を考えると,ヤコビアンは,
\\[
	J(s,t) = \left|
		\begin{array} {c}
			\frac{\partial s}{\partial x} & \frac{\partial s}{\partial y} \\\\
			\frac{\partial t}{\partial x} & \frac{\partial t}{\partial y}
		\end{array} \right|
		= \left|
		\begin{array} {c}
			1 &  1 \\\\
			0 &  1
		\end{array} \right| = 1
\\]
\\[
	\int \int f _X(x) f _Y(y) dx dy = \int \int f _X(s-t) f _Y(t) |J(s,t)| ds dt = \int \int f _{S,T}(s,t) |J(s,t)|dsdt
\\]
から,
\\[
	f _{S,T}(s,t) = f _X(s-t) f _Y(t)
\\]
ここで,得たいのは,確率変数\\(S\\)の確率密度関数関数である.同時確率密度関数の周辺分布から,
\\[
	f _S(s) = \int _{\Omega} f _{S,T}(s,t) dt = \int _{\Omega} f _X(s-t) f _Y(t)  dt
\\]
と書ける.これを**畳み込み**(convolution)といい. \\(f _S(s) = f _X * f _Y(s)\\)と書く.

### 特性関数を利用する方法

2つの確率変数\\(X\\)と\\(Y\\)の特性関数を\\(\varphi_X(t),\varphi_Y(t)\\)とする,この時,\\(Z = X + Y\\)の特性関数は,
\\[
	\varphi _Z(t) = E[e^{itZ}] = E[e^{it(X+Y)}] = E[e^{itX} e^{itY}] = E[e^{itX}] E[e^{itY}] = \varphi _X(t) \varphi _Y(t)
\\]
となる.Levyの反転公式によると,特性関数と分布は一対一対応するので,\\(\varphi _X(t) \varphi _Y(t)\\)を特性関数とする分布を見つけることができれば,それは,\\(\varphi _Z(t)\\)の分布となる.
