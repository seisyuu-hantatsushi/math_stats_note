## 変数変換
２つの確率変数\\(X,Y\\)を用意し,この二つの確率変数から新たに確率変数を
生成する関数\\(S=s(X,Y),T=t(X,Y)\\)を用意する.
では,２つの確率変数の同時確率密度関数を\\(f_{X,Y}(x,y)\\)としたとき,
変数変換後のは同時確率密度関数どうなるだろうか?
まず,関数\\(s,t\\)は偏微分可能であり,逆関数が存在するとする.
重積分の変数変換の公式から,
\\[
    \int \int f_{X,Y}(x,y)dxdy = \int \int f_{X,Y}(s^{-1}(s,t),t^{-1}(s,t))|J(s,t)| dsdt
\\]
\\[
J(s,t) = \det \left( \begin{array}{c} \frac{\partial s(x,y)}{\partial x}  & \frac{\partial s(x,y)}{\partial y} \\\\
\frac{\partial t(x,y)}{\partial x}  & \frac{\partial t(x,y)}{\partial y}
\end{array} \right) = \frac{\partial s(x,y)}{\partial x}\frac{\partial t(x,y)}{\partial y} - \frac{\partial s(x,y)}{\partial y}\frac{\partial t(x,y)}{\partial x}
\\]
から
\\[
    f_{S,T}(s,t) = f_{X,Y}(s^{-1}(s,t),t^{-1}(s,t))|J(s,t)|
\\]
となり,
\\[
    f_{X,Y}(x,y) = \frac{f_{S,T}(s,t)}{|J(s,t)|}
\\]
