## ベクトルと行列の微分
### 定義と表記
#### ベクトルと行列の表記
\\(\boldsymbol{x}=\begin{pmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n \end{pmatrix}\\)

\\(\boldsymbol{A}=\begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1n}  \\\\
                                  a_{21} & a_{22} & \cdots & a_{2n}  \\\\
                                  \vdots & \vdots & \ddots & \vdots  \\\\
                                  a_{n1} & a_{n2} & \cdots & a_{nm} \end{pmatrix}\\)
#### 転置記号
\\(\boldsymbol{x}^T=(x_1,x_2,\cdots,x_n) \\)

\\(\boldsymbol{A}^T=\begin{pmatrix} a_{11} & a_{21} & \cdots & a_{n1}  \\\\
                                    a_{12} & a_{22} & \cdots & a_{n1}  \\\\
                                  \vdots & \vdots & \ddots & \vdots  \\\\
                                  a_{1n} & a_{2n} & \cdots & a_{mn} \end{pmatrix}\\)
## 演算
### 行列の積
\\[
\boldsymbol{A}=\begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1m}  \\\\
a_{21} & a_{22} & \cdots & a_{2m}  \\\\
\vdots & \vdots & \ddots & \vdots  \\\\
a_{n1} & a_{n2} & \cdots & a_{nm} \end{pmatrix} \\
\\]
\\[
\boldsymbol{B}=\begin{pmatrix} b_{11} & b_{12} & \cdots & b_{1l}  \\\\
b_{21} & b_{22} & \cdots & b_{2l}  \\\\
\vdots & \vdots & \ddots & \vdots  \\\\
b_{m1} & b_{m2} & \cdots & b_{ml} \end{pmatrix}
\\]
と\\(n \times m\\)行列と\\(m \times l\\)行列を用意する.  
行列の積を
\\[
\boldsymbol{A}\boldsymbol{B}=\begin{pmatrix} 
\sum^m_{i=1} a_{1i}b_{i1} & \sum^m_{i=1} a_{1i}b_{i2} & \sum^m_{i=1} a_{1i}b_{i3} & \cdots & \sum^m_{i=1} a_{1i}b_{il} \\\\
\sum^m_{i=1} a_{2i}b_{i1} & \sum^m_{i=1} a_{2i}b_{i2} & \sum^m_{i=1} a_{2i}b_{i3} & \cdots & \sum^m_{i=1} a_{2i}b_{il} \\\\
\vdots & \vdots & \ddots & \vdots  \\\\
\sum^m_{i=1} a_{ni}b_{i1} & \sum^m_{i=1} a_{ni}b_{i2} & \sum^m_{i=1} a_{ni}b_{i3} & \cdots & \sum^m_{i=1} a_{ni}b_{il}
\end{pmatrix} \\
\\]
と定義する. 可換性は無い. 被乗数側の列数と乗数側の行数が一致しないと行けない.

### ベクトルの内積
\\(\boldsymbol{x}^T=(x_1,x_2,\cdots,x_n) \\)
\\(\boldsymbol{y}^T=(y_1,y_2,\cdots,y_n) \\)
とn列ベクトルを用意する.  
ベクトルの内積(ドット積)は以下のように定義する.  
\\[ \boldsymbol{x} \cdot \boldsymbol{y}\\ = x_1y_1 + x_2y_2 + \cdots + x_ny_n \\]
縦ベクトルを\\(1 \times n\\)の横ベクトルを\\(n \times 1\\)の行列と見なすと,
\\[ \boldsymbol{x} \cdot \boldsymbol{y}\\ = \boldsymbol{x}^T\boldsymbol{y} = \boldsymbol{y}^T\boldsymbol{x} \\]
と表せる.

### 転置に関する公式
\\[
\begin{align}
\boldsymbol{x}^T \boldsymbol{A} &= \begin{pmatrix} x_{1} & x_{2} & \cdots & x_{n} \end{pmatrix} \begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1m}  \\\\
a_{21} & a_{22} & \cdots & a_{2m}  \\\\
\vdots & \vdots & \ddots & \vdots  \\\\
a_{n1} & a_{n2} & \cdots & a_{nm} \\\\
\end{pmatrix} \\\\
&= \begin{pmatrix} a_{11}x_{1} + a_{21}x_{2} + \cdots + a_{n1}x_{n} & a_{12}x_{1} + a_{22}x_{2} + \cdots + a_{n2}x_{n} & \cdots & a_{1m}x_{1} + a_{2m}x_{2} + \cdots + a_{nm}x_{n}  \end{pmatrix} \\\\
&= \begin{pmatrix} a_{11} & a_{21} & \cdots & a_{n1}  \\\\
a_{12} & a_{22} & \cdots & a_{n2}  \\\\
\vdots & \vdots & \ddots & \vdots  \\\\
a_{1m} & a_{2m} & \cdots & a_{nm} \\\\
\end{pmatrix} \begin{pmatrix} x_1 \\\\  x_2 \\\\ \vdots \\\\  x_n \end{pmatrix} \\\\
&= \boldsymbol{A}^T \boldsymbol{x}
\end{align}
\\]

### 微分演算
微分演算子を以下のように定義する.
\\[ \frac{\partial}{\partial\boldsymbol{x}}=\begin{pmatrix} \frac{\partial}{\partial x_1} \\\\ \frac{\partial}{\partial x_2} \\\\ \vdots \\\\ \frac{\partial}{\partial x_n} \end{pmatrix}\\]
#### 演算定義
\\[
\boldsymbol{f}(\boldsymbol{x}) = \begin{pmatrix} f_1(\boldsymbol{x}) &  f_2(\boldsymbol{x}) & \cdots & f_m(\boldsymbol{x}) \end{pmatrix}
\\]
として,
\\[
\frac{\partial \boldsymbol{f}(\boldsymbol{x})}{\partial\boldsymbol{x}} = \begin{pmatrix} \frac{\partial f_1(\boldsymbol{x}) }{\partial x_1}  & \frac{\partial f_1(\boldsymbol{x}) }{\partial x_2} & \cdots & \frac{\partial f_1(\boldsymbol{x}) }{\partial x_n} \\\\
\frac{\partial f_2(\boldsymbol{x}) }{\partial x_1}  & \frac{\partial f_2(\boldsymbol{x}) }{\partial x_2} & \cdots & \frac{\partial f_2(\boldsymbol{x}) }{\partial x_n} \\\\ 
\vdots & \vdots & \ddots & \vdots  \\\\
\frac{\partial f_m(\boldsymbol{x}) }{\partial x_1}  & \frac{\partial f_m(\boldsymbol{x}) }{\partial x_2} & \cdots & \frac{\partial f_m(\boldsymbol{x}) }{\partial x_n}
\end{pmatrix}
\\]
#### 公式
\\[
	\frac{\partial \boldsymbol{x}}{\partial\boldsymbol{x}} = \begin{pmatrix} 1 & 0 & \cdots & 0 \\\\
	0 & 1 & \cdots & 0 \\\\
	0 & 0 & \ddots & 0 \\\\
	0 & 0 & \cdots & 1 \end{pmatrix} = \boldsymbol{I}
\\]

\\[
\begin{align}
	\frac{\partial \boldsymbol{A} \boldsymbol{x}}{\partial\boldsymbol{x}} &= 
	\begin{pmatrix} \frac{\partial}{\partial x_1} \\\\ \frac{\partial}{\partial x_2} \\\\ \vdots \\\\ \frac{\partial}{\partial x_n} \end{pmatrix} \begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\\\
a_{21} & a_{22} & \cdots & a_{2n}  \\\\
\vdots & \vdots & \ddots & \vdots  \\\\
a_{m1} & a_{m2} & \cdots & a_{mn} \end{pmatrix} \begin{pmatrix}x_1 \\\\ x_2 \\\\ \vdots \\\\ x_n \end{pmatrix} \\\\
   &= \begin{pmatrix} \frac{\partial}{\partial x_1} \\\\ \frac{\partial}{\partial x_2} \\\\ \vdots \\\\ \frac{\partial}{\partial x_n} \end{pmatrix} \begin{pmatrix} a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n \\\\
   a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n \\\\
   \vdots \\\\
   a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n
   \end{pmatrix} \\\\
   &= \begin{pmatrix} a_{11} &  a_{12} & \cdots & a_{1n} \\\\
   a_{21} &  a_{22} & \cdots & a_{2n} \\\\
   \vdots \\\\
   a_{m1} &  a_{m2} & \cdots & a_{mn}
   \end{pmatrix} = \boldsymbol{A}
\end{align}
\\]
\\[
\begin{align}
    \frac{\partial \boldsymbol{x}^T \boldsymbol{A} }{\partial\boldsymbol{x}} &= \frac{\partial}{\partial \boldsymbol{x}} \begin{pmatrix} a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n \\\\
   a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n \\\\
   \vdots \\\\
   a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n
   \end{pmatrix} \\\\
   &= \begin{pmatrix} a_{11} &  a_{12} & \cdots & a_{1n} \\\\
   a_{21} &  a_{22} & \cdots & a_{2n} \\\\
   \vdots \\\\
   a_{m1} &  a_{m2} & \cdots & a_{mn}
   \end{pmatrix} = \boldsymbol{A}
\end{align}
\\]
\\[
\begin{align}
    \frac{\partial \boldsymbol{x}^T \boldsymbol{A} \boldsymbol{x} }{\partial\boldsymbol{x}} &= \boldsymbol{A} \boldsymbol{x} + \boldsymbol{x}^T \boldsymbol{A} \\\\
	&= \boldsymbol{A} \boldsymbol{x} + \boldsymbol{A}^T \boldsymbol{x} \\\\
	&= (\boldsymbol{A} + \boldsymbol{A}^T) \boldsymbol{x}
\end{align}
\\]
