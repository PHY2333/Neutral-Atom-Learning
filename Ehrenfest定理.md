期望值$\langle A \rangle$的演化有两种方式得到：

---
方式一：利用薛定谔方程直接推导
$$
	\frac{d}{dt} \langle A \rangle (t)=\frac{d}{dt} \bra{\psi(t)} A(t) \ket{\psi(t)} =\left\langle  \frac{ \partial A }{ \partial t }   \right\rangle +\frac{1}{i\hbar}\langle [A,H] \rangle 
$$

---
方式二：利用经典对应
$$
\begin{aligned}
	\frac{d}{dt} A&=\frac{ \partial A }{ \partial t } +\frac{ \partial A }{ \partial q } \frac{\mathrm{d} q}{\mathrm{d} t} +\frac{ \partial A }{ \partial p } \frac{\mathrm{d} p}{\mathrm{d} t} \\
	&=\frac{ \partial A }{ \partial t } +\left( \frac{ \partial A }{ \partial q } \frac{ \partial H }{ \partial p } -\frac{ \partial A }{ \partial p } \frac{ \partial H }{ \partial q }  \right) \\
	&=\frac{ \partial A }{ \partial t } +\{A,H\}
\end{aligned}
$$
利用$\{~,~\}_{\mathrm{CM}}\leftrightarrow \frac{1}{i\hbar}[~,~]_{\mathrm{QM}}$，可以得到
$$
	\frac{d}{dt} \langle A \rangle (t)=\left\langle  \frac{ \partial A }{ \partial t }   \right\rangle +\frac{1}{i\hbar}\langle [A,H] \rangle 
$$

---
### 自旋进动
$$
	H=\boldsymbol{\omega} \cdot \mathbf{S}
$$
$$
	\frac{d}{dt} \langle S_{i} \rangle=\frac{1}{i\hbar}\langle [S_{i},\omega_{j}S_{j}] \rangle  =\langle \omega_{j}\epsilon_{ijk}S_{k} \rangle =[\boldsymbol{\omega}\times \langle \mathbf{S} \rangle ]_{i}
$$
用Pauli矩阵表达就是：
$$
	\frac{d}{dt} \langle \sigma_{i} \rangle =[\boldsymbol{\omega}\times \langle \boldsymbol{\sigma} \rangle ]_{i}
$$
