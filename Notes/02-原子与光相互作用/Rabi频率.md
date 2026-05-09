电偶极相互作用只保留$\ket{e},\ket{g}$两个态，关键矩阵元是：
$$
	\mathbf{d}_{eg}=\bra{e} \hat{\mathbf{d}}\ket{g}
$$
光场偏振方向记为$\boldsymbol{\epsilon}$，电场为：
$$
	\mathbf{E}(t)=E_{0}\boldsymbol{\epsilon}\cos(\omega t+\phi)=\frac{E_{0}}{2}\boldsymbol{\epsilon}[e^{ i(\omega t+\phi) }+e^{ -i(\omega t+\phi) }]
$$
$\hat{H}_{\mathrm{int}}=-\hat{\mathbf{d}}\cdot \mathbf{E}(t)$
则跃迁偶极矩在光场偏振方向上的投影$\mathbf{d}_{eg}\cdot\boldsymbol{\epsilon}$给出了Rabi频率：
$$
	\Omega=-\frac{\mathbf{d}_{eg}\cdot\boldsymbol{\epsilon}}{\hbar}E_{0}
$$
>对于二能级系统讨论不必使用复杂度任意偏振，因为强行引入任意偏振，只会引入$\mathbf{d}$和$\mathcal{E}$的夹角因子$\cos\theta$,影响$\Omega$的大小(偏振失配)。而实验中会避免这种情况发生(见[[半经典光-原子相互作用]]中电偶极矩方向的确定)

---
### 相互作用哈密顿量
$$
\begin{aligned}
	\hat{H}_{\mathrm{int}}&=-\mathbf{d}_{eg}\cdot \mathbf{E}(t)\ket{e} \bra{g} - \mathbf{d}_{ge}\cdot \mathbf{E}(t)\ket{g} \bra{e} \\
	&=\hbar \Omega \cos(\omega t+\phi)\ket{e} \bra{g} +\hbar \Omega^{*}\cos(\omega t+\phi)\ket{g} \bra{e} 
\end{aligned}
$$
所以
$$
	\hat{H}_{\mathrm{int}}=\begin{pmatrix}
	0 & \hbar \Omega \cos(\omega t+\phi) \\
	\hbar \Omega^{*}\cos(\omega t+\phi) & 0
	\end{pmatrix}
$$
---
### Rabi频率的规范自由度
在绝大多数情况下（包括标准的二能级系统以及研究的里德堡原子的树状激发），把 $\Omega$ 当作纯实数处理在物理上是完全没有关系的。

对于Rabi频率的定义:$\Omega=|\Omega|e^{ i\theta_{d} }$
[[二能级系统]]代入RWA后的$H_{\mathrm{int}}^{\mathrm{RWA}}=\frac{\hbar}{2}(\Omega e^{ -i\phi }\ket{e} \bra{g}+\Omega ^{*}\ket{g} \bra{e})$
>偶极矩阵元的内在相位$\theta_{d}$仅仅是给激光相位$\phi$增加了一个常数

物理上更严谨的操作是重新定义激发态的相位（规范变换）:
$$
	\ket{e'} =e^{ i\theta_{d} }\ket{e}
$$
$$
	\Omega'=-\frac{\mathbf{d}_{e'g}\cdot\boldsymbol{\epsilon}}{\hbar}E_{0}=\Omega e^{ -i\theta_{d} }=|\Omega|
$$
$\Omega$变成一个纯实数，为了方便计算，总是默认已经吸收过相位

但是$\Omega$的复数性没有物理意义吗？
>在闭环跃迁系统中会展现出真实的、不可消除的物理效应——[[AB效应]]

如果研究的不只是$\ket{g}\to \ket{e}$或者里德堡原子中的$\ket{g}\to \ket{e}\to \ket{r}$，而是存在一个闭合回路，比如微波驱动的三能级系统($\Delta$构型)：
- 激光1驱动$\ket{1}\leftrightarrow \ket{2}$,Rabi频率为$\Omega_{12}$
- 极光2驱动$\ket{2}\leftrightarrow \ket{3}$,Rabi频率为$\Omega_{23}$
- 激光3驱动$\ket{3}\leftrightarrow \ket{1}$,Rabi频率为$\Omega_{31}$
利用$\ket{2}$的相位可以让$\Omega_{12}$变实，锁定$\ket{1}$的相位，同理锁定$\ket{3}$相位让$\Omega_{23}$变实，但是$\Omega_{31}$的相位不能通过规范变换消除

在这个系统中，三个复Rabi频率相乘的相位:
$$
	\Phi_{\mathrm{loop}}=\mathrm{arg}(\Omega_{12}\Omega_{23}\Omega_{31})
$$
是一个规范不变量，它等价于电子在磁场中运动时积累的AB相位。而在中性原子中可以利用这个规范不变量，创造出[[合成规范场]](Synthetic Gauge Fields)。

