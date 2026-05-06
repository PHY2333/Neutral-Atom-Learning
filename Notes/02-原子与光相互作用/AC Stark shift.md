[[二能级系统]]等效哈密顿量为：
$$
	H_{\mathrm{eff}}=\frac{\hbar}{2}\begin{pmatrix}
	-\Delta & \Omega e^{ -i\phi } \\
	\Omega e^{ i\phi } & \Delta
	\end{pmatrix}
$$
求本征方程可以求得：
$$
	E_{\pm}=\pm \frac{\hbar}{2}\sqrt{ \Delta^{2}+\Omega^{2} }=\pm \frac{\hbar}{2}\Omega_{\mathrm{eff}}
$$
**有激光时 ($\Omega \neq 0$)**： 哈密顿量不再是对角矩阵。非对角项 $\Omega$ 把 $|g\rangle$ 和 $|e\rangle$ 耦合在了一起。此时，系统真实的能量本征态不再是 $|g\rangle$ 和 $|e\rangle$，而是它们的线性叠加。这种被光场“修饰”过的状态，被称为**缀饰态(Dressed States)** 。

**没有激光时**($\Omega=0$): 本征态称为裸态(Bare States)，能量为$E_{\pm}=\pm \frac{\hbar}{2}\Delta$

> 为什么仅仅是换了一个观察的坐标系，系统客观存在的能量差 $\hbar\omega_0$ 就凭空缩水成了 $\hbar\Delta$？能量守恒去哪了？ 
- 能量本质上是**相位随时间演化的速率**（$E = \hbar \frac{d\phi}{dt}$）。既然你在一个以 $\omega$ 旋转的坐标系里观察，原子相位的相对变化速率自然就只剩下 $\omega_0 - \omega$ 
- 我们在做幺正变换 $|\psi_{rot}\rangle = U(t)|\psi\rangle$ 时，有效哈密顿量多出了一项：
$$H_{rot} = U H_0 U^\dagger + \mathbf{i\hbar \dot{U}U^\dagger}$$
	由于坐标系本身带有时间依赖性，薛定谔方程强行给系统补偿了一个**负的能量项**。
- 在实验室里，原子从 $|g\rangle$ 跃迁到 $|e\rangle$，需要获得 $\hbar\omega_0$ 的能量。这个能量从吸收激光的一个光子 $\hbar\omega$ 来。假设激光场是一个频率为 0 的静电场（因为在 $\omega$ 旋转系里，频率为 $\omega$ 的光就变成静止的了），作为交换，我们把光子的能量 $\hbar\omega$ 直接“提前支付”给了原子。裸态之间的能量差变成 $\Delta$，并不是原子的物理结构发生了改变，而是我们**把驱动场的能量吸收到原子的定义中去了**。


---
### 远失谐近似
假设$|\Delta|\gg \Omega$，$E_{\pm}$可以泰勒展开:
$$
	E_{\pm}=\pm \frac{\hbar |\Delta|}{2}\sqrt{ 1+\left( \frac{\Omega}{\Delta} \right)^{2} }\approx\pm \frac{\hbar |\Delta|}{2}\left[ 1+\frac{1}{2}\left( \frac{\Omega}{\Delta} \right)^{2} \right]
$$
与裸态相比，尽管激光与原子几乎没有耦合，原子几乎不会跃迁，但是激光的存在本身，导致原子之间的能级排斥,能量变化量就是AC Stark shift:
$$
	\delta E=\frac{\hbar \Omega^{2}}{4\Delta}
$$
---
在量子力学中，这是一个普遍规律：**当两个能级被某种相互作用（这里是 $\Omega$）耦合时，它们总是倾向于互相排斥**。

- 基态能量会向下沉一点（更稳定）。
    
- 激发态能量会向上翘一点。
    推开的幅度，与耦合强度平方（光强 $\propto \Omega^2$）成正比，与能级原本的距离（失谐 $\Delta$）成反比。
---
### 光镊的原理
极度红失谐($\Delta< 0$且远失谐)可以保证不影响原子的态布居，同时由于原子感受到负的光位移，这时激光焦点中心$\Omega$最大，势能最低，这就是偶极阱