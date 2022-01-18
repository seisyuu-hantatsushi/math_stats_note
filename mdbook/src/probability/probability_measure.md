# 確率測度

## 標本空間
全事象\\(\Omega\\)に完全加法族\\(\mathcal{F}\\)を与えると,**標本空間**\\((\Omega,\mathcal{F})\\)得る.したがって,以下の条件を満たす.
\\[
\emptyset \in \mathcal{F} \tag{O.1}
\\]
\\[
\forall A \in \mathcal{F} \land A \subset \Omega \to  A^c \in \mathcal{F} \tag{O.2}
\\]
\\[
A_i \in \mathcal{F},i \in I=\\{1,2,\dots\\} \to \displaystyle \bigcup_{i \in I} A_i \in \mathcal{F} \tag{O.3}
\\]

上記条件より
1. \\( \mathcal{F} \subset \mathfrak{P}(\Omega) \\) (\\(\mathcal{F}\\)は全事象\\(\Omega\\)の部分集合全体の内,可測であるものだけから構成される.)
1. \\(\emptyset^c \in \mathcal{F} \to \Omega \in \mathcal{F} \\)

## 確率測度
事象から確率を得る関数を**確率測度**と言う. 確率測度は以下の条件を満たす.
\\[
\begin{align}
 & \forall A \in \mathcal{F} \to P(A) \in [0,1] \tag{M.1} \\\\
 & P(\Omega) = 1 \tag{M.2} \\\\
 & \forall i,j \in I, \forall A_i, A_j ( A_i, A_j \in \mathcal{F}, i \not = j \to A_i \cap A_j = \emptyset) \to P(\displaystyle \bigcup_{i \in I} A_i) = \sum_{i \in I} P(A_i) \tag{M.3}
\end{align}
\\]

### 確率測度の演算
\\(\forall A,B \in \mathcal{F}\\)に対して,以下が成立する.

\\[
\begin{align}
& P(A^c) = 1 - P(A) \tag{P.1} \\\\
& A \subset B \to P(A) \leq P(B) \tag{P.2} \\\\
& P(A \cup B) = P(A) + P(B) - P(A \cap B) \tag{P.3} 
\end{align}
\\]

証明は以下の通り,
- (P.1)
\\[
\begin{align}
&({\rm O}.2) \to A \cup A^c = \Omega \Rightarrow \\\\
& ({\rm M}.2) \to P(A \cup A^c) = P(\Omega) = 1 \Rightarrow \\\\
& ({\rm M}.3) \to P(A)+P(A^c) = 1 \Rightarrow \\\\
& P(A^c) = 1-P(A)
\end{align}
\\]

- (P.2)
\\[
\begin{align}
& A \subset B \to B = A \cup (B \cap A^c) \land \emptyset = A \cap (B \cap A^c) \Rightarrow \\\\
& P(B) = P(A \cup (B \cap A^c)) = P(A) + P(B \cap A^c) \\Rightarrow\\\\
& ({\rm M}.1) \to P(A) \leq P(B)
\end{align}
\\]

- (P.3)
\\[
\begin{align}
P(A \cup B) &= P(((A \cup B) \cap (A \cap B)^c) \cup (A \cap B)) \\\\
&= P(((A \cup B) \cap (A \cap B)^c))+P(A \cap B) \\\\
&= P((A \cap (A \cap B)^c) \cup (B \cap (A \cap B)^c))+P(A \cap B) \\\\
&= P(A \cap (A \cap B)^c) + P(B \cap (A \cap B)^c)+P(A \cap B) \\\\
&= P((A^c \cup (A \cap B))^c) + P((B^c \cup (A \cap B))^c)+P(A \cap B) \\\\
&= 2-P(A^c \cup (A \cap B)) - P(B^c \cup (A \cap B))+P(A \cap B) \\\\
&= 2-P(A^c) - P(A \cap B) - P(B^c) -P(A \cap B)+P(A \cap B) \\\\
&= 1 - P(A^c) + 1 - P(B^c) - P(A \cap B) \\\\
&= P(A) + P(B) - P(A \cap B) \\\\
\end{align}
\\]

### 条件付き確率

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
