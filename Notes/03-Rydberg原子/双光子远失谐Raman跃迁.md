[[阶梯型三能级系统]]大失谐条件为：单光子失谐远大于耦合强度和双光子失谐，双光子失谐比较小$\delta \approx 0$
$$
	|\Delta|\gg \Omega_{1},\Omega_{2},|\delta|
$$
---
### 绝热消除
由于激发的能量缺口 $\hbar\Delta$ 极大，原子要真实地跃迁到中间态 $|2\rangle$ 需要违背能量守恒。因此，中间态只作为一个极短寿命的“虚态”（Virtual State）参与过程，其布居数 $|c_2|^2$ 始终保持在接近 $0$ 的极低水平。这叫做绝热消除，下面是两种得到绝热消除的方法：
#### 1.微分方程直接绝热消除
设态矢量$\ket{\psi(t)}=(c_{1},c_{2},c_{3})^{\mathrm{T}}$
$$
	i\hbar \frac{ \partial  }{ \partial t } \begin{pmatrix}
	c_{1} \\
	c_{2} \\
	c_{3} \\
	\end{pmatrix}=\hbar \begin{pmatrix}
	0 & 0 & \Omega_{1}^{*}/2 \\
	0 & -\delta & \Omega_{2}/2 \\
	\Omega_{1}/2 & \Omega_{2}^{*}/2 & -\Delta
	\end{pmatrix}\begin{pmatrix}
	c_{1} \\
	c_{2} \\
	c_{3}
	\end{pmatrix}
$$
$$
\begin{aligned}
	i \dot{c_{1}}&=\frac{\Omega_{1}^{*}}{2}c_{3} \\
	i \dot{c_{2}}&=-\delta c_{2}+\frac{\Omega_{2}}{2}c_{3} \\
	i \dot{c_{3}}&=\frac{\Omega_{1}}{2}c_{1}+\frac{\Omega_{2}^{*}}{2}c_{2}-\Delta c_{3}
\end{aligned}
$$
由于$\Delta$很大，导致$c_{3}(t)$包含一个频率极高的振荡项$e^{ -i\Delta t }$，因此在慢演化的时间尺度上，$c_{3}$是几乎不变的，可以令$\dot{c_{3}}=0$
$$
	c_{3}=\frac{\Omega_{1}}{2\Delta}c_{1}+\frac{\Omega_{2}^{*}}{2\Delta}c_{2}
$$
代入前两个方程
$$
	\begin{aligned}
		i \dot{c_{1}}&=\frac{\Omega_{1}^{*}}{2}\left( \frac{\Omega_{1}}{2\Delta}c_{1}+\frac{\Omega_{2}^{*}}{2\Delta}c_{2} \right)=\frac{|\Omega_{1}|^{2}}{4\Delta}c_{1}+\frac{\Omega_{1}^{*}\Omega_{2}^{*}}{4\Delta}c_{2} \\
		i \dot{c_{2}}&=-\delta c_{2}+\frac{\Omega_{2}}{2}\left( \frac{\Omega_{1}}{2\Delta}c_{1}+\frac{\Omega_{2}^{*}}{2\Delta}c_{2} \right)=\frac{\Omega_{1}\Omega_{2}}{4\Delta}c_{1}+\left( \frac{|\Omega_{2}|^{2}}{4\Delta}-\delta \right)c_{2}
	\end{aligned}
$$
大失谐Raman跃迁的有效哈密顿量为：
$$
	H_{\mathrm{eff}}=\hbar\begin{pmatrix}
	\frac{|\Omega_{1}|^{2}}{4\Delta} & \frac{\Omega_{1}^{*}\Omega_{2}^{*}}{4\Delta} \\
	\frac{\Omega_{1}\Omega_{2}}{4\Delta} & -\delta+\frac{|\Omega_{2}|^{2}}{4\Delta}
	\end{pmatrix}
$$
#### 2. Schrieffer-Wolff (SW) 变换
懒得写了，杀鸡焉用牛刀

---
### 有效哈密顿量的物理意义
之前在[[AC Stark Shift]]中的等效哈密顿量为：
$$
	H_{\mathrm{eff}}=\frac{\hbar}{2}\begin{pmatrix}
	-\Delta & \Omega e^{ -i\phi } \\
	\Omega e^{ i\phi } & \Delta
	\end{pmatrix}
$$
这个哈密顿量是无迹的，代表没有全局相位演化。
现在先要**把$H_{\mathrm{eff}}$变成无迹的**
$$
	\mathrm{Tr}(H_{\mathrm{eff}})=\hbar\left( \frac{|\Omega_{1}|^{2}+|\Omega_{2}|^{2}}{4\Delta}-\delta \right)
$$
变成无迹后：
$$
	H_{\mathrm{eff}}=\frac{\hbar}{2}\begin{pmatrix}
	\delta+\frac{|\Omega_{1}|^{2}-|\Omega_{2}|^{2}}{4\Delta} & \Omega ^{*} \\
	\Omega & -\delta-\frac{|\Omega_{1}|^{2}-|\Omega_{2}|^{2}}{4\Delta}
	\end{pmatrix}
$$
其中（新的Rabi频率）**有效双光子Rabi频率**为：
$$
\Omega=\frac{\Omega_{1}\Omega_{2}}{2\Delta}
$$
定义不对称光频移为：
$$
	\Delta_{AC}=\frac{|\Omega_{1}|^{2}-|\Omega_{2}|^{2}}{4\Delta}
$$
如果双束激光的光强或偶极矩不相等（即 $\Omega_1 \neq \Omega_2$），必然导致 $\Delta_{AC} \neq 0$。此时，即便我们在外部将双光子频率严格对齐到原子的裸能级间距（即设置外部失谐 $\delta = 0$），哈密顿量中依然会顽固地存在一个**残余的 $\sigma_z$ 项**：$\frac{\hbar}{2} \Delta_{AC} \sigma_z$。进而会引入额外的相位误差和布居转移小于1。

>也就是说真正的双光子共振依赖于$\delta=-\Delta_{AC}$

---
### 对应的Rabi振荡
$$
	H_{\mathrm{eff}}=\frac{\hbar}{2}\begin{pmatrix}
	\delta_{\mathrm{eff}} & \Omega ^{*} \\
	\Omega & -\delta_{\mathrm{eff}}
	\end{pmatrix}
$$
广义Rabi频率为：
$$
	\Omega_{\mathrm{gen}}=\sqrt{ |\Omega|^{2}+\delta_{\mathrm{eff}}^{2} }
$$
$$
	P_{g\to r}(t)=\frac{|\Omega|^{2}}{\Omega_{\mathrm{gen}}^{2}}\sin ^{2}\left( \frac{\Omega_{\mathrm{gen}}}{2}t \right)
$$
当满足有效两光子共振时：
$$
	\delta_{\mathrm{eff}}=0
$$
$\pi$脉冲时间为：
$$
	t_{\pi}=\frac{2\pi |\Delta|}{|\Omega_{1}||\Omega_{2}|}
$$
这说明一个重要权衡：
- 增大 $|\Delta|$ 可以减少中间态布居；
- 但在光强固定时，会减小有效 Rabi 频率；
- 因此跃迁速度会变慢。
---
### 两光子动量
两光子动量转移为：
$$
	\Delta \mathbf{k}=\mathbf{k}_{1}+\mathbf{k}_{2}
$$
如果两束光反向传播，其中一个 $\mathbf k$ 本身就是负方向，因此可以通过几何安排减小或增大有效动量转移。