## 確率の連続性

事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)について,
\\[
A_k \subset A_{k+1}
\\]
を満たすとき**単調増大列**といい,
\\[
A_k \supset A_{k+1}
\\]
を満たすとき**単調減少列**という.

### 上方連続性
事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)が単調増大列のとき
\\[
P(\bigcup^{\infty} _ {k=1} A_k) =\lim_{k \to \infty} P(A_k)
\\]
が成立しこれを上方連続性という.

- 証明  
  測度空間の上方連続性の証明と同様

### 下方連続性
事象の列\\(A_k \in \mathcal{F},k=1,2,\dots\\)が単調減少列のとき
\\[
P(\bigcap^{\infty} _ {k=1} A_k) = \lim_{k \to \infty} P(A_k)
\\]
が成立しこれを下方連続性という.

- 証明  
  測度空間の下方連続性の証明と同様

### Borel-Cantelliの定理
\\(A_1,A_2,\dots\\)
