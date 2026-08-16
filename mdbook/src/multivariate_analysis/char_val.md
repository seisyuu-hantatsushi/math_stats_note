## 特徴を表す量
いま,ある個体について,\\(k\\)種類（項目)の値が得られるとする.個体が\\(n\\)体として各データの組を
\\[
	x_{i,j} \\; i,j,n,k \in \mathbb{N}^+, i < n, j < k
\\]
として,個体\\(i\\)の\\(k\\)番目のデータとする.

\\[
	\boldsymbol{x}\_{i} = \begin{pmatrix} x_{i,1} \\\\  x_{i,2} \\\\ \vdots \\\\ x_{i,k} \end{pmatrix}
\\]

\\[
	\mathbf{X} = (x_{i,j}) = \begin{pmatrix} 
		\boldsymbol{x}\_{1}^{\mathsf{T}} \\\\
		\boldsymbol{x}\_{2}^{\mathsf{T}} \\\\
		\vdots \\\\
		\boldsymbol{x}\_{n}^{\mathsf{T}}
	\end{pmatrix}  = \begin{pmatrix}
		x_{1,1} & x_{1,2} & \cdots & x_{1,k} \\\\
		x_{2,1} & x_{2,2} & \cdots & x_{2,k} \\\\
		\vdots & \vdots & \ddots & \vdots \\\\ 
		x_{n,1} & x_{n,2} & \cdots & x_{n,k} \\\\
	\end{pmatrix}
\\]
と,まとめて表せるように定義する.
個体\\(i\\)の標本平均を
\\[
	\bar{x}\_{i,.} = \frac{1}{k}\sum^{k}\_{j=1} x\_{i,j}
\\]
種類\\(j\\)の標本平均を
\\[
	\bar{x}\_{.,j} = \frac{1}{n}\sum^{n}\_{i=1} x\_{i,j}
\\]
と表す.   
\\(l,m \in \mathbb{N}^+ \; l,m \leq k \\)として,観測値間に関係があるかを調べるには,標本の分散,共分散を取ればいい.
\\[
	s_{l,l} = \frac{1}{n} \sum^{n}\_{i=1} (x_{i,l}-\bar{x}\_{.,l})^2 \\\\
	s_{l,m} = \frac{1}{n} \sum^{n}\_{i=1} (x_{i,l}-\bar{x}\_{.,l})(x_{i,m}-\bar{x}\_{.,m})
\\]
これを,標本分散,標本共分散という.\\(s_{l,l}={s_{l}}^2\\)とも書く
\\[
	\mathbf{S} = (s_{l,m}) = \begin{pmatrix} 
		s_{1,1} & s_{1,2} & \cdots & s_{1,k} \\\\
		s_{2,1} & s_{2,2} & \cdots & s_{2,k} \\\\
		\vdots & \vdots & \ddots & \vdots \\\\ 
		s_{k,1} & s_{k,2} & \cdots & s_{k,k}
	\end{pmatrix}
\\]
として\\(\mathbf{S}\\)を**標本共分散行列**という.
\\[
	r_{l,m} = \frac{s_{l,m}}{\sqrt{s\_{l,l}}\sqrt{s\_{m,m}}}
\\]
として,標本相関係数という.\\(r_{l,l}=\frac{s_{l,l}}{\sqrt{s\_{l,l}}\sqrt{s\_{l,l}}}=1\\)である.
\\[
	\mathbf{R} = (r_{l,m}) = \begin{pmatrix} 
		1 & r_{1,2} & \cdots & r_{1,k} \\\\
		r_{2,1} & 1 & \cdots & r_{2,k} \\\\
		\vdots & \vdots & \ddots & \vdots \\\\ 
		r_{k,1} & r_{k,2} & \cdots & 1
	\end{pmatrix}
\\]
として\\(\mathbf{R}\\)を**標本相関係数行列**という.
