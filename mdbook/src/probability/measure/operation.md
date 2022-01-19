# 確率の演算
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
