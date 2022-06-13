## ガウス積分
### \\(\int e^{-ax^2} dx\\)
\\[
  \begin{align}
	\int ^{\infty} _{-\infty} e^{-ax^2} dx &= \sqrt{\frac{\pi}{a}} \\\\
	\int ^{\infty} _{0} e^{-ax^2} dx &= \frac{1}{2}\sqrt{\frac{\pi}{a}}
  \end{align}
\\]
- 証明  
  \\(I = \int ^{\infty} _{-\infty} e^{-ax^2} dx\\)と置く,
  \\[
  \begin{align}
  I^2 &= \left(\int ^{\infty} _{-\infty} e^{-ax^2} dx\right)^2 \\\\
  &= \left(\int ^{\infty} _{-\infty} e^{-ax^2} dx\right)\left(\int ^{\infty} _{-\infty} e^{-ay^2} dy\right) \\\\
  &= \int ^{\infty} _{-\infty} \int ^{\infty} _{-\infty} e^{-a(x^2+y^2)} dy dx
  \end{align}
  \\]
  ここで,\\(x = r\cos\theta, y = r\sin\theta\\)と変数変換する.
  \\[
  \begin{align}
  \int ^{\infty} _{-\infty} \int ^{\infty} _{-\infty} e^{-a(x^2+y^2)} dy dx &= \int ^{\infty} _{0} \int ^{2\pi} _{0} e^{-ar^2}rdrd\theta \\\\
  &= 2\pi \int ^{\infty} _{0}  e^{-ar^2} rdr \\\\
  &= 2\pi \left[ -\frac{e^{-ar^2}}{2a} \right]^{\infty} _{0} \\\\
  &= \frac{\pi}{a}
  \end{align}
  \\]
  から\\(I^2=\frac{\pi}{a}\\)より,
  \\[
  \int ^{\infty} _{-\infty} e^{-ax^2} dx = \sqrt{\frac{\pi}{a}}
  \\]
  \\[
  \begin{align}
  \int ^{\infty} _{-\infty} e^{-ax^2} dx &= \int ^{\infty} _{0} e^{-ax^2} dx + \int ^{0} _{-\infty} e^{-ax^2} dx
  \end{align}
  \\]
  右辺第2項は\\(x=-y\\)と変数変換すると,
  \\[
  \int ^{0} _{-\infty} e^{-ax^2} dx = \int^{0} _{\infty} e^{-ay^2} -1 \cdot dy = \int^{\infty} _{0} e^{-ay^2} dy
  \\]
  から,
  \\[
  \int ^{\infty} _{-\infty} e ^{-ax^2} dx = 2 \int ^{\infty} _{0} e ^{-ax^2} dx
  \\]
  となり,
  \\[
  \int ^{\infty} _{0} e^{-ax^2} dx = \frac{1}{2} \sqrt{\frac{\pi}{a}}
  \\]

### \\(\int xe^{-ax^2} dx\\)
\\[
  \begin{align}
	\int ^{\infty} _{-\infty} xe^{-ax^2} dx &= 0 \\\\
	\int ^{\infty} _{0} xe^{-ax^2} dx &= \frac{1}{2a}
  \end{align}
\\]

- 証明  
\\[
	\int ^{\infty} _{-\infty} xe^{-ax^2} dx = \left[ -\frac{e^{-ax^2}}{2a} \right] ^{\infty} _{-\infty} = 0
\\]
\\[
	\int ^{\infty} _{0} xe^{-ax^2} dx = \left[ -\frac{e^{-ax^2}}{2a} \right] ^{\infty} _{0} = \frac{1}{2a}
\\]

### \\(\int x^2e^{-ax^2} dx\\)
\\[
  \begin{align}
	\int ^{\infty} _{-\infty} x^2 e^{-ax^2} dx &= \frac{1}{4}\sqrt{\frac{\pi}{a^3}} \\\\
	\int ^{\infty} _{0} x^2 e^{-ax^2} dx &= \frac{1}{2}\sqrt{\frac{\pi}{a^3}}
  \end{align}
\\]

- 証明
\\[
	I_0(a) = \int ^{\infty} _{-\infty} e^{-ax^2} dx \\\\
	I_2(a) = \int ^{\infty} _{-\infty} x^2 e^{-ax^2} dx
\\]
とおく,
\\[
  I_2(a) = -\frac{1}{da} \int ^{\infty} _{-\infty}  e^{-ax^2} dx = -\frac{1}{da} I_0(a) = \int ^{\infty} _{-\infty}  x^2 e^{-ax^2} dx \\\\
\\]
から,
\\[
	 I_2(a) = -\frac{1}{da} \sqrt{\frac{\pi}{a}} = \frac{1}{2}\sqrt{\frac{\pi}{a^3}}
\\]

\\[
  \begin{align}
  \int ^{\infty} _{-\infty} x^2 e^{-ax^2} dx &= \int ^{\infty} _{0} x^2 e^{-ax^2} dx + \int ^{0} _{-\infty} x^2 e^{-ax^2} dx \\\\
  &= 2  \int ^{\infty} _{0} x^2 e^{-ax^2} dx \\\\
  \end{align}
\\]
から,
\\[
\int ^{\infty} _{0} x^2 e^{-ax^2} dx = \frac{1}{2} \int ^{\infty} _{-\infty} x^2 e^{-ax^2} dx = \frac{1}{4}\sqrt{\frac{\pi}{a^3}}
\\]
