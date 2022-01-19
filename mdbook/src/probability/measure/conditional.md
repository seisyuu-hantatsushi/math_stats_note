#### 条件付き確率
2つの事象\\(A,B\\)にて\\(P(B) > 0 \\)のとき
\\[
	P(A|B) = \frac{P(A \cap B)}{P(B)}
\\]
と表したものを\\(B\\)を与えたときの\\(A\\)の条件付き確率と言う.
\\(B\\)を与えたときとは\\(B\\)が発生したということが分かっているということである.
上記式から,
\\[
\begin{align}
	P(A \cap B) &= P(A|B)P(B) \\\\
	P(A \cap B) &= P(B|A)P(A), P(A) > 0 \\\\
\end{align}
\\]

#### 乗法定理
\\(A_1,A_2,\dots,A_n\\)の\\(n\\)個の事象の積事象の確率は,
\\[
P(A_1 \cap A_2 \cap \dots \cap A_n) = P(A_n|A_1 \cap A_2 \cap \dots \cap A_{n-1}) \cdots P(A_2|A_1) P(A_1)
\\]
となり,これを**乗法定理**という
- 証明  
  \\(n = 1\\)のときは自明  
  \\(n = 2\\)のとき
  \\[
	  P(A_2 \cap A_1) = P(A_2 | A_1)P(A_1)
  \\]
  \\(n = k\\)のとき
  \\[
	  P(A_1 \cap A_2 \cap \dots \cap A_k) = P(A_k|A_1 \cap A_2 \cap \dots \cap A_{k-1}) \cdots P(A_2|A_1) P(A_1)
  \\]
  が成立すると仮定する.  
  \\(n = k+1\\)のとき
  \\[
  \begin{align}
   P(A_{k+1}|A_1 \cap A_2 \cap \dots \cap A_{k}) &= \frac{P(A_1 \cap A_2 \cap \dots \cap A_{k+1})}{P(A_1 \cap A_2 \cap \dots \cap A_{k})} \\\\
P(A_1 \cap A_2 \cap \dots \cap A_{k+1}) &= P(A_1 \cap A_2 \cap \dots \cap A_{k})P(A_{k+1}|A_1 \cap A_2 \cap \dots \cap A_{k})
  \end{align}
  \\]
	\\(n=k\\)のときの式を代入し
\\[
  \begin{align}
	P(A_1 \cap A_2 \cap \dots \cap A_{k+1}) &= P(A_1 \cap A_2 \cap \dots \cap A_{k})P(A_k|A_1 \cap A_2 \cap \dots \cap A_{k-1}) \cdots P(A_2|A_1) P(A_1)
  \end{align}
  \\]

### 全確率の公式
事象\\(B_1,B_2,\dots,B_n\\)を互いに排反な事象とする,\\(P(B_i)>0,i=1,2,\dots,n\\)かつ\\(\bigcup^{n} _ {i=1} B_i = \Omega\\)のとき
\\[
	P(A) = \sum^{\infty}_{i=1} P(A|B_i)P(B_i)
\\]
が成立する.これを**全確率の公式**という.
- 証明  
  \\(A = A \cap \Omega = A \cap \bigcup^{n} _ {i=1} B_i = \bigcup^{n} _ {i=1} A \cap B_i \\)で\\(B_i\\)が互いに排反なので,
  \\[
\begin{align}
P(\bigcup^{n} _ {i=1} A \cap B_i) &= \sum^{n}_{i=1} P(A \cap B_i) \\\\
&= \sum^{n} _{i=1} P(A|B_i)P(B_i)
\end{align}
  \\]

### Bayesの定理
事象\\(B_1,B_2,\dots,B_n\\)を互いに排反な事象とする,\\(P(B_i)>0,i=1,2,\dots,n\\)かつ\\(\bigcup^{n} _ {i=1} B_i = \Omega\\)のとき,\\(A\\)を与えたときの\\(B_j\\)の確率は,
\\[
	P(B_j|A) = \frac{P(A|B_j)P(B_j)}{\sum^{n} _{i=1} P(A|B_i)P(B_i)}
\\]
となる.
- 証明  
\\[
\begin{align}
\frac{P(A|B_j)P(B_j)}{\sum^{n} _{i=1} P(A|B_i)P(B_i)} &= \frac{P(A|B_j)P(B_j)}{P(A)} \\\\
&= \frac{P(A \cap B_j)}{P(B_j)}\frac{P(B_j)}{P(A)} \\\\
&= P(B_j|A) \\\\
\end{align}
\\]

### 独立
事象\\(A,B\\)に関連性がない場合,\\(B\\)の確率に\\(A\\)の確率が影響しない場合,条件付き確率は,\\(P(B|A)=P(B)\\)となる.であるので,
\\[
  P(A \cap B) = P(A)P(B)
\\]
が成立するとき,事象\\(A,B\\)は**独立**していると言い.事象\\(A,B\\)の独立性とも言う.
