考虑两个原子，暂时忽略$\ket{0}$，只看参与Rydberg激发的子空间：
$$
	\ket{11} ,\ket{r_{1}} ,\ket{1r} ,\ket{rr}
$$
经过旋波近似和坐标系旋转，两原子哈密顿量可以写成：
$$
	\frac{H}{\hbar}=\sum \limits_{i=1}^{2}\left[ -\delta \ket{r_{i}} \bra{r_{i}} +\frac{\Omega}{2}(\ket{r_{i}} \bra{1_{i}} +\ket{1_{i}} \bra{r_{i}} ) \right]+B(R)\ket{rr} \bra{rr}
$$
其中$B(R)=\frac{V(R)}{\hbar}$，可以是van der Waals型，也可以是resonant dipole-dipole型。
对角项$\ket{rr} \bra{rr}$不含时间是因为旋转不影响对角项。

在基底$\{\ket{11},\ket{r_{1}},\ket{1r},\ket{rr}\}$下，哈密顿量为：
$$
	\frac{H}{\hbar}=\begin{pmatrix}
	0 & \Omega/2 & \Omega/2 & 0 \\
	\Omega/2 & -\delta & 0 & \Omega/2 \\
	\Omega/2 & 0 & -\delta & \Omega/2 \\
	0 & \Omega/2 & \Omega/2 & B-2\delta
	\end{pmatrix}
$$
本质是$\ket{rr}$的能量被相互作用移动了。

---
### 暗态$\ket{D}$
驱动原子的跃迁部分是：
$$
	\hat{V_{L}}=\frac{\Omega}{2}(\ket{r_{1}} \bra{1_{1}} +\ket{r_{2}} \bra{1_{2}} )+\text{h.c.}
$$
计算从$\ket{11}$跃迁到反对称态$\ket{D}=\frac{1}{\sqrt{ 2 }}(\ket{r1}-\ket{1r})$的概率幅：
$$
	\bra{D} \hat{V}_{L} \ket{11} =\frac{1}{\sqrt{ 2 }}(\bra{r1}-\bra{1r}  )\left[ \frac{\Omega}{2}(\ket{r1}+\ket{1r}  ) \right]=0
$$
因为激光无法将布居数打入这个状态，所以它被称为**暗态（Dark State）**。在哈密顿量中它可以被完全剔除，所以 $4 \times 4$ 的矩阵可以降维成 $3 \times 3$。

### 亮态$\ket{W}$
同理计算对称态$\ket{W}$的跃迁概率幅：
$$
	\bra{W} \hat{V_{L}} \ket{11} =\frac{1}{\sqrt{ 2 }}(\bra{r1}+\bra{1r}  )\left[ \frac{\Omega}{2}(\ket{r1}+\ket{1r}  ) \right]=\frac{\Omega}{\sqrt{ 2 }}
$$
在标准的二能级系统矩阵中，非对角元写作 $\Omega/2$ 时，对应的拉比振荡频率是 $\Omega$。现在我们的非对角元变成了 $\Omega/\sqrt{2}$，这相当于原来的 $\sqrt{2}$ 倍。因此，系统的等效拉比频率就是 $\sqrt{2}\Omega$。

>有意思的一点是，如果有$N$个原子，会增强为$\sqrt{ N }\Omega$，有一个多体加速。本质是到达对称态的多条路径可以相干叠加。

---
### 重构后的矩阵
以$\{\ket{11},\ket{W},\ket{rr}\}$为新基底，重写哈密顿量
$$
	\frac{H}{\hbar}=\begin{pmatrix}
	0 & \Omega/\sqrt{ 2 } & 0 \\
	\Omega/\sqrt{ 2 } & -\delta & \Omega/\sqrt{ 2 } \\
	0 & \Omega/\sqrt{ 2 } & B-2\delta
	\end{pmatrix}
$$
---
### 理想Rydberg Blockade
若$\delta=0$，则$\ket{11}$和$\ket{W}$共振Rabi振荡，而$\ket{rr}$的能量为$\hbar B$
如果
$$
	|B|\gg \Omega
$$
那么$\ket{W}\to \ket{rr}$这一步强失谐，几乎不会跃迁到这个态上，这时我们可以进行绝热消除，这一点在远失谐Raman跃迁提到过。
设$\ket{\psi}=c_{g}\ket{11}+c_{W}\ket{W}+c_{rr}\ket{rr}$，运动方程为：
$$
	\begin{aligned}
		i \dot{c}_{g}&=\frac{\Omega}{\sqrt{ 2 }}c_{W} \\
		i \dot{c}_{W}&=\frac{\Omega}{\sqrt{ 2 }}c_{g}+\frac{\Omega}{\sqrt{ 2 }}c_{rr} \\
		i \dot{c}_{rr}&=\frac{\Omega}{\sqrt{ 2 }}c_{W}+Bc_{rr}
	\end{aligned}
$$
当$|B|\gg \Omega$时，$\ket{rr}$是快变量，$\dot{c}_{rr}=0$
$$
	c_{rr}=-\frac{\Omega}{\sqrt{ 2 }B}c_{W}
$$
双激发概率大约是：
$$
	P_{rr}\sim\left( \frac{\Omega}{B} \right)^{2}
$$
如果考虑线宽，还需要$|B|\gg \Gamma$.