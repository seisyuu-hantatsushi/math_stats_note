# 事象

## 集合論との対応付
集合論で扱うためには,偶然性を含む行為で得られる結果を対象としないといけない.
偶然性を含む行為で対象を得ることを**試行**と言う.偶然性を含む行為とは具体的には,実験,調査,観測である.1回の試行から得られた結果の値を,**単一事象**,**観測値**などと言う.これが,集合の要素に当たり,単一事象の集合を**事象**という.
試行により得られる全単一事象の集合を**標本空間**,**全事象**といい,\\(\Omega\\)で表す.ある事象\\(A\\)は全事象の部分空間である.
\\[
	A \subset \Omega
\\]

### 事象の演算
事象も集合と同じ演算が行える.
- 積事象 \\( A \cap B \\) &emsp; 事象\\( A, B\\)がともに起こる.
- 和事象 \\( A \cup B \\) &emsp; 事象\\( A, B\\)どちらかが起こる.
- 余事象 \\( A^c \\) &emsp; 事象\\( A \\)ではない事象が起こる.
- 空事象 \\( \emptyset \\) &emsp; 単一事象を全く含まない事象.

これらから,以下を定義する.
- 差事象 \\(A \backslash B = A \cap B^c\\)
- 対称差 \\(A \Delta B = (A \backslash B) \cup (B \backslash A)\\)  

事象\\(A,B\\)にて,\\( A \cap B = \emptyset \\)ならば,事象\\(A,B\\)は互いに**排反**である.

集合の演算と同様,**交換律**,**結合律**,**分配律**が成立する.
- 交換律
  - \\( A \cap B = B \cap A,  A \cup B = B \cup A \\)
- 結合律
  - \\( A \cap B \cap C = (A \cap B) \cap C = A \cap (B \cap C) \\)
  - \\( A \cup B \cup C = (A \cup B) \cup C = A \cup (B \cup C) \\)
- 分配律
  - \\( A \cap (B \cup C) = (A \cap B) \cup (A \cap C) \\)
  - \\( A \cup (B \cap C) = (A \cup B) \cap (A \cup C) \\)

集合の演算と同様,**ド・モルガン則**が成立する.
  - \\( (A \cap B)^c = A^c \cup B^c \\)
  - \\( (A \cup B)^c = A^c \cap B^c \\)
