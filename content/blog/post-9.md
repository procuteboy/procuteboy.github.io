---
math: true
---

实现Caldeira-Leggett模型的量子场论形式：分步骤解析

Caldeira-Leggett（CL）模型是研究量子耗散系统的经典框架，其核心思想是通过将主系统与一个由无穷多谐振子组成的热浴耦合，描述耗散和量子涨落。在量子场论中，这一模型可推广为场与场的耦合，热浴由连续的自由度（场模式）表示。以下是其量子场论形式的具体实现步骤：

---

**步骤1：定义系统与热浴的场论自由度**
目标：明确主系统和热浴的场论表示。

1. 主系统  
   主系统可以是局域自由度（如粒子坐标\(X(t)\)）或一个量子场。为简化，假设主系统为单个粒子的位置\(X(t)\)，其作用量为：
   \[
   S_{\text{sys}} = \int dt \, \left( \frac{m}{2} \dot{X}^2 - V(X) \right),
   \]
   其中\(V(X)\)为势能。

2. 热浴场  
   热浴由无穷多自由度的标量场\(\phi(x,t)\)描述（例如一维场，\(x \in \mathbb{R}\)），其作用量为：
   \[
   S_{\text{bath}} = \int dt \int dx \, \left( \frac{1}{2} (\partial_t \phi)^2 - \frac{1}{2} (\partial_x \phi)^2 - \frac{\omega_0^2}{2} \phi^2 \right),
   \]
   其中\(\omega_0\)为场的内禀频率（可选为零，对应无质量场）。

---

**步骤2：引入线性耦合项**
目标：建立主系统与热浴场的相互作用。

1. 线性耦合作用量  
   假设主系统与热浴场在时空某点（如\(x=0\)）线性耦合：
   \[
   S_{\text{int}} = \int dt \, \lambda X(t) \phi(0, t),
   \]
   其中\(\lambda\)为耦合常数，描述相互作用强度。

2. 总作用量  
   完整的作用量为：
   \[
   S_{\text{total}} = S_{\text{sys}} + S_{\text{bath}} + S_{\text{int}}.
   \]

---

**步骤3：路径积分量化与积分出热浴场**
目标：通过路径积分消去热浴自由度，得到主系统的有效动力学。

1. 路径积分表达式  
   系统的配分函数为：
   \[
   Z = \int \mathcal{D}X \mathcal{D}\phi \, e^{i S_{\text{total}}/\hbar}.
   \]

2. 高斯积分消去热浴场  
   热浴场\(\phi(x,t)\)的作用量是二次型，可通过高斯积分精确积分：
   \[
   Z = \int \mathcal{D}X \, e^{i S_{\text{sys}}/\hbar} \cdot \left\langle e^{i \int dt \, \lambda X(t) \phi(0,t)/\hbar} \right\rangle_{\text{bath}}.
   \]
   其中\(\langle \cdot \rangle_{\text{bath}}\)为热浴场的自由路径积分期望值。

3. 生成热浴关联函数  
   展开耦合项至二阶（弱耦合近似）：
   \[
   \left\langle e^{i \int \lambda X \phi \, dt} \right\rangle_{\text{bath}} \approx e^{-\frac{\lambda^2}{2\hbar^2} \iint dt dt' X(t) X(t') \langle \phi(0,t)\phi(0,t') \rangle}.
   \]
   热浴场的两点关联函数\(\langle \phi(0,t)\phi(0,t') \rangle\)由自由场理论计算。

---

**步骤4：计算热浴格林函数**
目标：确定热浴场的推迟格林函数（响应函数）和涨落关联函数。

1. 自由场传播子  
   对于无质量场（\(\omega_0=0\)），其传播子在频率空间为：
   \[
   G_R(\omega) = \frac{1}{\omega^2 - k^2 + i \epsilon},
   \]
   在实空间中的推迟格林函数为：
   \[
   G_R(t-t') = \int \frac{d\omega}{2\pi} \frac{e^{-i\omega(t-t')}}{\omega^2 - k^2 + i \epsilon}.
   \]

2. 涨落-耗散定理  
   热平衡下，涨落关联函数与推迟格林函数满足：
   \[
   \langle \phi(0,t)\phi(0,t') \rangle = \int \frac{d\omega}{2\pi} \text{Im}[G_R(\omega)] \coth\left( \frac{\hbar \omega}{2k_B T} \right) e^{-i\omega(t-t')}.
   \]

---

**步骤5：导出有效郎之万方程**
目标：通过变分法或运动方程得到主系统的耗散动力学。

1. 有效作用量  
   积分出热浴场后，主系统的有效作用量为：
   \[
   S_{\text{eff}} = S_{\text{sys}} - \frac{\lambda^2}{2} \iint dt dt' X(t) K(t-t') X(t'),
   \]
   其中核函数\(K(t-t') = \text{Im}[G_R(t-t')]\)包含耗散和记忆效应。

2. 运动方程  
   对\(S_{\text{eff}}\)变分，得到广义郎之万方程：
   \[
   m \ddot{X}(t) + \frac{\partial V}{\partial X} + \lambda^2 \int_{-\infty}^t \text{Im}[G_R(t-t')] X(t') dt' = \xi(t),
   \]
   其中随机力\(\xi(t)\)满足：
   \[
   \langle \xi(t)\xi(t') \rangle = \lambda^2 \text{Re}[G_R(t-t')] \coth\left( \frac{\hbar \omega}{2k_B T} \right).
   \]

---

**步骤6：量子耗散与涨落的谱分解**
目标：在频率空间分析耗散和涨落性质。

1. 耗散核的谱密度  
   定义谱密度\(J(\omega) = \lambda^2 \text{Im}[G_R(\omega)]\)，耗散核的傅里叶变换为：
   \[
   \gamma(\omega) = J(\omega)/\omega.
   \]

2. 量子涨落耗散定理  
   随机力的噪声谱满足：
   \[
   \langle \xi(\omega)\xi(\omega') \rangle = 2\pi \delta(\omega+\omega') \, \hbar \omega \, \gamma(\omega) \coth\left( \frac{\hbar \omega}{2k_B T} \right).
   \]

---

**物理意义与关键结论**
1. 场论热浴的优势  
   场论形式自然包含连续谱的耗散模式，避免离散谐振子的人为截断，适用于非马尔可夫动力学。

2. 紫外发散与重整化  
   若热浴场无质量（如\(J(\omega) \propto \omega^d\)），高频模式可能导致发散，需引入截断或重整化条件。

3. 全息对偶的对应  
   在AdS/CFT框架中，AdS内部的引力场可视为热浴场的全息对偶，边界系统的耗散由AdS黑洞的准正则模决定。

---

**关键公式总结**
| 物理量                | 表达式                                                                 |
|-----------------------|----------------------------------------------------------------------|
| 有效作用量            | \(S_{\text{eff}} = S_{\text{sys}} - \frac{\lambda^2}{2} \iint X(t) K(t-t') X(t') dt dt'\) |
| 耗散核                | \(K(t) = \text{Im}[G_R(t)]\)                                        |
| 噪声关联函数          | \(\langle \xi(t)\xi(t') \rangle = \lambda^2 \text{Re}[G_R(t-t')] \coth\left( \frac{\hbar\omega}{2k_B T} \right)\) |
| 量子涨落耗散定理      | \(\kappa(\omega) = \hbar \omega \gamma(\omega) \coth\left( \frac{\hbar\omega}{2k_B T} \right)\) |

通过以上步骤，Caldeira-Leggett模型的量子场论形式得以构建，为研究开放量子系统的非平衡动力学提供了普适框架。
