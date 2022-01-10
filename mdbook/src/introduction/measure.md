# 測度
数学において,対象を**測る**ということは,集合の大きさ得るということである.
そのための関数を**測度**と言う. 測る対象の集合が測ることが可能なら**可測**といい,
その集合を**可測集合**と言う.

## 測度
測度
: 集合\\( S \\)の冪集合\\( \mathfrak{P}(S) \\)から集合\\(\overline{\mathbb{R}^{+}} = \\{x| 0 \leq x \leq \infty \\} = [0,\infty]\\)の部分集合\\(D \subset \overline{\mathbb{R}^{+}} \\)への写像である.
\\[
	m: \mathfrak{P}(S) \mapsto D
\\]
集合\\(E \in \mathfrak{P}(S) \\)が可測なら,\\(m(E)\\)は集合\\(D\\)に属する値(要素)が定まる.

## 可測集合

- 完全加法族\\(\mathcal{F}\\)
  1. \\( \emptyset \in \mathcal{F} \\)
  1. \\( \forall A \in \mathcal{F} \to  A^c \in \mathcal{F} \\)
  1. \\(A_i \in \mathcal{F},i \in I=\\{1,2,\dots\\} \to \displaystyle \bigcup_{i \in I} A_i \in \mathcal{F} \\)
