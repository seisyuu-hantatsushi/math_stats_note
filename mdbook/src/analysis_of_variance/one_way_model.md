### 一元配置のモデル
因子が1つのモデルを一元配置という.因子の水準に対し,一つ,一つ個別に値を取る.もしくは,とある条件にて繰り返しをまとめる.のモデルがある.
#### 一元配置
とある陶器の焼結で,とある釉薬の量を変化させて,発色に変化をみる.その因子を\\(A\\)として,釉薬の量に対して\\(A_i, i \leq I\\)とラベルをつける.
<table>
<tr>
	<th></th><th colspan="6">繰り返し</th>
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
   
上図のようにデータがまとめられたとする.  
各因子の水準が同じデータの母平均を\\(\mu_{A_i}\\)として,観測値\\(y_{ij}\\)は以下の様な確率変数のモデルの実現値とする.
\\[
Y\_{ij} = \mu\_{A_i} + E\_{ij} \\; \mu\_{A_i} = \mathrm{E}[\bar{Y}\_{i.}], \bar{Y}\_{i.}=\frac{1}{J}\sum^J_{j=1}Y\_{ij}, E\_{ij} \mathrm{.i.i.d} \sim \mathcal{N}(0, \sigma^2)
\\]
\\(E_{ij}\\)は観測誤差,実験誤差である.\\(Y_{ij} \sim \mathcal{N}(\mu_{A_i}, \sigma^2)\\). もし,要因の水準\\(A_i\\)に効果があるとすれば,全データの平均を\\(\mu\\)とすると,
\\[
\alpha_i = \mu\_{A_i}-\mu, \\; \mu = \mathrm{E}[\bar{Y}\_{..}], \bar{Y}\_{..} = \frac{1}{IJ}\sum^{I}\_{i=1}\sum^{J}\_{j=1} Y\_{ij}
\\]
としたときに,いずれかの\\(i\\)に対して\\(\alpha_i \not= 0\\)である.
改めて,
\\[
Y_{ij} = \mu + \alpha_i + E_{ij}
\\]

\\[
	\sum^{N\_{A}}\_{i=1}\alpha_i = \sum^{N\_{A}}\_{i=1} \mu_{A_i} - N\_{A} \mu \\\\
	\mu = \frac{1}{N\_{A}}\Bigr\\{\sum^{N\_{A}}\_{i=1} \mu_{A_i} - \sum^{N\_{A}}\_{i=1}\alpha_i \Bigl\\}
\\]
ここで,
\\[
\mu = \mathrm{E}\Bigr[\frac{1}{IJ}\sum^{I}\_{i=1}\sum^{J}\_{j=1} Y\_{ij}\Bigl] = \frac{1}{I} \sum^{I}\_{i=1}\mathrm{E}\Bigr[\frac{1}{J}\sum_{j=1} Y\_{ij}  \Bigl] =  \frac{1}{I} \sum^{I}\_{i=1} \mu_{A_i}
\\]
なので,
\\[
	\sum^{N\_{A}}\_{i=1}\alpha_i = 0
\\]
となる.
各水準に効果があるかを確認するために,検定を行う.仮説は,
\\[
	H_0:全てのiに対して\alpha_i=0 \\; \mathrm{vs} \\; H_1:いずれかのiに対して\alpha_i\not=0
\\]

帰無仮説が正しいなら,実験誤差と因子の水準でのばらつきは区別がつかない.\\({\sigma_{A_i}}^2/\sigma^2 = 1\\)である.
ということで,実験誤差の分散と因子の水準の分散を比較する.
\\[
	\begin{align}
	\bar{Y}\_{i.} &= \frac{1}{J} \sum^{J}\_{j=1} Y\_{ij} \\\\
	              &= \frac{1}{J} \sum^{J}\_{j=1} \Bigl\\{ \mu + \alpha_i + E\_{ij} \Bigr\\} \\\\
				  &= \mu + \alpha_i + \frac{1}{J} \sum^{J}\_{j=1} E\_{ij} \\\\
				  &= \mu + \alpha_i + \bar{E}\_{i.} \sim \mathcal{N}\Bigr(\mu\_{A_i}, \frac{\sigma^2}{J}\Bigl) = \mathcal{N}\Bigr(\mu+\alpha_i, \frac{\sigma^2}{J}\Bigl) \\\\
	\bar{Y}\_{..} &= \frac{1}{I} \sum^{I}\_{i=1} \frac{1}{J} \sum^{J}\_{j=1} Y\_{ij} \\\\
	              &= \frac{1}{I} \sum^{I}\_{i=1} \bar{Y}\_{i.} \\\\
  	              &= \frac{1}{I} \sum^{I}\_{i=1} \Bigl\\{\mu + \alpha_i + \bar{E}\_{i.}\Bigr\\} \\\\
   	              &= \mu + \frac{1}{I J} \sum^{I}\_{i=1} \sum^{J}\_{j=1}E\_{ij} \\\\
   	              &= \mu + \bar{E}\_{..} \sim \mathcal{N}\Bigr(\mu, \frac{\sigma^2}{N_{A}J}\Bigl)
	\end{align}
\\]

つまり,
\\[
	\mathrm{E}[\bar{Y}\_{i.} - \bar{Y}\_{..}] = \mathrm{E}[\bar{Y}\_{i.}] - \mathrm{E}[\bar{Y}\_{..}] = \alpha_i \\\\
	\mathrm{V}[\bar{Y}\_{i.} - \bar{Y}\_{..}] = \mathrm{V}[\bar{Y}\_{i.}] + \mathrm{V}[\bar{Y}\_{..}] - 2\mathrm{Cov}(\bar{Y}\_{i.},\bar{Y}\_{..}) \\\\
	\begin{align}
	\mathrm{Cov}(\bar{Y}\_{i.},\bar{Y}\_{..}) &= \mathrm{Cov}(\bar{Y}\_{i.},\frac{1}{I} \sum^{I}\_{k=1}\bar{Y}\_{k.}) \\\\
	&= \frac{1}{I}\mathrm{E}[(\bar{Y}\_{i.} - \mathrm{E}[\bar{Y}\_{i.}])(\sum^{I}\_{k=1}\bar{Y}\_{k.} - \mathrm{E}[\sum^{I}\_{k=1}\bar{Y}\_{k.}]) \\\\
	&= \frac{1}{I} \sum^{I}\_{k=1} \mathrm{E}[(\bar{Y}\_{i.} - \mathrm{E}[\bar{Y}\_{i.}])(\bar{Y}\_{k.} - \mathrm{E}[\bar{Y}\_{k.}])] \\\\
	&= \frac{1}{I} \mathrm{V}[\bar{Y}\_{i.}] \\\\
	&= \frac{1}{I} \frac{1}{J} \sigma^2
	\end{align} \\\\
	\mathrm{V}[\bar{Y}\_{i.} - \bar{Y}\_{..}] = \frac{\sigma^2}{J} + \frac{\sigma^2}{I J} - 2 \frac{\sigma^2}{I J} = \frac{1}{J}(1-\frac{1}{I})\sigma^2
\\]
なので,\\(\bar{Y}\_{i.} - \bar{Y}\_{..}\\)が\\(\alpha_i\\)の推定量.   

\\[
	\begin{align}
	Y\_{ij} - \bar{Y}\_{i.} &= \mu + \alpha_i + E_{ij} - (\mu + \alpha_i + \frac{1}{J} \sum^{J}\_{j=1}E_{ij}) \\\\
	&= E_{ij} - \frac{1}{J}\sum^{J}\_{j=1}E_{ij} \\\\
	&= E_{ij} - \bar{E}_{i.}
	\end{align} \\\\
\\]

\\[
	\mathrm{E}[Y\_{ij} - \bar{Y}\_{i.}] = 0 \\\\
	\begin{align}
	\mathrm{V}[Y\_{ij} - \bar{Y}\_{i.}] &= \mathrm{V}[E_{ij} - \frac{1}{J}\sum^{J}\_{j=1}E_{ij}] \\\\
		&= \mathrm{V}[E_{ij}] + \mathrm{V}[\frac{1}{J}\sum^{J}\_{j=1}E_{ij}] - 2\mathrm{Cov}(E_{ij},\frac{1}{J}\sum^{J}\_{j=1}E_{ij}) \\\\
		&= \sigma^2 + \frac{1}{J}\sigma^2 - 2 \mathrm{E}[(E_{ij} - \mathrm{E}[E_{ij}])(\frac{1}{J}\sum^{J}\_{j=1}E_{ij} - \mathrm{E}[\frac{1}{J}\sum^{J}\_{j=1}E_{ij}])] \\\\
		&= (1 + \frac{1}{J})\sigma^2 - 2 \frac{1}{J} \sum^{J}\_{k=1} \mathrm{E}[(E_{ij} - \mathrm{E}[E_{ij}])(E_{ik} - \mathrm{E}[E_{ik}])] \\\\
		&= (1 + \frac{1}{J})\sigma^2 - 2 \frac{1}{J} \sigma^2 \\\\
		&= (1 - \frac{1}{J})\sigma^2
	\end{align}
\\]

\\(\alpha_i\\)のばらつきを調べたいので,\\(\mu_{A_i}\\)と\\(\mu\\)の距離を得たい.
\\[
\begin{align}
	SS_A &= \sum^{I}_{i=1} \sum^{J}\_{j=1} (\bar{Y}\_{i.} - \bar{Y}\_{..})^2 \\\\
		 &= J\sum^{I}\_{i=1}(\bar{Y}\_{i.} - \bar{Y}\_{..})^2
\end{align}
\\]

\\[
\begin{align}
	\mathrm{E}[SS_A] &= \mathrm{E}[(\bar{Y}\_{i.} - \bar{Y}\_{..})^2] \\\\
	&=J\sum^{I}\_{i=1}\mathrm{E}[(\bar{Y}\_{i.} - \bar{Y}\_{..})^2] \\\\
	&=J\sum^{I}\_{i=1}\mathrm{E}[(\bar{Y}\_{i.} - \bar{Y}\_{..} - \mathrm{E}[\bar{Y}\_{i.} - \bar{Y}\_{..}] + \mathrm{E}[\bar{Y}\_{i.} - \bar{Y}\_{..}])^2] \\\\
	&=J\sum^{I}\_{i=1}\mathrm{E}[(\bar{Y}\_{i.} - \bar{Y}\_{..} - \mathrm{E}[\bar{Y}\_{i.} - \bar{Y}\_{..}])^2 + 2\alpha_i (\bar{Y}\_{i.} - \bar{Y}\_{..} - \mathrm{E}[\bar{Y}\_{i.} - \bar{Y}\_{..}])  + \alpha_i^2] \\\\
	&=J\sum^{I}\_{i=1} \Bigl\\{ \mathrm{V}[\bar{Y}\_{i.} - \bar{Y}\_{..}] + \alpha_i^2 \Bigr\\} \\\\
    &= J\sum^{I}\_{i=1} \alpha_i^2 + J\sum^{I}\_{i=1} \frac{1}{J}(1-\frac{1}{N_{A}})\sigma^2 \\\\
    &= J\sum^{I}\_{i=1} \alpha_i^2 + (N_{A}-1)\sigma^2
\end{align}
\\]

で,実験誤差は,
\\[
	SS_E = \sum^{I}_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.})^2 \\\\
	\begin{align}
		\mathrm{E}[SS_E] &= \mathrm{E}[\sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.})^2] \\\\
		&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \mathrm{E}[(Y\_{ij} - \bar{Y}\_{i.})^2] \\\\
		&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \mathrm{E}[(E\_{ij} - \bar{E}\_{i.})^2] \\\\
		&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \mathrm{E}[(E\_{ij} - \bar{E}\_{i.}) - \mathrm{E}[E\_{ij} - \bar{E}\_{i.}] + \mathrm{E}[E\_{ij} - \bar{E}\_{i.}] )^2] \\\\
		&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \mathrm{E}[((E\_{ij} - \bar{E}\_{i.}) - \mathrm{E}[E\_{ij} - \bar{E}\_{i.}])^2 + 2 ((E\_{ij} - \bar{E}\_{i.}) - \mathrm{E}[E\_{ij} - \bar{E}\_{i.}]) \mathrm{E}[E\_{ij} - \bar{E}\_{i.}] + \mathrm{E}[E\_{ij} - \bar{E}\_{i.}]^2] \\\\
		&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} \mathrm{V}[E\_{ij} - \bar{E}\_{i.}] \\\\
		&= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (1 - \frac{1}{J})\sigma^2 \\\\
		&= I(J-1)\sigma^2
	\end{align}
\\]

から,\\(H_0\\)のときは,\\(\sigma^2\\)の不偏推定量は,\\(MS_A = \frac{SS_A}{I-1}\\)と\\(MS_E = \frac{SS_E}{I(J-1)}\\),\\(MS_{\cdot}\\)を平均平方和という.
\\[
	\frac{(I(J-1))MS_E}{\sigma^2} \sim \chi^2_{I(J-1)} \\\\
	\frac{(I-1)MS_A}{\sigma^2} \sim \chi^2_{I-1}
\\]

\\[
	\frac{(\frac{(I-1)MS_A}{\sigma^2})/(I-1)}{(\frac{(I(J-1))MS_E}{\sigma^2})/(I(J-1))} = \frac{MS_A}{MS_E} = \frac{SS_A/(I-1)}{SS_E/I(J-1)} \sim F_{I-1, I(J-1)}
\\]

もし,\\(H_1\\)であるときは,この\\(F\\)分布よりは外れているはずである.

\\[
	SS_T = \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y_{ij} - \bar{Y}_{..})^2
\\]
として,\\(SS_T\\)を総平方和という.
\\[
\begin{align}
	SS_T &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.} + \bar{Y}\_{i.} - Y\_{..})^2 \\\\
		 &= \sum^{I}\_{i=1} \sum^{J}\_{j=1} ((Y\_{ij} - \bar{Y}\_{i.})^2 + 2(Y\_{ij} - \bar{Y}\_{i.})(\bar{Y}\_{i.} - Y\_{..}) + (\bar{Y}\_{i.} - Y\_{..})^2) \\\\
		 &= SS_A + SS_E + 2 \sum^{I}\_{i=1} \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.})(\bar{Y}\_{i.} - Y\_{..}) \\\\
		 &= SS_A + SS_E + 2 \sum^{I}\_{i=1} (\bar{Y}\_{i.} - Y\_{..}) \sum^{J}\_{j=1} (Y\_{ij} - \bar{Y}\_{i.}) \\\\
		 &= SS_A + SS_E + 2 \sum^{I}\_{i=1} (\bar{Y}\_{i.} - Y\_{..})(J \bar{Y}\_{i.} - J \bar{Y}\_{i.}) \\\\
		 &= SS_A + SS_E
\end{align}
\\]
である.

#### 分散分析表
データの自由度,平方和をならべた表を**分散分析表**という.
<table>
<tr>
	<th>変動因子</th><th>自由度</th><th>平方和</th><th>平均平方和</th><th>F値</th>
</tr>
<tr>
	<th>因子\(A\)</th><td>\(I-1\)</td><td>\(SS_A\)</td><td>\(MS_A=\frac{1}{I-1}SS_A\)</td><td>\(MS_A/MS_E\)</td>
</tr>
<tr>
	<th>誤差\(E\)</th><td>\(I(J-1)\)</td><td>\(SS_E\)</td><td>\(MS_E=\frac{1}{I(J-1)}SS_E\)</td>
</tr>
<tr>
	<th>全体</th><td>\(IJ-1\)</td><td>\(SS_T\)</td>
</tr>
</table>

#### 母平均の推定
\\(\mu_{A_i} = \mathrm{E}[\bar{Y}\_{i.}]\\)より,\\(\bar{Y}\_{i.}\\)は\\(\mu\_{A_i}\\)の不偏推定量.   
\\(\bar{Y}\_{i.} \sim \mathcal{N}(\mu\_{A_i}, \frac{\sigma^2}{J}) \\)から,
\\[
	\frac{\sqrt{J}(\bar{Y}\_{i.} - \mu\_{A_i})}{\sigma} \sim \mathcal{N}(0, 1)
\\]

\\(\sigma^2\\)が未知の場合,\\(MS_E\\)を利用する
\\[
	\frac{\frac{\sqrt{J}(\bar{Y}\_{i.} - \mu\_{A_i})}{\sigma}}{\sqrt{\frac{\frac{(I(J-1))MS_E}{\sigma^2}}{I(J-1)}}} = \frac{\sqrt{J}(\bar{Y}\_{i.} - \mu\_{A_i})}{MS_E} \sim T_{I(J-1)}
\\]
上記が統計検定量. \\(\mu\_{A_i}\\)の信頼係数\\(1-100\alpha\\%\\)の信頼区間は両側の場合,\\(P(T_{I(J-1)} > t_{I(J-1),\frac{\alpha}{2}}) = P(T_{I(J-1)} < -t_{I(J-1),\frac{\alpha}{2}}) = \frac{\alpha}{2}\\)として,
\\[
\begin{align}
	P\Bigl(\frac{\sqrt{J}(\bar{Y}\_{i.} - \mu\_{A_i})}{MS_E} > t_{I(J-1),\frac{\alpha}{2}}\Bigr) &= P\Bigl(\bar{Y}\_{i.} - \mu\_{A_i} > \frac{MS_E \cdot t_{I(J-1),\frac{\alpha}{2}}}{\sqrt{J}} \Bigr) \\\\
	&= P\Bigl(\bar{Y}\_{i.} > \frac{MS_E \cdot t_{I(J-1),\frac{\alpha}{2}}}{\sqrt{J}} + \mu\_{A_i} \Bigr) \\\\
	&= \frac{\alpha}{2}
\end{align}
\\]
もう片側も同様で,実際に得られたデータを当てはめると,
\\[
	\bar{y}\_{i.} - \frac{MS_E \cdot t_{I(J-1),\frac{\alpha}{2}}}{\sqrt{J}} < \mu_{A_i} < \bar{y}\_{i.} + \frac{MS_E \cdot t_{I(J-1),\frac{\alpha}{2}}}{\sqrt{J}}
\\]
が母平均の信頼区間.

#### 母平均の差の推測
\\(	H_0:全てのiに対して\alpha_i=0\\)が棄却されるときに,\\(i,j,i \not= j\\)に対して,どの\\(i,j\\)が\\(\mu_{A_i} \not= \mu_{A_j}\\)であったか知りたいときは,\\(\mu_{A_i} - \mu_{A_j}\\)の推測を行う.   
\\(\bar{Y}\_{i.} - \bar{Y}\_{j.} \sim \mathcal{N}(\mu_{A_i} - \mu_{A_j}, \frac{\sigma^2}{N_{A_i}} + \frac{\sigma^2}{N_{A_j}})\\)なので,
\\[
\frac{\bar{Y}\_{i.} - \bar{Y}\_{j.} - (\mu_{A_i} - \mu_{A_j})}{\sqrt{(\frac{1}{N_{A_i}} + \frac{1}{N_{A_j}})\sigma^2}} \sim \mathcal{N}(0, 1)
\\]

\\(\sigma^2\\)の推定量として,\\(MS_E \sim \chi^2_{I(J-1)}\\)を使い,
\\[
\frac{\frac{\bar{Y}\_{i.} - \bar{Y}\_{j.} - (\mu_{A_i} - \mu_{A_j})}{\sqrt{(\frac{1}{N_{A_i}} + \frac{1}{N_{A_j}})\sigma^2}}}{\sqrt{\frac{\frac{(I(J-1))MS_E}{\sigma^2}}{I(J-1)}}} = \frac{1}{\sqrt{\frac{1}{N_{A_i}} + \frac{1}{N_{A_j}}}}\frac{\bar{Y}\_{i.} - \bar{Y}\_{j.} - (\mu_{A_i} - \mu_{A_j})}{\sqrt{MS_E}} \sim T_{I(J-1)}
\\]

#### 一元配置で水準間の繰り返し回数が違う場合
一元配置で水準間の繰り返し回数が違う場合を考える. 水準\\(A_i\\)での繰り返し回数を\\(J_i\\)とする.
構造モデルは
\\[
	Y_{ij} = \mu_{A_i} + E\_{ij} = \mu + \alpha_i + E\_{ij} \\\\
	J = \sum^{I}\_{i=1} J_i \\\\
   	\mu = \mathrm{E}[\bar{Y}\_{..}] \\\\
	\bar{Y}\_{i.} = \frac{1}{J_i} \sum^{J_i}\_{j=1} Y_{ij} \\\\
	\bar{Y}\_{..} = \frac{1}{J}\sum^{I}\_{i=1}\sum^{J_i}\_{j=1} Y_{ij} \\\\
\\]

\\(\mu = \mathrm{E}[\bar{Y}\_{..}]\\)としたので、
\\[
\begin{align}
 \mu &= \mathrm{E}[\frac{1}{J}\sum^{I}\_{i=1}\sum^{J_i}\_{j=1} Y_{ij}] \\\\
&= \frac{1}{J}\sum^{I}\_{i=1}\sum^{J_i}\_{j=1} \mathrm{E}[Y_{ij}] \\\\
&= \frac{1}{J}\sum^{I}\_{i=1}\sum^{J_i}\_{j=1} \mu_{A_i} \\\\
&= \frac{1}{J}\sum^{I}\_{i=1} J_i \mu_{A_i} \\\\
&= \frac{1}{J}\sum^{I}\_{i=1} J_i (\mu+\alpha_i) \\\\
&= \frac{1}{J} \Bigl( \sum^{I}\_{i=1} J_i\mu + \sum^{I}\_{i=1} J_i \alpha_i \Bigr) \\\\
&= \mu + \sum^{I}\_{i=1} J_i \alpha_i \\\\
\end{align}
\\]
から,
\\[
\sum^{I}\_{i=1} J_i \alpha_i = 0
\\]
総平方和\\(SS_T\\)は,
\\[
	SS_T = \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} ( Y_{ij} - \bar{Y}\_{..} )^2
\\]

因子\\(A\\)の平方和は,
\\[
\begin{align}
	SS_A &= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} ( \bar{Y}_{i.} - \bar{Y}\_{..} )^2 \\\\
		&= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} ( \mu + \alpha_i + \bar{E}\_{i.} - (\mu + \bar{E}\_{..}) )^2 \\\\
		&= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} (\alpha_i + \bar{E}\_{i.} - \bar{E}\_{..})^2 \\\\
\end{align}
\\]

誤差の平方和は,
\\[
\begin{align}
	SS_E &= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} ( Y_{ij} - \bar{Y}\_{i.} )^2 \\\\
		&= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1} ( \mu + \alpha\_i + E\_{ij} - (\mu + \alpha_i + \bar{E}\_{i.}) )^2 \\\\
		&= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1} (E\_{ij} -  \bar{E}\_{i.})^2
\end{align}
\\]

\\[
\begin{align}
	SS_T &= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} ( Y_{ij} - \bar{Y}\_{..} )^2 \\\\
		 &= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} ( Y_{ij} - \bar{Y}\_{i.} + \bar{Y}\_{i.} -\bar{Y}\_{..} )^2 \\\\
		 &= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} \Bigl\\{ (Y_{ij} - \bar{Y}\_{i.})^2 - 2 (Y_{ij} - \bar{Y}\_{i.})(\bar{Y}\_{i.} -\bar{Y}\_{..}) + (\bar{Y}\_{i.} -\bar{Y}\_{..} )^2 \Bigr\\} \\\\
		 &= \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} (Y_{ij} - \bar{Y}\_{i.})^2 + \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} (\bar{Y}\_{i.} -\bar{Y}\_{..} )^2 \\\\
		 &= SS_A + SS_E
\end{align}
\\]

\\[
\begin{align}
	\mathrm{E}[SS_A] &= \mathrm{E}\Bigr[ \sum^{I}\_{i=1} \sum^{J_i}\_{j=1} (\alpha_i + \bar{E}\_{i.} - \bar{E}\_{..})^2 \Bigl] \\\\
			&= \mathrm{E}\Bigr[\sum^{I}\_{i=1} J_i \Bigl\\{\alpha_i^2 + 2\alpha_i(\bar{E}\_{i.} - \bar{E}\_{..}) + (\bar{E}\_{i.} - \bar{E}\_{..})^2 \Bigl\\} \Bigl] \\\\
			&= \sum^{I}\_{i=1} J_i \alpha_i^2  + \sum^{I}\_{i=1} J_i \mathrm{E}\Bigr[ (\bar{E}\_{i.} - \bar{E}\_{..})^2 \Bigl] \\\\
			&= \sum^{I}\_{i=1} J_i \alpha_i^2  + \sum^{I}\_{i=1} J_i \mathrm{V}\Bigr[ \bar{E}\_{i.} - \bar{E}\_{..} \Bigl] \\\\
\end{align}
\\]

\\[
\begin{align}
	\mathrm{V}[\bar{E}\_{i.} - \bar{E}\_{..}] &= \mathrm{V}[\bar{E}\_{i.}] - 2\mathrm{Cov}(\bar{E}\_{i.},\bar{E}\_{..}) + \mathrm{V}[\bar{E}\_{..}] \\\\
	\mathrm{Cov}(\bar{E}\_{i.},\bar{E}\_{..}) &= \mathrm{Cov}(\bar{E}\_{i.},\frac{1}{I} \sum^{I}_{i=1} \bar{E}\_{i.}) \\\\
	&= \frac{1}{I} \sum^{I}\_{i=1} \mathrm{Cov}(\bar{E}\_{i.}, \bar{E}\_{i.}) \\\\
	&= \frac{1}{I} \sum^{I}\_{i=1} \mathrm{V}[\bar{E}\_{i.}] \\\\
	&= \frac{1}{I} \sum^{I}\_{i=1} \frac{\sigma^2}{J_i}\\\\
	\mathrm{V}[\bar{E}\_{i.} - \bar{E}\_{..}] &= \frac{\sigma^2}{J_i} - \frac{2}{I} \sum^{I}\_{k=1} \frac{\sigma^2}{J_k} + \frac{\sigma^2}{J} \\\\
	\mathrm{E}[SS_A] &= \sum^{I}\_{i=1} J_i \alpha_i^2  + \sum^{I}\_{i=1} J_i \Bigr(\frac{\sigma^2}{J_i} - \frac{2}{I} \sum^{I}\_{k=1} \frac{\sigma^2}{J_k} + \frac{\sigma^2}{J} \Bigl) \\\\
		&= \sum^{I}\_{i=1} J_i \alpha_i^2  + I\sigma^2 - \frac{2}{I} \sum^{I}\_{i=1} J_i \sum^{I}\_{k=1} \frac{\sigma^2}{J_k} + \sigma^2 \\\\
		&= \sum^{I}\_{i=1} J_i \alpha_i^2  + I\sigma^2 - \frac{2}{I} \sum^{I}\_{i=1} \sum^{I}\_{k=1} \frac{J_i}{J_k} \sigma^2 + \sigma^2 \\\\
		&= \sum^{I}\_{i=1} J_i \alpha_i^2  + I\sigma^2 - \frac{2}{I} \sum^{I}\_{k=1} \frac{J}{J_k} \sigma^2 + \sigma^2 \\\\
		&= \sum^{I}\_{i=1} J_i \alpha_i^2  + I\sigma^2 - 2\sigma^2 + \sigma^2 \\\\
	&= \sum^{I}\_{i=1} J_i \alpha_i^2  + (I-1)\sigma^2
\end{align}
\\]

\\[
\begin{align}
	\mathrm{E}[SS\_E] &= \mathrm{E}[(E\_{ij} -  \bar{E}\_{i.})^2] \\\\
	&= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1}\mathrm{E}[(E\_{ij} -  \bar{E}\_{i.})^2] \\\\
	&= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1}\mathrm{V}[E\_{ij} -  \bar{E}\_{i.}] \\\\
	&= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1}\Bigl\\{ \mathrm{V}[E\_{ij}] - 2 \mathrm{Cov}(E\_{ij},\bar{E}\_{i.}) + \mathrm{V}[\bar{E}\_{i.}] \Bigr\\}\\\\
	&= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1}\Bigl\\{ \sigma^2 + \frac{\sigma^2}{J_i} - 2 \mathrm{Cov}(E\_{ij},\bar{E}\_{i.}) \Bigr\\}\\\\
	\mathrm{Cov}(E\_{ij},\bar{E}\_{i.}) &= \mathrm{Cov}(E\_{ij}, \bar{E}\_{i.}) \\\\
	&= \mathrm{Cov}(E\_{ij}, \frac{1}{J\_i} \sum^{J\_i}\_{k=1}  E\_{ik}) \\\\
	&= \frac{1}{J\_i} \sum^{J\_i}\_{k=1} \mathrm{Cov}(E\_{ij}, E\_{ik})  \\\\
	&= \frac{1}{J\_i} \mathrm{V}[E\_{ij}] \\\\
	&= \frac{1}{J\_i} \sigma^2 \\\\
	\mathrm{E}[SS\_E] &= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1}\Bigl\\{ \sigma^2 + \frac{\sigma^2}{J_i} - \frac{2}{J\_i} \sigma^2 \Bigr\\}\\\\
	&= \sum^{I}\_{i=1} \sum^{J\_i}\_{j=1} \Bigl(1 - \frac{1}{J_i}\Bigr)\sigma^2 \\\\
	&= \sum^{I}\_{i=1} (J_i -  1)\sigma^2 \\\\
	&= ( J -  I)\sigma^2 \\\\
\end{align}
\\]

仮説は,
\\[
	H_0:全てのiに対して\alpha_i=0 \\; \mathrm{vs} \\; H_1:いずれかのiに対して\alpha_i\not=0
\\]
\\(H_0\\)のとき,
\\[
	MS_A = \frac{1}{I-1} SS_A, 	MS_E = \frac{1}{J-I} SS_E, 
\\]
としたら,それぞれは\\(\sigma^2\\)の不偏推定量.
\\[
	\frac{(I-1)MS_A}{\sigma^2} \sim \chi^2_{I-1} \\\\
	\frac{(J-I)MS_E}{\sigma^2} \sim \chi^2_{J-I} \\\\
\\]
なので,
\\[
	\frac{MS_A}{MS_E} \sim F_{I-1,J-I}
\\]
が検定統計量となる,分散分析表は,
<table>
<tr>
	<th>変動因子</th><th>自由度</th><th>平方和</th><th>平均平方和</th><th>F値</th>
</tr>
<tr>
	<th>因子\(A\)</th><td>\(I-1\)</td><td>\(SS_A\)</td><td>\(MS_A=\frac{1}{I-1}SS_A\)</td><td>\(MS_A/MS_E\)</td>
</tr>
<tr>
	<th>誤差\(E\)</th><td>\(J-I\)</td><td>\(SS_E\)</td><td>\(MS_E=\frac{1}{J-I)}SS_E\)</td>
</tr>
<tr>
	<th>全体</th><td>\(J-1\)</td><td>\(SS_T\)</td>
</tr>
</table>
