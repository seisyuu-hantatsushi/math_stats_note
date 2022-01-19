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

