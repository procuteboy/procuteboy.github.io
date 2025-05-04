---
math: true
---

在量子力学中，涨落耗散定理（Fluctuation-Dissipation Theorem, FDT）需考虑量子涨落和零点能的影响，其形式与经典情形不同。以下是量子涨落耗散定理的推导过程，最终结果为：
\[
\kappa(\omega) = m \hbar \omega \, \text{Re}[\gamma(\omega)] \coth\left(\frac{\hbar\omega}{2k_B T}\right),
\]
其中经典结果 \(\kappa(\omega) = 2mT \,\text{Re}[\gamma(\omega)]\) 是其高温极限（\(\hbar\omega \ll k_B T\)）下的近似。

---

**1. 量子布朗运动模型**
考虑量子粒子与热浴耦合的模型（如Caldeira-Leggett模型）：
• 系统哈密顿量：\( H_S = \frac{p^2}{2m} + V(x) \)

• 热浴哈密顿量：\( H_B = \sum_j \left( \frac{p_j^2}{2m_j} + \frac{1}{2}m_j \omega_j^2 x_j^2 \right) \)

• 耦合项：\( H_{SB} = -x \sum_j c_j x_j \)，其中 \(c_j\) 是耦合常数。


总哈密顿量 \(H = H_S + H_B + H_{SB}\) 的运动方程导出量子朗之万方程：
\[
m \ddot{x}(t) + \int_{-\infty}^t \gamma(t-t') \dot{x}(t') dt' = R(t),
\]
其中：
• 摩擦核 \(\gamma(t)\) 来自热浴的响应：\(\gamma(t) = \sum_j \frac{c_j^2}{m_j \omega_j^2} \cos(\omega_j t)\)。

• 随机力 \(R(t)\) 满足量子涨落关联：

  \[
  \langle R(t) R(t') \rangle = \frac{\hbar}{2} \int_{-\infty}^\infty \frac{d\omega}{2\pi} \kappa(\omega) e^{-i\omega(t-t')}.
  \]

---

**2. 热浴的量子关联函数**
热浴的随机力 \(R(t)\) 的量子关联函数由热平衡态下的期望值给出：
\[
\langle R(t) R(t') \rangle = \frac{\hbar}{\pi} \int_0^\infty d\omega \, \text{Im}[\gamma(\omega)] \left[ \coth\left(\frac{\hbar\omega}{2k_B T}\right) \cos\omega(t-t') - i \sin\omega(t-t') \right].
\]
其傅里叶变换为：
\[
\kappa(\omega) = \hbar \omega \, \text{Re}[\gamma(\omega)] \coth\left(\frac{\hbar\omega}{2k_B T}\right).
\]

---

**3. 关键推导步骤**
**(1) 热浴的谱密度**
定义热浴的谱密度 \(J(\omega)\)：
\[
J(\omega) = \frac{\pi}{2} \sum_j \frac{c_j^2}{m_j \omega_j} \delta(\omega - \omega_j),
\]
则摩擦核的虚部与谱密度相关：
\[
\text{Im}[\gamma(\omega)] = \frac{2}{\pi} J(\omega).
\]

**(2) 涨落耗散关系**
通过Kubo-Martin-Schwinger（KMS）条件，量子关联函数满足：
\[
\langle R(t) R(t') \rangle = \frac{\hbar}{\pi} \int_0^\infty d\omega \, \text{Im}[\gamma(\omega)] \left( \coth\left(\frac{\hbar\omega}{2k_B T}\right) + 1 \right) e^{-i\omega(t-t')}.
\]
对称化后得到：
\[
\kappa(\omega) = \hbar \omega \, \text{Re}[\gamma(\omega)] \coth\left(\frac{\hbar\omega}{2k_B T}\right).
\]

---

**4. 高温极限下的经典恢复**
当 \(\hbar\omega \ll k_B T\) 时，\(\coth\left(\frac{\hbar\omega}{2k_B T}\right) \approx \frac{2k_B T}{\hbar\omega}\)，此时：
\[
\kappa(\omega) \approx \hbar \omega \, \text{Re}[\gamma(\omega)] \cdot \frac{2k_B T}{\hbar\omega} = 2mT \, \text{Re}[\gamma(\omega)],
\]
与经典结果一致（其中 \(m \gamma(\omega)\) 替换为 \(\text{Re}[\gamma(\omega)]\)）。

---

**5. 物理意义**
1. 量子修正项：\(\coth\left(\frac{\hbar\omega}{2k_B T}\right)\) 包含：
   • 玻色-爱因斯坦分布：描述热激发的统计。

   • 零点涨落：即使 \(T \to 0\)，仍有 \(\coth(\infty) = 1\)，体现量子真空涨落。

2. 能量量子化：能量交换以 \(\hbar\omega\) 为单位，修正了经典白噪声谱。

---

**结论**
量子涨落耗散定理为：
\[
\kappa(\omega) = m \hbar \omega \, \text{Re}[\gamma(\omega)] \coth\left(\frac{\hbar\omega}{2k_B T}\right),
\]
其核心在于：
• 量子热浴的关联函数 包含 \(\coth\) 因子，反映玻色统计和零点能。

• 经典极限 下退化为 \(\kappa(\omega) = 2mT \, \text{Re}[\gamma(\omega)]\)，与实验结果一致。


这一结果在介观系统、量子输运和冷原子物理中有广泛应用，揭示了量子与经典热涨落的本质区别。
