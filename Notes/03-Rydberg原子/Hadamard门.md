[点击打开Hadmard门演示](<../../Code/Hadamard门.html>)
中性原子一般直接驱动两个超精细能级之间的Rabi振荡。
在旋转坐标系下，二能级驱动哈密顿量：
$$
	\boldsymbol{\Omega}_{\mathrm{eff}}=(\Omega \cos \phi,\Omega \sin \phi,-\Delta)
$$
$$
	\hat{H}_{\mathrm{eff}}=\frac{\hbar}{2}\boldsymbol{\Omega}_{\mathrm{eff}}\cdot\boldsymbol{\sigma}
$$
在共振情形下，写出演化算符$U=e^{ -i Ht/\hbar }$：
$$
	U(\theta,\phi)=\exp\left[ -\frac{i\theta}{2}(\cos \phi X+\sin \phi Y) \right]
$$
其中$\theta=\int \Omega(t) dt$

利用矩阵指数的欧拉公式：
$$
	e^{ i\theta A }=\cos\theta I+i\sin\theta A,A^{2}=I
$$
则
$$
	U(\theta,\phi)=\cos\left( \frac{\theta}{2} \right)I-i\sin\left( \frac{\theta}{2} \right)(\cos \phi X+\sin \phi Y)
$$
Hadamard门要把$\ket{0}$转到$\ket{+}$，Bloch矢量需要绕Y轴转$\frac{\pi}{2}$，令$\theta=\frac{\pi}{2},\phi=\frac{\pi}{2}$：
$$
	R_{y}\left( \frac{\pi}{2} \right)=\cos\left( \frac{\pi}{4} \right)I-i\sin\left( \frac{\pi}{4} \right)Y=\frac{1}{\sqrt{ 2 }}\begin{pmatrix}
	1 & -1  \\
	1 & 1
	\end{pmatrix}
$$
但是这不足以得到Hadmard门，我们还需要一个virtual z门，来实现对任意态的Hadamard门。virtual的含义是虚拟的，即不会真的进行操作，而是在软件上通过修改所有后续激光的相位来实现：
$$
	R_{z}(\alpha)(\cos \phi X+\sin \phi Y)R_{z}^{\dagger}(\alpha)=\cos(\phi-\alpha)X+\sin(\phi-\alpha)Y
$$
取$\alpha =\pi$，可以得到：
$$
	R_{y}\left( \frac{\pi}{2} \right)R_{z}(\pi)=-i\left[ \frac{1}{\sqrt{ 2 }}\begin{pmatrix}
	1 & 1 \\
	1 & -1
	\end{pmatrix} \right]
$$
即$H \dot{=}R_{y}\left( \frac{\pi}{2} \right)R_{z}(\pi)$。

