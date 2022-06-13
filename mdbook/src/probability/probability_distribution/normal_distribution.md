## 正規分布
Gauss分布とも言う.確率変数\\(X\\)が平均\\(\mu\\),分散\\(\sigma^2\\)の**正規分布**(normal distribution)に従うとは,確率変数\\(X\\)の確率密度関数が,
\\[
	f_X(x:\mu,\sigma^2) = \frac{1}{\sqrt{2\pi}\sigma} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2}\right), (x \in \overline{\mathbb{R}})
\\]
で与えられることであり,\\(\mathcal{N}(\mu,\sigma^2)\\)と表す.

### 平均
\\[
	E[X] = \int^{\infty}_{-\infty} \frac{x}{\sqrt{2\pi}\sigma} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2}\right) dx
\\]

\\(y=x-\mu\\)と変数変換する.
\\[
  \begin{align}
	\int ^{\infty} _{-\infty} \frac{x}{\sqrt{2\pi}\sigma} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2}\right) dx &= \int ^{\infty} _{-\infty} \frac{y+\mu}{\sqrt{2\pi}\sigma} \exp\left( -\frac{{y}^2}{2\sigma^2}\right) dy \\\\
	&= \frac{1}{\sqrt{2\pi}\sigma}\left( \int ^{\infty} _{-\infty} y \exp\left( -\frac{{y}^2}{2\sigma^2}\right) dy + \int ^{\infty} _{-\infty} \mu \exp\left( -\frac{{y}^2}{2\sigma^2}\right) dy\right)
  \end{align}
\\]

右辺第1項は\\(z=\frac{y}{\sqrt{2}\sigma}\\)と変数変換すると,\\(\frac{dz}{dy} = \frac{1}{\sqrt{2}\sigma}\\)から,
\\[
  \begin{align}
\int ^{\infty} _{-\infty} y \exp\left( -\frac{{y}^2}{2\sigma^2}\right) &= \int ^{\infty} _{-\infty} \sqrt{2}\sigma z \exp\left( -z^2 \right) \cdot \sqrt{2}\sigma \cdot dz \\\\
	&= 0
  \end{align}
\\]
最終式はガウス積分より得られる.

右辺第2項も同様に変数変換して,
\\[
  \begin{align}
\int ^{\infty} _{-\infty} \mu \exp\left( -\frac{{y}^2}{2\sigma^2}\right) &= \mu \int ^{\infty} _{-\infty}\exp\left( -z^2 \right) \cdot \sqrt{2}\sigma \cdot dz \\\\
	&= \mu \sigma \sqrt{2\pi} 
  \end{align}
\\]
から,
\\[
	E[X] = \int^{\infty} _{-\infty} \frac{x}{\sqrt{2\pi}\sigma} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2}\right) dx = \frac{1}{\sqrt{2\pi}\sigma} \cdot \mu \sigma \sqrt{2\pi} = \mu
\\]

### 分散
\\[
	E[(X-\mu)^2] = \int^{\infty}_{-\infty} \frac{(x-\mu)^2}{\sqrt{2\pi}\sigma} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2}\right) dx
\\]
\\(y=x-\mu\\)と変数変換すると,
\\[
  \begin{align}
	\int ^{\infty} _{-\infty} \frac{(x-\mu)^2}{\sqrt{2\pi}\sigma} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2}\right) dx &= \int ^{\infty} _{-\infty} \frac{y^2}{\sqrt{2\pi}\sigma} \exp\left( -\frac{y^2}{2\sigma^2}\right) dy \\\\
	&= \frac{1}{\sqrt{2\pi}\sigma} \frac{1}{2} \sqrt{\pi \cdot 8\sigma^6} \\\\
	&= \sigma^2
  \end{align}
\\]
