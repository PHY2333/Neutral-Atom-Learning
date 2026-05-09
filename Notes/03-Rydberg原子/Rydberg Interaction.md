[[偶极-偶极相互作用]]哈密顿量涉及电偶极矩:
$$
	U=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}_{1}\cdot \mathbf{p}_{2}-3(\mathbf{p}_{1}\cdot \hat{\mathbf{r}})(\mathbf{p}_{2}\cdot \hat{\mathbf{r}})}{r^{3}}
$$
其中$r$是原子之间的距离，为经典参数不是算符
考虑两个Rydberg态直积$\ket{rr}$
由于$\bra{r} \hat{\mathbf{d}_{1,2}} \ket{r}$=0：
所以$\Delta E^{(1)}=\bra{rr} V_\text{dd} \ket{rr}=0$

偶极-偶极相互作用不能直接改变单个态$\ket{rr}$的能量，只能通过**非对角元**将 $|rr\rangle$ 耦合到其他宇称相反的态（例如 $|ab\rangle$）来改变能量。

>考虑双原子相互作用必须考虑多个态，而不是单个态

---
假设存在另一个双原子态$\ket{ab}$,和$\ket{rr}$通过 $V_{\text{dd}}$ 耦合。
这两个基底 $\{ |rr\rangle, |ab\rangle \}$ 下写出哈密顿量矩阵。
-  $|rr\rangle$ 的无微扰能量设为零点（参考点）：$E_{rr} = 2E_r \rightarrow 0$。
-  $|ab\rangle$ 的无微扰能量相对于 $|rr\rangle$ 就是：$E_a + E_b - 2E_r \equiv \hbar\Delta_F$,称为**Förster defect**。
- 两个态之间的耦合强度由偶极相互作用决定：$\langle rr | V_{\text{dd}} | ab \rangle = \hbar U(R)$。由于偶极场随距离的三次方衰减，所以 $U(R) = C_3 / R^3$。
哈密顿量为：
$$
	H=\hbar \begin{pmatrix}
	0 & U(R) \\
	U(R) & \Delta_{F}
	\end{pmatrix}
$$
求解本征值可得：
$$
	\frac{E_{\pm}}{\hbar}=\frac{\Delta_{F}}{2}\pm \frac{1}{2}\sqrt{ \Delta_{F}^{2}+4U(R)^{2} }
$$
---
### van der Waals相互作用
在**非共振或远距离**情形下，偶极耦合远小于能级失配：
$$
	|U(R)|\ll |\Delta_{F}|
$$
可以进行泰勒展开:
$$ |\Delta_F| \sqrt{1 + 4\left(\frac{U(R)}{\Delta_F}\right)^2} \approx |\Delta_F| \left[ 1 + \frac{1}{2} \cdot 4\left(\frac{U(R)}{\Delta_F}\right)^2 \right] = |\Delta_F| + \frac{2U(R)^2}{|\Delta_F|} $$

假设 $\Delta_F > 0$，得到与初始态 $|rr\rangle$连续相连的那个解（即取负号的那个根 $E_-$）：
$$ \frac{E_-}{\hbar} = \frac{\Delta_F}{2} - \frac{1}{2} \left( \Delta_F + \frac{2U(R)^2}{\Delta_F} \right) = -\frac{U(R)^2}{\Delta_F} $$
于是相互作用势能为：
$$ V(R) = \hbar \cdot \left( -\frac{(C_3/R^3)^2}{\Delta_F} \right) = -\frac{\hbar C_3^2}{\Delta_F} \frac{1}{R^6} $$
在远距离下，原本 $1/R^3$ 的偶极相互作用表现出了 $1/R^6$ 的范德华（van der Waals）形式。从微扰论的角度看，这就是标准的二阶微扰结果。

---
### 共振偶极-偶极相互作用(resonant dipole-dipole)
如果 $\Delta_F \approx 0$ （这是可以通过外加电场斯塔克效应调节原子能级来实现的，称为 Förster 共振），或者距离 $R$ 非常近导致 $|U(R)| \gg |\Delta_F|$。
此时，方程中的 $\Delta_F$ 项可以直接忽略：

$$ \frac{E_{\pm}}{\hbar} \approx \pm \frac{1}{2}\sqrt{0 + 4U(R)^2} = \pm |U(R)| $$
代入 $U(R) = C_3/R^3$：

$$ V(R) \approx \pm \frac{\hbar C_3}{R^3} $$
**物理图像：** 此时 $|rr\rangle$ 和 $|ab\rangle$ 完全简并，它们发生强烈的量子杂化，形成了对称与反对称叠加态 $(|rr\rangle \pm |ab\rangle)/\sqrt{2}$。相互作用能量不再是二阶的微扰移动，而是一阶的能级劈裂，因此表现为 $1/R^3$ 的共振偶极-偶极相互作用。