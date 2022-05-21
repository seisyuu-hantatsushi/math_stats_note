## 確率測度の性質
確率測度は一般の測度性質を受け継ぐ.
以下,\\(\mathcal{F}\\)を完全加法族,\\(P\\)を

### 有限加法性
事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)とした時

\\[
	P(\bigcup^{n} _{k=1} A_k) = P(\coprod^{n} _{k=1} A_k) = \sum^{n} _{k=1} P(A_k) \tag{PM.4}
\\]

- 証明  
  測度空間の有限加法性の証明と同様

### 単調性
  \\[
  A_1,A_2 \in \mathcal{F} \land A_1 \subset A_2 \to P(A_1) \leq P(A_2) \tag{PM.5}
  \\]
  - 証明  
    測度空間の単調性の証明と同様

事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)について,
\\[
  A_k \subset A_{k+1}
\\]
を満たすとき**単調増大列**といい,
\\[
  A_k \supset A_{k+1}
\\]
を満たすとき**単調減少列**という.

#### 劣加法性
事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)とした時
\\[
	P(\bigcup^{\infty}_{k=0}A_k) \leq \sum^{\infty} _{i=0} P(A_k) \tag{PM.6}
\\]
- 証明
  測度空間の劣加法性の証明と同様


### 上方連続性
事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)が単調増大列のとき
\\[
P(\bigcup^{\infty} _ {k=1} A_k) =\lim_{k \to \infty} P(A_k) \tag{PM.7}
\\]
が成立しこれを上方連続性という.

- 証明  
  測度空間の上方連続性の証明と同様

### 下方連続性
事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)が単調減少列のとき
\\[
P(\bigcap^{\infty} _ {k=1} A_k) = \lim_{k \to \infty} P(A_k) \tag{PM.8}
\\]
が成立しこれを下方連続性という.

- 証明  
  測度空間の下方連続性の証明と同様
