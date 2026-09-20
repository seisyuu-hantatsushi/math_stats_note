### 二元配置のモデル
因子が2つあるモデルを二元配置という.
### 二元配置
とある合金の製造で,温度と触媒の量で延性がどのように変わるかを知りたいとき,温度の水準を\\(A_i, i \leq I\\),触媒の水準を\\(B_j, j \leq J\\),繰り返し回数を\\(K\\)とする.
<table>
<tr>
	<th>因子\(A\)</th><th>因子\(B\)</th><th colspan="6">繰り返し</th>
</tr>
<tr>
	<th></th>
	<th></th>
	<th>1</th>
	<th>2</th>
	<th>\(\cdots\)</th>
	<th>\(j\)</th>
	<th>\(\cdots\)</th>
	<th>\(J\)</th>
</tr>
<tr>
    <th rowspan="6">\(A_1\)</th><th>\(B_1\)</th><td>\(y_{111}\)</td><td>\(y_{112}\)</td><td>\(\cdots\)</td><td>\(y_{11k}\)</td><td>\(\cdots\)</td><td>\(y_{11K}\)</td>
</tr>
<tr>
	<th>\(B_2\)</th><td>\(y_{121}\)</td><td>\(y_{122}\)</td><td>\(\cdots\)</td><td>\(y_{12k}\)</td><td>\(\cdots\)</td><td>\(y_{12K}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_j\)</th><td>\(y_{1j1}\)</td><td>\(y_{1j2}\)</td><td>\(\cdots\)</td><td>\(y_{1jk}\)</td><td>\(\cdots\)</td><td>\(y_{1jK}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_J\)</th><td>\(y_{1J1}\)</td><td>\(y_{1J2}\)</td><td>\(\cdots\)</td><td>\(y_{1Jk}\)</td><td>\(\cdots\)</td><td>\(y_{1JK}\)</td>
</tr>
<tr>
    <th rowspan="6">\(A_2\)</th><th>\(B_1\)</th><td>\(y_{211}\)</td><td>\(y_{212}\)</td><td>\(\cdots\)</td><td>\(y_{21k}\)</td><td>\(\cdots\)</td><td>\(y_{21K}\)</td>
</tr>
<tr>
	<th>\(B_2\)</th><td>\(y_{221}\)</td><td>\(y_{222}\)</td><td>\(\cdots\)</td><td>\(y_{22k}\)</td><td>\(\cdots\)</td><td>\(y_{22K}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_j\)</th><td>\(y_{2j1}\)</td><td>\(y_{2j2}\)</td><td>\(\cdots\)</td><td>\(y_{2jk}\)</td><td>\(\cdots\)</td><td>\(y_{2jK}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_J\)</th><td>\(y_{2J1}\)</td><td>\(y_{2J2}\)</td><td>\(\cdots\)</td><td>\(y_{2Jk}\)</td><td>\(\cdots\)</td><td>\(y_{2JK}\)</td>
</tr>
<tr>
    <th>\(\vdots\)</th><th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
    <th rowspan="6">\(A_i\)</th><th>\(B_1\)</th><td>\(y_{i11}\)</td><td>\(y_{i12}\)</td><td>\(\cdots\)</td><td>\(y_{i1k}\)</td><td>\(\cdots\)</td><td>\(y_{i1K}\)</td>
</tr>
<tr>
	<th>\(B_2\)</th><td>\(y_{i21}\)</td><td>\(y_{i22}\)</td><td>\(\cdots\)</td><td>\(y_{i2k}\)</td><td>\(\cdots\)</td><td>\(y_{i2K}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_j\)</th><td>\(y_{ij1}\)</td><td>\(y_{ij2}\)</td><td>\(\cdots\)</td><td>\(y_{ijk}\)</td><td>\(\cdots\)</td><td>\(y_{ijK}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_J\)</th><td>\(y_{iJ1}\)</td><td>\(y_{iJ2}\)</td><td>\(\cdots\)</td><td>\(y_{iJk}\)</td><td>\(\cdots\)</td><td>\(y_{iJK}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
    <th rowspan="6">\(A_I\)</th><th>\(B_1\)</th><td>\(y_{I11}\)</td><td>\(y_{I12}\)</td><td>\(\cdots\)</td><td>\(y_{I1k}\)</td><td>\(\cdots\)</td><td>\(y_{I1K}\)</td>
</tr>
<tr>
	<th>\(B_2\)</th><td>\(y_{I21}\)</td><td>\(y_{I22}\)</td><td>\(\cdots\)</td><td>\(y_{I2k}\)</td><td>\(\cdots\)</td><td>\(y_{I2K}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_j\)</th><td>\(y_{Ij1}\)</td><td>\(y_{Ij2}\)</td><td>\(\cdots\)</td><td>\(y_{Ijk}\)</td><td>\(\cdots\)</td><td>\(y_{IjK}\)</td>
</tr>
<tr>
	<th>\(\vdots\)</th><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\ddots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td><td>\(\vdots\)</td>
</tr>
<tr>
	<th>\(B_J\)</th><td>\(y_{IJ1}\)</td><td>\(y_{IJ2}\)</td><td>\(\cdots\)</td><td>\(y_{IJk}\)</td><td>\(\cdots\)</td><td>\(y_{IJK}\)</td>
</tr>
</table>

因子\(A\)と因子\(B\)には交互作用があるかもしれない.なので,交互作用を\\(A \times B\\)と表示する.

構造モデルは
\\[
	Y_{ijk} = \mu + \alpha_{i} + \beta\_{j} + (\alpha\beta)\_{ij} + E\_{ijk}, E\_{ijk} \sim \mathcal{N}(0, \sigma^2) \\\\
	\sum^{I}\_{i=1} \alpha_i = 0 \\\\
	\sum^{J}\_{j=1} \beta_j = 0 \\\\
	\sum^{I}\_{i=1} (\alpha\beta)\_{ij} = \sum^{J}\_{j=1} (\alpha\beta)\_{ij} = 0	
\\]
で,\\((\alpha\beta)\_{ij}\\)は交互作用の効果を表す.

各平方和は,
\\[
	SS_T = \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(Y_{ijk} - \bar{Y}_{...})^2
\\]

\\[
\\begin{align}
	SS_A &= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\bar{Y}\_{i..} - \bar{Y}\_{...})^2 \\\\
		&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\alpha_{i} + \bar{E}\_{i..} - \bar{E}\_{...})^2 \\\\
		&= JK\sum^{I}\_{i=1}(\alpha_{i} + \bar{E}\_{i..} - \bar{E}\_{...})^2
\end{align}
\\]

\\[
\\begin{align}
	SS_B &= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\bar{Y}\_{.j.} - \bar{Y}\_{...})^2 \\\\
		&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\beta_{j} + \bar{E}\_{.j.} - \bar{E}\_{...})^2 \\\\
		&= IK\sum^{J}\_{j=1}(\beta_{j} + \bar{E}\_{.j.} - \bar{E}\_{...})^2 \\\\
\end{align}
\\]

\\[
\\begin{align}
	SS_{A \times B} &= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\bar{Y}\_{ij.} - \bar{Y}\_{i..} - \bar{Y}\_{.j.} + \bar{Y}\_{...})^2 \\\\
		&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}((\alpha\beta)\_{ij} + \bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...})^2 \\\\
		&= K\sum^{I}\_{i=1}\sum^{J}\_{j=1}((\alpha\beta)\_{ij} + \bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...})^2
\end{align}
\\]

\\[
\\begin{align}
	SS_{E} &= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\bar{Y}\_{ijk} - \bar{Y}\_{ij.})^2 \\\\
		&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\mu + \alpha_{i} + \beta\_{j} + (\alpha\beta)\_{ij} + E\_{ijk} 
		- (\mu + \alpha_{i} + \beta_{j} +  (\alpha\beta)\_{ij} + \bar{E}\_{ij.}))^2 \\\\
		&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(E\_{ijk} - \bar{E}\_{ij.})^2
\end{align}
\\]

\\[
\\begin{align}
	SS_T &= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(Y\_{ijk} - \bar{Y}\_{ij.} + \bar{Y}\_{ij.} + \bar{Y}\_{i..} - \bar{Y}\_{i..} + \bar{Y}\_{.j.} - \bar{Y}\_{.j.} + \bar{Y}\_{...} - \bar{Y}\_{...} - \bar{Y}\_{...})^2 \\\\	
 &= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}((Y\_{i..} - Y\_{...}) + (Y\_{.j.} - Y\_{...}) + (\bar{Y}\_{ij.} - Y\_{i..} - Y\_{.j.} + \bar{Y}\_{...}) + (\bar{Y}\_{ijk} - \bar{Y}\_{ij.}))^2 \\\\
  &= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(Y\_{i..} - Y\_{...})^2 + 
  \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(Y\_{.j.} - Y\_{...})^2 + 
  \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\bar{Y}\_{ij.} - Y\_{i..} - Y\_{.j.} + \bar{Y}\_{...})^2 +
  \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\bar{Y}\_{ijk} - \bar{Y}\_{ij.})^2 \\\\
  &= SS_A+SS_B+SS_{A \times B} + SS_E
\\end{align}
\\]

それぞれの平均を取ると,
\\[
\\begin{align}
	\mathrm{E}[SS_A] &= \mathrm{E}[(\alpha_{i} + \bar{E}\_{i..} - \bar{E}\_{...})^2] \\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + JK\sum^{I}\_{i=1}\mathrm{E}[(\bar{E}\_{i..} - \bar{E}\_{...})^2] \\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + JK\sum^{I}\_{i=1}\mathrm{V}[\bar{E}\_{i..} - \bar{E}\_{...}] \\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + JK\sum^{I}\_{i=1}\\{\mathrm{V}[\bar{E}\_{i..}] + \mathrm{V}[\bar{E}\_{...}] - 2 \mathrm{Cov}(\bar{E}\_{i..}, \bar{E}\_{...})\\}\\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + JK\sum^{I}\_{i=1}\Bigl\\{\frac{\sigma^2}{JK} + \frac{\sigma^2}{IJK} - 2 \mathrm{Cov}\Bigl(\bar{E}\_{i..}, \frac{1}{I} \sum^{I}\_{k=1} \bar{E}\_{k..}\Bigr) \Bigr\\} \\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + JK\sum^{I}\_{i=1}\Bigl\\{\frac{\sigma^2}{JK} + \frac{\sigma^2}{IJK} - 2 \frac{1}{I} \mathrm{V}[\bar{E}\_{i..}] \Bigr\\}\\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + JK\sum^{I}\_{i=1}\Bigl\\{\frac{\sigma^2}{JK} + \frac{\sigma^2}{IJK} - 2 \frac{\sigma^2}{IJK}\Bigr\\}\\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + \sum^{I}\_{i=1}\Bigl(\sigma^2 + \frac{\sigma^2}{I} - 2 \frac{\sigma^2}{I}\Bigr)\\\\
	&= JK\sum^{I}\_{i=1}\alpha_{i}^2 + (I-1)\sigma^2
\end{align}
\\]

\\[
\\begin{align}
	\mathrm{E}[SS_B] &= \mathrm{E}[(\beta_{j} + \bar{E}\_{.j.} - \bar{E}\_{...})^2] \\\\
	&= IK\sum^{J}\_{i=1}\beta_{j}^2 + IK\sum^{J}\_{j=1}\mathrm{E}[(\bar{E}\_{.j.} - \bar{E}\_{...})^2] \\\\
	&= IK\sum^{J}\_{i=1}\beta_{j}^2 + IK\sum^{J}\_{j=1}\mathrm{V}[\bar{E}\_{.j.} - \bar{E}\_{...}] \\\\
	&= IK\sum^{J}\_{j=1}\beta_{j}^2 + IK\sum^{J}\_{j=1}\\{\mathrm{V}[\bar{E}\_{.j.}] + \mathrm{V}[\bar{E}\_{...}] - 2 \mathrm{Cov}(\bar{E}\_{.j.}, \bar{E}\_{...})\\}\\\\
	&= IK\sum^{J}\_{j=1}\beta_{j}^2 + IK\sum^{J}\_{j=1}\Bigl\\{\frac{\sigma^2}{IK} + \frac{\sigma^2}{IJK} - 2 \mathrm{Cov}\Bigl(\bar{E}\_{.j.}, \frac{1}{J} \sum^{J}\_{k=1} \bar{E}\_{.k.}\Bigr) \Bigr\\} \\\\
	&= IK\sum^{J}\_{j=1}\beta_{j}^2 + IK\sum^{J}\_{j=1}\Bigl\\{\frac{\sigma^2}{IK} + \frac{\sigma^2}{IJK} - 2 \frac{1}{I} \mathrm{V}[\bar{E}\_{.j.}] \Bigr\\}\\\\
	&= IK\sum^{J}\_{j=1}\beta_{j}^2 + IK\sum^{J}\_{j=1}\Bigl\\{\frac{\sigma^2}{IK} + \frac{\sigma^2}{IJK} - 2 \frac{\sigma^2}{IJK}\Bigr\\}\\\\
	&= IK\sum^{J}\_{j=1}\beta_{j}^2 + \sum^{J}\_{j=1}\Bigl(\sigma^2 + \frac{\sigma^2}{J} - 2 \frac{\sigma^2}{J}\Bigr)\\\\
	&= IK\sum^{J}\_{j=1}\beta_{j}^2 + (J-1)\sigma^2
\end{align}
\\]

\\[
\\begin{align}
	\mathrm{E}[SS_{A \times B}] &= \mathrm{E}[K\sum^{I}\_{i=1}\sum^{J}\_{j=1}((\alpha\beta)\_{ij} + \bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...})^2] \\\\
		&= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} \mathrm{E}[(\alpha\beta)\_{ij} + \bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...})^2] \\\\
		&= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} \mathrm{E}[{(\alpha\beta)\_{ij}}^2 + 2(\alpha\beta)\_{ij}(\bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...}) + (\bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...})^2] \\\\
		&= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + K\sum^{I}\_{i=1}\sum^{J}\_{j=1} \mathrm{E}[(\bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...})^2] \\\\
		&= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + K\sum^{I}\_{i=1}\sum^{J}\_{j=1} \mathrm{V}[\bar{E}\_{ij.} - \bar{E}\_{i..} - \bar{E}\_{.j.} + \bar{E}\_{...}] \\\\
		&= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + 
			K\sum^{I}\_{i=1}\sum^{J}\_{j=1} \\{ \mathrm{V}[\bar{E}\_{ij.}] + 
			    \mathrm{V}[\bar{E}\_{i..}] + \mathrm{V}[\bar{E}\_{.j.}] + \mathrm{V}[\bar{E}\_{...}]
				- 2 \mathrm{Cov}[\bar{E}\_{ij.},\bar{E}\_{i..}] - 2 \mathrm{Cov}[\bar{E}\_{ij.},\bar{E}\_{.j.}] + 2 \mathrm{Cov}[\bar{E}\_{ij.},\bar{E}\_{...}]
				+ 2 \mathrm{Cov}[\bar{E}\_{i..},\bar{E}\_{.j.}] - 2 \mathrm{Cov}[\bar{E}\_{i..},\bar{E}\_{...}] 
				- 2 \mathrm{Cov}[\bar{E}\_{.j.},\bar{E}\_{...}]  \\} \\\\
	   &= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + 
			K\sum^{I}\_{i=1}\sum^{J}\_{j=1} \\{ \frac{\sigma^2}{K} + \frac{\sigma^2}{JK} + \frac{\sigma^2}{IK} + \frac{\sigma^2}{IJK}
				- 2 \frac{1}{J}\frac{\sigma^2}{K} - 2 \frac{1}{I}\frac{\sigma^2}{K} + 2 \frac{1}{IJ}\frac{\sigma^2}{K} + 2 \frac{1}{IJ}\frac{\sigma^2}{K} - 2 \frac{1}{I} \frac{\sigma^2}{JK} 
				- 2 \frac{1}{IK}\frac{\sigma^2}{J} \\} \\\\
	   &= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + (IJ+I+J+1-2I-2J+2+2-2-2)\sigma^2 \\\\
	   &= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + (IJ+1-I-J)\sigma^2 \\\\
	   &= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + (I(J-1)-(J-1))\sigma^2 \\\\
	   &= K\sum^{I}\_{i=1}\sum^{J}\_{j=1} {(\alpha\beta)\_{ij}}^2 + (I-1)(J-1)\sigma^2 \\\\
\end{align}
\\]

\\[
\begin{align}
	\mathrm{E}[SS\_{E}] &= \mathrm{E}[\sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(E\_{ijk} - \bar{E}\_{ij.})^2] \\\\
	&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}\mathrm{E}[(E\_{ijk} - \bar{E}\_{ij.})^2] \\\\
	&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}\mathrm{V}[E\_{ijk} - \bar{E}\_{ij.}] \\\\
	&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\mathrm{V}[E\_{ijk}] + \mathrm{V}[\bar{E}\_{ij.}] - 2\mathrm{Cov}[E\_{ijk}, \bar{E}\_{ij.}])\\\\
	&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\sigma^2 + \frac{\sigma^2}{K} - 2\frac{1}{K}\sigma^2) \\\\
	&= \sum^{I}\_{i=1}\sum^{J}\_{j=1}\sum^{K}\_{k=1}(\sigma^2 - \frac{\sigma^2}{K}) \\\\
	&= IJK\sigma^2 - IJ\sigma^2 \\\\
	&= IJ(K-1)\sigma^2
\end{align}
\\]

これまでと同様に,各因子の効果がない場合と考え,各平均平方和は,
\\[
MS_A = \frac{SS_A}{I-1} \\\\
MS_B = \frac{SS_B}{J-1} \\\\
MS_{A \times B} = \frac{SS_{A \times B}}{(I-1)(J-1)} \\\\
MS\_{E} = \frac{SS_E}{IJ(K-1)}
\\]
で,
\\[
	\frac{(I-1)MS_A}{\sigma^2} \sim \chi^2_{I-1} \\\\
	\frac{(J-1)MS_B}{\sigma^2} \sim \chi^2_{J-1} \\\\
	\frac{(I-1)(J-1)MS_{A \times B}}{\sigma^2} \sim \chi^2_{(I-1)(J-1)} \\\\
	\frac{IJ(K-1)MS\_{E}}{\sigma^2} \sim \chi^2_{IJ(K-1)}
\\]
なので,検定統計量は,
\\[
	\frac{MS_A}{MS_E} \sim F_{I-1,IJ(K-1)}\\\\
	\frac{MS_B}{MS_E} \sim F_{J-1,IJ(K-1)}\\\\
	\frac{MS_{A \times B}}{MS_E} \sim F_{(I-1)(J-1),IJ(K-1)}\\\\
\\]
