### マルコフ過程
とある確率変数の確率が,現在（直前の過去)の確率変数にのみ依存する確率過程を**マルコフ過程**という.
\\[
	\mathrm{P}(...,X_{t-2},X_{t-1},X_t,X_{t+1}=x,X_{t+2},...) = \mathrm{P}(X_{t+1} = x | X_t)
\\]

#### マルコフ連鎖
\\(X_t\\)が\\( i,j,n \in \mathbb{N}^+, i,j \leq n \\)として,\\(X_t \in S=\\{x| x \in i\\}\\)とする.
\\(X_t\\)が取りうる値を**状態**といい.\\(S\\)は状態の集合である.

\\[
	\mathrm{P}(X\_{s+t} = j | X\_s = i) = p\_{ij}(t) \\;\\; s \in T
\\]

と確率を定義したとき,\\(X\_t = i\\)のとき,\\(X\_{s+t} = j\\)が発生する確率を行列で表したものを**推移確率行列**という.
\\[
	\mathbf{P}(t) = (p_{ij}(t)) = \begin{pmatrix} 
		p_{11}(t) & p_{12}(t) & \cdots & p_{1n}(t) \\\\
		p_{21}(t) & p_{22}(t) & \cdots & p_{2n}(t) \\\\
		\vdots & \vdots & \ddots & \vdots \\\\
		p_{n1}(t) & p_{n2}(t) & \cdots & p_{nn}(t) \\\\
	\end{pmatrix}, \sum^{n}\_{j=1} p\_{ij}(t) = 1 
\\]
推移確率行列は時刻\\(s\\)から時間\\(t\\)経過したとき,状態\\(i\\)が,状態\\(j\\)に移る確率の表である.

更に,経過時間が一定なら\\(X\_t = i\\)のとき,\\(X\_{t+1} = j\\)として,
\\[
	\mathrm{P}(X\_{t+1} = j | X\_t = i) = p\_{ij}
\\]

と書き,
\\[
	\mathbf{P} = (p_{ij}) = \begin{pmatrix} 
		p_{11} & p_{12} & \cdots & p_{1n} \\\\
		p_{21} & p_{22} & \cdots & p_{2n} \\\\
		\vdots & \vdots & \ddots & \vdots \\\\
		p_{n1} & p_{n2} & \cdots & p_{nn} \\\\
	\end{pmatrix} , \sum^{n}\_{j=1} p\_{ij} = 1 
\\]

\\(\mathrm{P}(X_t=i)=p^{(t)}_i\\)として,時刻\\(t\\)に状態\\(i\\)である確率であることを示す.
これを,状態について並べたベクトルを状態確率ベクトルという.
\\[
	\boldsymbol{\pi}_t = \begin{pmatrix} p^{(t)}_0 \\\\ p^{(t)}_1 \\\\ \vdots \\\\ p^{(t)}_n \end{pmatrix}, \sum^n\_{i=1} p^{(t)}_i = 1 
\\]
\\(\boldsymbol{\pi}_0\\)として,**初期状態確率ベクトル**という.時刻\\(t=0\\)の時点で,状態\\(i\\)であった場合,   
\\(\boldsymbol{\pi}_0 = (0,0,...,\underbrace{1}\_{i-th},0,...,0)^{\mathsf{T}}\\)と\\(i\\)番目の要素が1になる.
また,状態\\(i\\)であることを示すベクトルを\\(\boldsymbol{e}_i = (0,0,...,\underbrace{1}\_{i-th},0,...,0)^{\mathsf{T}} \\)と書く.

これらの記法を使うと,状態\\(i\\)が次の時刻でどの状態になっているかの確率を求めることができる.
\\[
	\boldsymbol{e}\_i^{\mathsf{T}} \mathbf{P} =  (p\_{i1},p\_{i2},...,p\_{in})^{\mathsf{T}}
\\]
更に,状態\\(i\\)が次の時刻に状態\\(j\\)となっている確率は,
\\[
	\boldsymbol{e}\_i^{\mathsf{T}} \mathbf{P} \boldsymbol{e}\_j = p\_{ij} = \mathrm{P}(X\_{t+1} = j | X\_t = i)
\\]

一定の経過時間をステップと言ううことにするとsステップ後に状態\\(i\\)が状態\\(j\\)がなっている確率は,
\\[
\begin{align}
	\boldsymbol{e}\_i^{\mathsf{T}} \mathbf{P}^s \boldsymbol{e}\_j &= \mathrm{P}(X\_{t+s} = j | X\_t=i) \\\\
	&= \sum^n\_{k\_{s-1}=1}\mathrm{P}(X\_{t+s} = j| X \_{t+s-1}=k_{s-1})\mathrm{P}(X\_{t+s-1}=k_{s-1}|X\_t=i) \\\\
	&= \sum^n\_{k\_{s-1},k\_{s-2},...,k\_{1}=1}\mathrm{P}(X\_{t+s} = j| X \_{t+s-1}=k_{s-1})\mathrm{P}(X\_{t+s-1}=k_{s-1}|X\_{t+s-2}=k\_{s-2})\cdots\mathrm{P}(X\_{t+2}=k_{2} | X\_{t+1}=k_{1})\mathrm{P}(X\_{t+1}=k_{1} | X\_{t}=i)
	\end{align}
\\]

となる.

#### 定常状態
