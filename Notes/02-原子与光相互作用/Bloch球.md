一个二能级体系的态矢量最普遍的形式是：
$$
	\ket{\psi} =\begin{bmatrix}
	e^{ -i\frac{\varphi}{2} }\cos \frac{\theta}{2} \\
	e^{ i\frac{\varphi}{2} }\sin \frac{\theta}{2}
	\end{bmatrix},\theta \in [0,\pi],\varphi \in[0,2\pi).
$$
密度矩阵为：
$$
	\rho=\ket{\psi} \bra{\psi} =\begin{bmatrix}
	\cos \frac{^{2}\theta}{2} & e^{ -i\varphi }\sin \frac{\theta}{2}\cos \frac{\theta}{2} \\
	e^{ i\varphi }\sin \frac{\theta}{2}\cos \frac{\theta}{2} & \sin \frac{^{2}\theta}{2}
	\end{bmatrix}=\frac{1}{2}(\boldsymbol{1}+\mathbf{r}\cdot\boldsymbol{\sigma})
$$
其中$\mathbf{r}=(\sin\theta \cos\varphi,\sin\theta \sin\varphi,\cos\theta)$.

---
$\mathbf{r}$的物理含义是$\boldsymbol{\sigma}$算子的期望：
$$
	\langle \sigma_{i} \rangle =\mathrm{Tr}(\rho\sigma_{i})=r_{i}
$$
---
### Bloch球内部的性质
$$
	\begin{aligned}
		\rho^{2}&=\frac{1}{4}\left( \mathbf{1}+2\mathbf{r}\cdot\boldsymbol{\sigma}+\sum \limits_{i,j}r_{i}r_{j}\sigma_{i}\sigma_{j} \right) \\
		&=\frac{1}{4}\left( \mathbf{1}+2\mathbf{r}\cdot\boldsymbol{\sigma}+\mathbf{r}^{2}+\sum \limits_{i\neq j}r_{i}r_{j}\sigma_{i}\sigma_{j} \right)
	\end{aligned}
$$
最后一项由Pauli算符反对易可知等于0.
$$
	\rho^{2}=\frac{1}{4}((1+\mathbf{r}^{2})\mathbf{1}+2\mathbf{r}\cdot\boldsymbol{\sigma})
$$
由$\mathrm{Tr}(\rho^{2})=\frac{1}{2}(1+\mathbf{r}^{2})\leq 1$可得：
$$
	|\mathbf{r}|\leq 1
$$
>也可以由半正定性得到相同结论