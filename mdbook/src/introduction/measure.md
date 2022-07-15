# 測度
数学において,対象を**測る**ということは,集合の大きさ得るということである.
そのための関数を**測度**と言う. 測る対象の集合が測ることが可能なら**可測**といい,
その集合を**可測集合**と言う.

## 準備
以下のように自然数,実数などの集合を定義する.
- \\(\mathbb{N} = \\{0,1,2,\dots\\} \\)
- \\(\mathbb{N}_+ = \\{1,2,\dots\\} \\)
- \\(\overline{\mathbb{N}} = \mathbb{N} \cup \\{ +\infty \\} \\)
- \\(\overline{\mathbb{N}_+} = \\{1,2,\dots\\} \cup \\{ +\infty \\} \\)
- \\(\mathbb{R} = \\{x|実数\\} \\)
- \\(\mathbb{R}^d = \prod_{i=1}^{d} \mathbb{R} \\)
- \\(\mathbb{R}_+ = \\{x|x \geq 0 の実数\\} \\)
- \\(\overline{\mathbb{R}} = \\{x|実数\\}\cup \\{-\infty,+\infty \\} \\)
- \\(\overline{\mathbb{R}\_{+}} = \\mathbb{R}\_{+} \cup \\{+\infty\\} \\)


## 測度
測度
: 集合\\( S \\)から集合\\(\overline{\mathbb{R}_{+}} = \\{x| 0 \leq x \leq \infty \\} = [0,\infty]\\)の
部分集合\\(D \subset \overline{ \mathbb{R} } \\)への写像である.
\\[
	m: S \mapsto D
\\]
集合\\(E \in \mathfrak{P}(S) \\)が可測なら,\\(m(E)\\)は集合\\(D\\)に属する値(要素)が定まる.
