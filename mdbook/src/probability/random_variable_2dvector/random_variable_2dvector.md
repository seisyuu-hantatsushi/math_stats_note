## 確率変数2次元ベクトル
まず,2次元の場合を考える.2つの確率変数\\(X,Y\\)を用意する. &nbsp;\\(X=x,Y=y\\)である時の確率を,
\\[
P(\\{\omega|X(\omega)=x\\} \cap \\{\omega|Y(\omega)=y\\}) = P(X=x,Y=y), \\; x \in D_X, y \in D_Y
\\]
とかく.2つの事象が同時に発生する確率を得ることができるので,**同時確率**と言う.

### 同時累積分布関数
1次元の時と同様に,
\\[
	F_{X,Y}(x,y) := P(X \leq x, Y \leq y) = P(\\{\omega|X(\omega)\leq x\\} \cap \\{\omega|Y(\omega) \leq y\\})
\\]
を累積分布関数として定義する.2つの事象が同時に発生す分布となるので,**同時累積分布関数**という.
任意の関数\\(F(x,y)\\)が同時累積分布関数になるための必要十分条件は,
\\(x,x_1,x_2,y,y_1,y_2 \in \overline{\mathbb{R}}\\)に対して,以下の3つの条件が成立することである.
1. \\(\lim_{x \to -\infty} F(x,y) = 0, \\; \lim_{y \to -\infty} F(x,y) = 0, \\; \lim_{x \to \infty,y \to \infty} F(x,y) = 1\\)
1. \\( \forall x_1, \forall x_2, x_1 < x_2,\forall y_1, \forall y_2, y_1 < y_2 \to F(x_1,y_1) \leq F(x_2,y_2) \\)
1. \\(\lim_{x \to a+0,y \to b+0} F(x,y) = F(a,b) \\)

上の定義より,
\\[
\begin{align}
P(a < X \leq b, c < Y \leq d) &= P(\\{\omega|X(\omega)\leq b\\}\backslash\\{\omega| X(\omega) \leq a\\} \cap \\{\omega|Y(\omega)\leq d\\}\backslash\\{\omega|Y(\omega) \leq c\\}) \\\\
=& P((\\{\omega|X(\omega)\leq b\\} \cap \\{\omega| X(\omega) \leq a\\}^c) \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c\\}^c)) \\\\
=& P((\\{\omega|X(\omega)\leq b\\} \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c\\}^c)) \cap \\\\
	&(\\{\omega|X(\omega) \leq a \\}^c \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c \\}^c))) \\\\
=& P(\\{\omega|X(\omega)\leq b\\} \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c\\}^c)) + \\\\
 & P(\\{\omega| X(\omega) \leq a \\}^c \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c\\}^c)) - \\\\
 & P((\\{\omega|X(\omega)\leq b\\} \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c \\}^c)) \cup \\\\
	&(\\{\omega|X(\omega) \leq a\\}^c \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c \\}^c))) \\\\
=& P(\\{\omega|X(\omega)\leq b\\} \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c \\}^c)) + \\\\
 & P(\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c \\}^c) - P(\\{\omega| X(\omega) \leq a \\} \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega|Y(\omega) \leq c\\}^c)) - \\\\
 & P(\\{\omega|X(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c\\}^c) \\\\
=& P(\\{\omega|X(\omega)\leq b\\} \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega|c \leq Y(\omega)\\}^c)) - P(\\{\omega| X(\omega) \leq a \\} \cap (\\{\omega|Y(\omega)\leq d\\}\cap\\{\omega| Y(\omega) \leq c \\}^c)) \\\\
=& P((\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega)\leq d\\}) \cap (\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega) \leq c\\}^c)) - \\\\
& P((\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega)\leq d\\}) \cap (\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega) \leq c\\}^c)) \\\\
=& P(\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega)\leq d\\}) +  P(\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega) \leq c\\}^c) - \\\\
& P((\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega)\leq d\\}) \cup (\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega) \leq c\\}^c)) - \\\\
& P(\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega)\leq d\\}) - P(\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega) \leq c \\}^c) + \\\\
& P((\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega)\leq d\\}) \cup (\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega) \leq c\\}^c)) \\\\
=& P(\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega)\leq d\\}) +  P(\\{\omega|X(\omega)\leq b\\} \cap \\{\omega | Y(\omega) \leq c\\}^c) - \\\\
& P((\\{\omega|X(\omega)\leq b\\}) - \\\\
& P(\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega)\leq d\\}) - P(\\{\omega| X(\omega) \leq a \\} \cap \\{\omega| Y(\omega) \leq c\\}^c) + \\\\
& P((\\{\omega| X(\omega) \leq a \\}) \\\\
=& P(\\{\omega|X(\omega)\leq b\\} \cap \\{\omega|Y(\omega)\leq d\\}) -  P(\\{\omega|X(\omega)\leq b\\} \cap \\{\omega | Y(\omega) \leq c\\}) - \\\\
& P(\\{\omega| X(\omega) \leq a \\} \cap \\{\omega|Y(\omega)\leq d\\}) + P(\\{\omega| X(\omega) \leq a \\} \cap \\{\omega| Y(\omega) \leq c\\}) + \\\\
=& F_{X,Y}(b,d) - F_{X,Y}(b,c) - F_{X,Y}(a,d) + F_{X,Y}(a,c)
\end{align}
\\]

### 周辺累積分布関数
同時累積分布関数\\(F_{X,Y}(x,y)\\)を定義した時, &nbsp;\\(y \to \infty\\)とすると,
\\[
\begin{align}
	\lim_{y \to \infty} F_{X,Y}(x,y) &= P(\\{\omega|X(\omega)\leq x\\} \cap \\{\omega|Y(\omega) \leq \infty\\}) \\\\
	&= P(\\{\omega|X(\omega)\leq x\\} \cap \Omega) = P(\\{\omega|X(\omega)\leq x\\}) = F_X(x)
\end{align}
\\]
これを,\\(X\\)の周辺累積分布関数という.

### 同時確率密度関数
同時累積分布関数の\\(x,y\\)での変化量を得ることができると,積分することにより任意の事象に対する確率が得られる.
\\[
\begin{align}
	\frac{\partial^2 P(\\{\omega|X(\omega)\leq x\\} \cap \\{\omega|Y(\omega) \leq y\\})}{\partial x \partial y} &= \lim_{\Delta x \to 0} \lim_{\Delta y \to 0} \frac{P(\\{\omega|X(\omega)\leq x + \Delta x\\} \cap \\{\omega|Y(\omega) \leq y + \Delta y\\}) - P(\\{\omega|X(\omega)\leq x\\} \cap \\{\omega|Y(\omega) \leq y  + \Delta y\\})}{\Delta x \Delta y} \\\\
	&= \lim_{\Delta x \to 0} \lim_{\Delta y \to 0} \frac{P(X \leq x + \Delta x, Y \leq y + \Delta y) - P(X \leq x, Y \leq y)}{\Delta x \Delta y} \\\\
	&= \lim_{\Delta x \to 0} \lim_{\Delta y \to 0} \frac{F_{X,Y}(x + \Delta x, y + \Delta y) - F_{X,Y}(x, y)}{\Delta x \Delta y} \\\\
	&= \frac{\partial^2 F_{X,Y}(x, y)}{\partial x \partial y}
\end{align}
\\]
\\(F_{X,Y}(x, y)\\)が微分可能なら,\\(\frac{\partial^2 F_{X,Y}(x, y)}{\partial x \partial y} = f_{X,Y}(x,y)\\)として,&nbsp;\\(f_{X,Y}(x,y)\\)を**同時確率密度関数**という.

定義より,
\\[
P(X \leq a,Y \leq c) = F_{X,Y}(a,c) = \int^c_{-\infty} \int^a_{-\infty} f_{X,Y}(x,y) dx dy
\\]

\\[
\begin{align}
P(a < X \leq b, c < Y \leq d) &= F_{X,Y}(b,d) - F_{X,Y}(b,c) - F_{X,Y}(a,d) + F_{X,Y}(a,c) \\\\
&= \int^d_{-\infty} \int^b_{-\infty} f_{X,Y}(x,y) dx dy - \int^c_{-\infty} \int^b_{-\infty} f_{X,Y}(x,y) dx dy - \int^d_{-\infty} \int^a_{-\infty} f_{X,Y}(x,y) dx dy + \int^c_{-\infty} \int^a_{-\infty} f_{X,Y}(x,y) dx dy \\\\
&= \int^d_c \int^b_{-\infty} f_{X,Y}(x,y) dx dy - (\int^d_{-\infty} \int^a_{-\infty} f_{X,Y}(x,y) dx dy - \int^c_{-\infty} \int^a_{-\infty} f_{X,Y}(x,y) dx dy) \\\\
&= \int^d_c \int^b_{-\infty} f_{X,Y}(x,y) dx dy - \int^d_c \int^a_{-\infty} f_{X,Y}(x,y) dx dy \\\\
&= \int^d_c \int^b_a f_{X,Y}(x,y) dx dy
x\end{align}
\\]
\\[
f_{X,Y}(x,y) \geq 0
\\]
\\[
\int_{D_Y} \int_{D_X} f_{X,Y}(x,y) dxdy = 1
\\]

### 周辺確率密度関数
同時確率密度関数を\\(f_{X,Y}(x,y)\\)と定義した時,
\\[
\lim_{y \to \infty} F_{X,Y}(x,y) = \int ^x _{-\infty} \int ^{\infty} _{-\infty} f _{X,Y}(x,y) dy dx = F_X(x) = \int ^x _{-\infty} f _{X}(x) dx
\\]
から,
\\[
\int ^{\infty} _{-\infty} f _{X,Y}(x,y) dy  = f _{X}(x)
\\]
これを\\(X\\)の周辺確率密度関数という.
