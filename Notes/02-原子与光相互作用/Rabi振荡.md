### 共振情形：绕赤道方向转动
当$\Delta=0$,$\boldsymbol{\Omega}_{\mathrm{eff}}=(\Omega \cos \phi,\Omega \sin \phi,0)$
旋转轴在Bloch赤道平面内,Bloch矢量绕轴旋转
[点击打开 Rabi 模拟器](<file:///D:/MyKnowledgeBase/Neutral Atom Vault/Code/Rabi振荡.html>)

---
### $\pi$脉冲
在共振情形下，且初态处在基态$\ket{g}$，旋转角度$\theta_{\mathrm{rot}}=\Omega t=\pi$时，
Bloch矢量从南极转到北极：$\ket{g}\to \ket{e}$

---
### $2\pi$脉冲
在共振情形下，且初态处在基态$\ket{g}$，旋转角度$\theta_{\mathrm{rot}}=\Omega t=2\pi$时，
Bloch 向量回到基态$\ket{g}$。
但注意：Bloch 向量看不见整体相位。
对于态矢量，自旋 $1/2$ 系统绕 Bloch 球转一圈会得到一个负号：
$$
	\ket{\psi} \to-\ket{\psi}
$$
这在单独二能级空间里是整体相位，不能观测；但如果系统还有一个旁观态，比如 Rydberg 门中的 $|0\rangle$，那么$\ket{0}$没有参与循环，而$\ket{1}$经历了 $2\pi$ 循环并获得 $-1$，这个负号就变成可观测的相对相位，这个效应用于构建里德堡CZ门。

---
### $\pi/2$脉冲
在共振情形下，且初态处在基态$\ket{g}$，旋转角度$\theta_{\mathrm{rot}}=\Omega t=\frac{\pi}{2}$时，
Bloch向量从南极转到赤道，也就是从$\ket{g}$制备叠加态
例如绕x轴：
$$
	\ket{g} \to \frac{\ket{g} -i\ket{e} }{\sqrt{ 2 }}
$$
---
### 失谐情形：旋转轴倾斜
如果$\Delta\neq 0$，则旋转角速度为$\Omega_{R}=\sqrt{ \Omega^{2}+\Delta^{2} }$,称为广义Rabi频率
在初态为$\ket{g}$的情况下，则
$$
	P_{e}(t)=\frac{\Omega^{2}}{\Omega^{2}+\Delta^{2}}\sin ^{2}\left( \frac{\sqrt{ \Omega^{2}+\Delta^{2} }}{2}t \right)
$$
失谐的结果：
- 旋转速度变大：$\Omega\to \sqrt{ \Omega^{2}+\Delta^{2} }$
- 最大激发概率小于1
失谐越大，旋转轴越接近z轴，布居转移越弱

图像：失谐导致光子能量不足或者过多，都会导致原子无法从基态$\ket{g}$完美激发到激发态$\ket{e}$

---
### 只有失谐，没有驱动
如果$\Omega=0$,而$\Delta \neq 0$，则Bloch矢量绕$z$轴旋转，这时布居保持不变，只改变相对相位

---
### [[AC Stark shift]]
