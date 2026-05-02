原子能级在外磁场中发生分裂，本质是
$$
	\hat{H}_{Z}=-\boldsymbol{\mu}\cdot \mathbf{B}
$$
打破了原子哈密顿量的球对称性，$\boldsymbol{\mu}=\boldsymbol{\mu}_{L}+\boldsymbol{\mu}_{S}$。
$$
	\boldsymbol{\mu}_{L}=-\mu_{B} \frac{\mathbf{L}}{\hbar},
	\boldsymbol{\mu}_{S}=-g_{s}\mu_{B} \frac{\mathbf{S}}{\hbar}
$$
其中$\mu_{B}=\frac{e\hbar}{2m_{e}}$，叫做[[玻尔磁子]]。

---
### 1.弱磁场下$J$仍然是好量子数

$$
	H_{Z}\ll H_{\mathrm{fs}}
$$
这时适合使用LS耦合，本征矢为$\ket{L,S,J,M_{J}}$
$$
	\Delta E=\mu_{B}g_{J}M_{J}B
$$
$g_{J}$是[[Lande g因子]]。
其中
$$
	g_{J}=g_{L} \frac{J(J+1)+L(L+1)-S(S+1)}{2J(J+1)}+g_{S}\frac{J(J+1)-L(L+1)+S(S+1)}{2J(J+1)}
$$

这个朗德g因子公式只在轻原子，弱磁场的情况下成立，因为这个时候才算LS耦合，jj耦合的因子需要另外计算。

___
### 2.正常Zeeman效应:选择定则导致一条谱线分裂成三条
$S=0$的弱塞曼效应就是正常塞曼效应。$J=L$。
则
$$
	\Delta \nu=\frac{\mu_{B}B}{h}\Delta M
$$
由于[[选择定则]]，电偶极跃迁$\Delta M=0,\pm 1$。
比如从原来的一个能级跳到另一个能级，这两个能级都会分裂成很多子能级，但是在正常塞曼效应中，频移只取决于$\Delta M$，所以只会分裂成三条谱线,且这三条谱线分别为$\pi,\sigma^{+},\sigma^{-}$偏振（这一点也可以看[[选择定则]]）。

---
### 3.反常Zeeman效应为什么不止三条
是因为上能级和下能级的Laude g因子不同
$$
	\Delta \nu=\frac{\mu_{B} B}{h}(g_{J_{1}}M_{1}-g_{J_{2}}M_{2})
$$
选择定则虽然保证$\Delta M=M_{2}-M_{1}=0,\pm 1$，但是不同跃迁不能再简单合并成三组。

---
### 4.强磁场：Paschen-Back效应
磁场很强的情况下：
$$
	H_{Z}≳H_{SO}
$$
外磁场对$L$和$S$的作用已经可以和LS耦合相比甚至更强，好的量子数为:$M_{L},M_{S}$。
$$
	\Delta E=\mu_{B}B(M_{L}+g_{s}M_{S})
$$
