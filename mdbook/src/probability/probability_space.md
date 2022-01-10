# 確率空間
事象の確率は,全事象の内でその事象が発生,観測できる割合で表される.なので,\\([0,1]\\)の間の値で表される.なので,事象の確率を得る関数\\(P(\cdot)\\)は,
\\[
	P: \mathfrak{P}(\Omega) \mapsto [0,1]
\\]
で定義される写像である.\\(P(A)\\)は事象\\(A\\)の確率である.

関数\\(P(\cdot)\\)は集合の大きさを測る関数なので,**測度**となる.なので,事象は可測集合だけで構成されているのが良い.可測集合にするには,可測なるような構造を与えないといけない.
以下のような,完全加法族,(\\(\sigma\\)-加法族)をあたえると,集合は可測となる.

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

## 確率空間
標本空間と確率測度をまとめたものを**確率空間**と言う.\\((\Omega,\mathcal{F},P)\\)で表す.

