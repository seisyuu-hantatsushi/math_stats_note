## Fubiniの定理
1. \\(f: X _1 \times X _2 \mapsto \overline{\mathbb{R} _{+}} \\)を\\(\mathcal{F} _{X _1} \times \mathcal{F} _{X _2}\\)可測関数とする時,
   \\[
   F_1(x _1) = \int _{X _2} f(x _1,x _2)m _2 (dx_2), F_2(x _2) = \int _{X _1} f(x _1,x _2)m _1 (dx _1)
   \\]
   \\(F_1(x _1),F_2(x _2)\\)は,ぞれぞれ\\(\mathcal{F} _{X _1}, \mathcal{F} _{X _2}\\)可測で,

	\\[
	\begin{align}
	\iint _{X _1 \times X _2} f(x _1,x _2) (m _1 \times m _2)(dx_1,dx_2) &= \int _X \left(\int _Y f(x _1, x _2) m_2(dx_2)\right) m_1(dx_1) \\\\
	&= \int _Y \left(\int _X f(x _1, x _2) m_1(dx_1)\right) m_2(dx_2)
	\end{align}
	\\]
1. \\(f: X _1 \times X _2 \mapsto \overline{\mathbb{R}} \\)が\\(\mathcal{F} _{X _1} \times \mathcal{F} _{X _2}\\)可積分ならば,\\(m _1\\)が\\(x\\)で概収束するなら,\\(f(x,y)\\)は\\(m _2\\)可積分,\\(m _2\\)が\\(y\\)で概収束するなら,\\(f(x,y)\\)は\\(m _1\\)可積分である.さらに,
   \\[
   F_1(x _1) = \int _{X _2} f(x _1,x _2)m _2 (dx_2), F_2(x _2) = \int _{X _1} f(x _1,x _2)m _1 (dx _1)
   \\]
	\\[
	\begin{align}
	\iint _{X _1 \times X _2} f(x _1,x _2) (m _1 \times m _2)(dx_1,dx_2) &= \int _X \left(\int _Y f(x _1, x _2) m_2(dx_2)\right) m_1(dx_1) \\\\
	&= \int _Y \left(\int _X f(x _1, x _2) m_1(dx_1)\right) m_2(dx_2)
	\end{align}
	\\]
