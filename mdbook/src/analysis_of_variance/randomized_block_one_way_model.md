### 一元配置乱塊法のモデル
何らかの理由で,時間的に繰り返しが制限がある中で,効果を効率的に確かめたい.
例えば,農作物の栽培で肥料の種類の効果を調べたいが,一年に一回しか取れない,個体の区別が難しいや,
陶器の試薬の効果を調べたいが,炉が一つしか無いなどである.
#### 一元配置乱塊法
とある農作物を栽培したエリアを\\(R_j, j \leq J\\)とし,肥料の量を因子として\\(A_i, i \leq I\\)とする. 観測値は\\(y_{ij}\\)とする.
<table>
<tr>
	<th></th><th colspan="6">ブロック</th>
</tr>
<tr>
	<th></th>
	<th></th>
	<th>\(R_1\)</th>
	<th>\(R_2\)</th>
	<th>\(\cdots\)</th>
	<th>\(R_j\)</th>
	<th>\(\cdots\)</th>
	<th>\(R_J\)</th>
</tr>
<tr>
    <th rowspan="6">因子\(A\)</th><th>\(A_1\)</th><td>\(y_{11}\)</td><td>\(y_{12}\)</td><td>\(\cdots\)</td><td>\(y_{1j}\)</td><td>\(\cdots\)</td><td>\(y_{1J}\)</td>
</tr>
<tr>
	<th>\(A_2\)</th><td>\(y_{21}\)</td><td>\(y_{22}\)</td><td>\(\cdots\)</td><td>\(y_{2j}\)</td><td>\(\cdots\)</td><td>\(y_{2J}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td></td><td>\(\vdots\)</td><td></td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(A_i\)</th><td>\(y_{i1}\)</td><td>\(y_{i2}\)</td><td>\(\cdots\)</td><td>\(y_{ij}\)</td><td>\(\cdots\)</td><td>\(y_{iJ}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td></td><td>\(\vdots\)</td><td></td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(A_{I}\)</th><td>\(y_{I 1}\)</td><td>\(y_{I 2}\)</td><td>\(\cdots\)</td><td>\(y_{I j}\)</td><td>\(\cdots\)</td><td>\(y_{I J}\)</td>
</tr>
</table>

構造モデルは
\\[
	Y_{ij} = \mu + \alpha_i + \rho_j + E_{ij}, E_{ij} \sim \mathcal{N}(0,\sigma^2) \\\\
	\sum^{I}\_{i=1} \alpha_i = 0 \\\\
	\sum^{J}\_{j=1} \rho_j = 0
\\]

とする.
もし,\\(\sum^{I}\_{i=1} \alpha_i = 0, \sum^{J}\_{j=1} \rho_j = 0\\)としない場合,
\\(\sum^{I}\_{i=1} \alpha_i = \alpha, \sum^{J}\_{j=1} \rho_j = \rho\\)として,
\\[
	\frac{1}{I} \sum^{I}\_{i=1} (\mu + \alpha_i + \rho_j + E\_{ij}) = \mu + \alpha + \rho\_j + \frac{1}{I} \sum^{I}\_{i=1} E\_{ij} \\\\
	\frac{1}{J} \sum^{J}\_{j=1} (\mu + \alpha_i + \rho_j + E\_{ij}) = \mu + \alpha\_i + \rho + \frac{1}{J} \sum^{J}\_{j=1} E\_{ij} \\\\
	\frac{1}{IJ} \sum^{I}\_{i=1} \sum^{J}\_{j=1} (\mu + \alpha\_i + \rho\_j + E\_{ij}) = \mu + \alpha + \rho + \frac{1}{IJ} \sum^{J}\_{j=1} E_{ij}\\\\
\\]
となり,\\(\mu,\alpha,\rho\\)は分離できない.

\\[
	\bar{Y}\_{i.} = \sum^{J}\_{j=1} (\mu + \alpha\_i + \rho\_j + E\_{ij}) = \mu + \alpha\_i + \bar{E}\_{i.} \\\\
	\bar{Y}\_{.j} = \frac{1}{I} \sum^{I}\_{i=1} (\mu + \alpha\_i + \rho\_j + E\_{ij}) = \mu + \rho\_j + \bar{E}\_{.j} \\\\
	\bar{Y}\_{..} = \frac{1}{IJ} \sum^{J}\_{j=1} (\mu + \alpha\_i + \rho\_j + E\_{ij}) = \mu + \bar{E}_{..}
\\]

総平方和は
\\[
	SS_T = \sum^{I}\_{i=1}\sum^{J}\_{j=1} (Y_{ij} - \bar{Y}\_{..})^2 
\\]

因子\\(A\\)の平方和は,
\\[
\begin{align}
	SS_A &= \sum^{I}\_{i=1}\sum^{J}\_{j=1} (Y\_{i.} - \bar{Y}\_{..})^2 \\\\ 
	     &= J\sum^{I}\_{i=1} (\alpha_i + \bar{E}\_{i.} - \bar{E}\_{..})^2
\end{align}
\\]

ブロック要因の平方和は,
\\[
\begin{align}
	SS_R &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{.j} - \bar{Y}\_{..})^2 \\\\ 
	     &= I \sum^{J}\_{j=1} (\rho_j + \bar{E}\_{.j} - \bar{E}\_{..})^2
\end{align}
\\]

誤差平方和は
\\[
\begin{align}
	SS_E &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}_{..})^2 \\\\ 
	     &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \\{\mu + \alpha_i + \rho_j + E\_{ij} - (\mu + \alpha\_i + \bar{E}\_{i.}) - (\mu + \rho\_j + \bar{E}\_{.j}) + (\mu + \bar{E}\_{..})\\}^2 \\\\
		 &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (E\_{ij} - \bar{E}\_{i.} - \bar{E}\_{.j} + \bar{E}\_{..})^2
\end{align}
\\]

\\[
\begin{align}
	SS_T &= \sum^{I}\_{i=1}\sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.} + \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{.j} - \bar{Y}\_{..} + \bar{Y}\_{..} - \bar{Y}\_{..})^2 \\\\
	&=  \sum^{I}\_{i=1}\sum^{J}\_{j=1} ((Y\_{i.} - \bar{Y}\_{..}) + (Y\_{.j} - \bar{Y}\_{..}) + (Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..}))^2 \\\\
	&= \\sum^{I}\_{i=1}\sum^{J}\_{j=1}\\{(Y\_{i.} - \bar{Y}\_{..})^2 + (Y\_{.j} - \bar{Y}\_{..})^2 + (Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..})^2
		+2(Y\_{i.} - \bar{Y}\_{..})(Y\_{.j} - \bar{Y}\_{..}) + 2 (Y\_{.j} - \bar{Y}\_{..})(Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..}) + 2 (Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..})(Y\_{i.} - \bar{Y}\_{..})\\}\\\\
	&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}(Y\_{i.} - \bar{Y}\_{..})^2 + \sum^{I}\_{i=1}\sum^{J}\_{j=1}(Y\_{.j} - \bar{Y}\_{..})^2 + \sum^{I}\_{i=1}\sum^{J}\_{j=1}(Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..}))^2 + \sum^{I}\_{i=1}\sum^{J}\_{j=1}2(Y\_{i.} - \bar{Y}\_{..})(Y\_{.j} - \bar{Y}\_{..}) + \sum^{I}\_{i=1}\sum^{J}\_{j=1} 2 (Y\_{.j} - \bar{Y}\_{..})(Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..}) + \sum^{I}\_{i=1}\sum^{J}\_{j=1}2(Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..})(Y\_{i.} - \bar{Y}\_{..})\\\\
	&= J \sum^{I}\_{i=1}(Y\_{i.} - \bar{Y}\_{..})^2 + I\sum^{J}\_{j=1}(Y\_{.j} - \bar{Y}\_{..})^2 + \sum^{I}\_{i=1}\sum^{J}\_{j=1}(Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{.j} + \bar{Y}\_{..}))^2 \\\\
	&= SS_A + SS_R + SS_E
\end{align}
\\]
と,総平方和は分解できる.

\\[
\begin{align}
	\mathrm{E}[SS_A] &= \mathrm{E}[J\sum^{I}\_{i=1} (\alpha_i + \bar{E}\_{i.} - \bar{E}\_{..})^2] \\\\
	&= J\sum^{I}\_{i=1} \mathrm{E}[(\alpha_i + \bar{E}\_{i.} - \bar{E}\_{..})^2] \\\\
	&= J\sum^{I}\_{i=1} \mathrm{E}[(\alpha_i^2 + 2\alpha_i(\bar{E}\_{i.} - \bar{E}\_{..}) + (\bar{E}\_{i.} - \bar{E}\_{..})^2] \\\\
	&= J\sum^{I}\_{i=1} \alpha_i^2 + J\sum^{I}\_{i=1} 2\alpha_i \mathrm{E}[(\bar{E}\_{i.} - \bar{E}\_{..})] + J\sum^{I}\_{i=1} \mathrm{E}[(\bar{E}\_{i.} - \bar{E}\_{..})^2] \\\\
	&= J\sum^{I}\_{i=1} \alpha_i^2 + J\sum^{I}\_{i=1} \mathrm{E}[(\bar{E}\_{i.} - \bar{E}\_{..})^2] \\\\
	&= J\sum^{I}\_{i=1} \alpha_i^2 + J\sum^{I}\_{i=1} \mathrm{V}[\bar{E}\_{i.} - \bar{E}\_{..}] \\\\
	&= J\sum^{I}\_{i=1} \alpha_i^2 + J\sum^{I}\_{i=1} \\{\mathrm{V}[\bar{E}\_{i.}] -2\mathrm{Cov}(\bar{E}\_{i.}, \bar{E}\_{..}) + \mathrm{V}[\bar{E}\_{..}] \\}\\\\
\end{align}
\\]

\\[
\begin{align}
\mathrm{Cov}(\bar{E}\_{i.}, \bar{E}\_{..}) &= \mathrm{Cov}(\bar{E}\_{i.}, \frac{1}{I}\sum^{I}\_{k=1}\bar{E}\_{k.}) \\\\
&= \frac{1}{I} \sum^{I}\_{k=1} \mathrm{Cov}(\bar{E}\_{i.}, \bar{E}\_{k.}) \\\\
&= \frac{1}{I} \mathrm{V}[\bar{E}\_{i.}] \\\\
&= \frac{\sigma^2}{IJ} \\\\
\end{align}
\\]

\\[
\begin{align}
	\mathrm{E}[SS\_A] &= J\sum^{I}\_{i=1} \alpha_i^2 + J\sum^{I}\_{i=1} (\frac{\sigma^2}{J} - 2 \frac{\sigma^2}{IJ} + \frac{\sigma^2}{IJ}) \\\\
	&= J\sum^{I}\_{i=1} \alpha_i^2 + (I-1)\sigma^2
\end{align}
\\]

\\[
\begin{align}
	\mathrm{E}[SS_R] &= \mathrm{E}[I \sum^{J}\_{j=1} (\rho_j + \bar{E}\_{.j} - \bar{E}\_{..})^2] \\\\
	&= I \sum^{J}\_{j=1} \rho_j^2 +  I \sum^{J}\_{j=1}\mathrm{E}[(\bar{E}\_{.j} - \bar{E}\_{..})^2] \\\\
	&= I \sum^{J}\_{j=1} \rho_j^2 +  I \sum^{J}\_{j=1}\mathrm{V}[\bar{E}\_{.j} - \bar{E}\_{..}] \\\\
	&= I \sum^{J}\_{j=1} \rho_j^2 +  I \sum^{J}\_{j=1}\\{\mathrm{V}[\bar{E}\_{.j}] - 2\mathrm{Cov}(\bar{E}\_{.j},\bar{E}\_{..}) + \mathrm{V}[\bar{E}\_{..}]\\} \\\\
	&= I \sum^{J}\_{j=1} \rho_j^2 +  I \sum^{J}\_{j=1}(\frac{\sigma^2}{I} + \frac{\sigma^2}{IJ} - \frac{2\sigma^2}{IJ}) \\\\
	&= I \sum^{J}\_{j=1} \rho_j^2 +  (J-1)\sigma^2 \\\\
\end{align}
\\]	

\\[
\begin{align}
\mathrm{E}[SS_E] &= \mathrm{E}[\sum^{I}\_{i=1} \sum^{J}\_{j=1} (E\_{ij} - \bar{E}\_{i.} - \bar{E}\_{.j} + \bar{E}\_{..})^2] \\\\
&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \mathrm{V}[E\_{ij} - \bar{E}\_{i.} - \bar{E}\_{.j} + \bar{E}\_{..}]\\\\
&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \\{ \mathrm{V}[E\_{ij}] + \mathrm{V}[\bar{E}\_{i.}] + \mathrm{V}[\bar{E}\_{.j}] + \mathrm{V}[\bar{E}\_{..}]
	- 2\mathrm{Cov}(E\_{ij}, \bar{E}\_{i.}) - 2 \mathrm{Cov}(E\_{ij}, \bar{E}\_{.j}) + 2 \mathrm{Cov}(E\_{ij}, \bar{E}\_{..})
	+ 2 \mathrm{Cov}(\bar{E}\_{i.}, \bar{E}\_{.j}) - 2 \mathrm{Cov}(\bar{E}\_{i.}, \bar{E}\_{..}) - 2 \mathrm{Cov}(\bar{E}\_{.j}, \bar{E}\_{..}) \\\\
&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} ( \sigma^2 + \frac{\sigma^2}{J} + \frac{\sigma^2}{I} + \frac{\sigma^2}{IJ}
	- 2\frac{\sigma^2}{J} - 2 \frac{\sigma^2}{I} + 2 \frac{\sigma^2}{IJ} + 2 \frac{\sigma^2}{IJ} - 2 \frac{\sigma^2}{IJ} - 2 \frac{\sigma^2}{IJ}) \\\\
	&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} ( \sigma^2 - \frac{\sigma^2}{J} - \frac{\sigma^2}{I} + \frac{\sigma^2}{IJ}) \\\\
	&= \sum^{I}\_{i=1} ( J\sigma^2 -  \sigma^2 - \frac{J\sigma^2}{I} + \frac{\sigma^2}{I}) \\\\
	&= IJ\sigma^2 -  I\sigma^2 - J\sigma^2 + \sigma^2 \\\\
	&= (IJ -  I - J + 1)\sigma^2 \\\\
	&= (I(J -1) - (J - 1))\sigma^2 \\\\
	&= (I-1)(J-1)\sigma^2 \\\\
\end{align}
\\]
より,
\\(\frac{SS_E}{(I-1)(J-1)}\\)が\\(\sigma^2\\)の不偏推定量.

\\[
	MS_E = \frac{SS_E}{(I-1)(J-1)}
\\]
として, 平均誤差平方和とする.

各水準に効果があるかを確認するために,検定を行う.仮説は,
\\[
	H_0:全てのiに対して\alpha_i=0 \\; \mathrm{vs} \\; H_1:いずれかのiに対して\alpha_i\not=0
\\]
\\(H_0\\)のとき,
\\[
\mathrm{E}[SS\_A] = (I-1)\sigma^2
\\]
なので,検定統計量は,
\\[
	MS_A = \frac{SS\_A}{I-1} \\\\
\\]
として,
\\[
	\frac{MS_A}{MS_E} \sim F_{I-1,(I-1)(J-1)}
\\]

また,ブロックが何らかの影響を与えているか確認するには,
\\[
	H_0:全てのiに対して\rho_j=0 \\; \mathrm{vs} \\; H_1:いずれかのiに対して\rho_j\not=0
\\]
\\(H_0\\)のとき,
\\[
\mathrm{E}[SS\_R] = (J-1)\sigma^2
\\]
なので,
\\[
	MS_R = \frac{SS\_R}{J-1} \\\\
\\]
として,
\\[
	\frac{MS_R}{MS_E} \sim F_{J-1,(I-1)(J-1)}
\\]
なので,検定統計量としてつかう.
分散分析表は,
<table>
<tr>
	<th>変動因子</th><th>自由度</th><th>平方和</th><th>平均平方和</th><th>F値</th>
</tr>
<tr>
	<th>因子\(A\)</th><td>\(I-1\)</td><td>\(SS_A\)</td><td>\(MS_A=\frac{1}{I-1}SS_A\)</td><td>\(MS_A/MS_E\)</td>
</tr>
<tr>
	<th>因子\(R\)</th><td>\(J-1\)</td><td>\(SS_R\)</td><td>\(MS_R=\frac{1}{I-1}SS_R\)</td><td>\(MS_R/MS_E\)</td>
</tr>
<tr>
	<th>誤差\(E\)</th><td>\((I-1)(J-1)\)</td><td>\(SS_E\)</td><td>\(MS_E=\frac{1}{(I-1)(J-1)}SS_E\)</td>
</tr>
<tr>
	<th>全体</th><td>\(J-1\)</td><td>\(SS_T\)</td>
</tr>
</table>

#### 交互作用を考えてみる.
とある農作物を栽培したエリアを\\(R_j, j \leq J\\)とし,肥料の量を因子として\\(A_i, i \leq I\\)として,もしかしたら,エリアと肥料が交互に作用しているかもしれない.
その時のモデルを考える.  
交互作用の因子を\\((A \times R)_{ij}\\)と表現する. 構造モデルは,

\\[
	Y\_{ij} = \mu + \alpha_i + \rho_j + (\alpha\rho)\_{ij} + E\_{ij}, E\_{ij} \sim \mathcal{N}(0,\sigma^2) \\\\
	\sum^{I}\_{i=1} \alpha_i = 0 \\\\
	\sum^{J}\_{j=1} \rho_j = 0 \\\\
	\sum^{I}\_{i=1} (\alpha\rho)\_{ij} = \sum^{J}\_{j=1} (\alpha\rho)\_{ij} = 0
\\]

各平方和は,
\\[
	SS_T = \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{..})^2
\\]

\\[
\begin{align}
	SS_A &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (\bar{Y}\_{i.} - \bar{Y}\_{..})^2 \\\\
	&= J \sum^{I}\_{i=1} (\alpha\_i + \bar{E}\_{i.} - \bar{E}\_{..})^2 \\\\
\end{align}
\\]

\\[
\begin{align}
	SS_R &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{.j} - \bar{Y}\_{..})^2 \\\\ 
	     &= I \sum^{J}\_{j=1} (\rho_j + \bar{E}\_{.j} - \bar{E}\_{..})^2
\end{align}
\\]	

\\[
\begin{align}
	SS_{A \times R} &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{j.} + \bar{Y}\_{..})^2 \\\\ 
	     &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} ( \mu + \alpha_i + \rho_j + (\alpha\rho)\_{ij} + E\_{ij} - (\mu + \alpha_i + \bar{E}\_{i.}) - (\mu + \rho_j  + \bar{E}\_{.j}) + (\mu + \bar{E}\_{..}))^2 \\\\
		 &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} ( (\alpha\rho)\_{ij} + E\_{ij} - \bar{E}\_{i.} - \bar{E}\_{.j} + \bar{E}\_{..} )^2 
\end{align}
\\]

\\[
\begin{align}
	SS_E &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.} - \bar{Y}\_{j.} + \bar{Y}\_{..})^2 \\\\ 
	     &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} ( \mu + \alpha_i + \rho_j + (\alpha\rho)\_{ij} + E\_{ij} - (\mu + \alpha_i + \bar{E}\_{i.}) - (\mu + \rho_j  + \bar{E}\_{.j}) + (\mu + \bar{E}\_{..}))^2 \\\\
		 &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} ( (\alpha\rho)\_{ij} + E\_{ij} - \bar{E}\_{i.} - \bar{E}\_{.j} + \bar{E}\_{..} )^2 
\end{align}
\\]	
となり,一元配置乱塊法ではブロックと因子の交互作用は実験誤差と分離ができない.
