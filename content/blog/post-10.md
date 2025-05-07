---
math: true
---


在量子力学和统计物理中，推迟格林函数（Retarded Green's Function） 是描述系统对扰动的时间因果响应的核心工具。以下是其详细计算步骤，结合开放系统（如Caldeira-Leggett模型）的具体示例：

---

**1. 推迟格林函数的定义**
推迟格林函数 \( G^R(t) \) 定义为算符在时间演化下的因果响应：
\[
G^R(t) = -\frac{i}{\hbar} \theta(t) \langle [A(t), B(0)] \rangle,
\]
其中：
• \( \theta(t) \) 是阶跃函数（保证因果性，仅 \( t > 0 \) 时有贡献）。

• \( [A(t), B(0)] \) 是算符 \( A \) 和 \( B \) 的量子对易子。

• \( \langle \cdot \rangle \) 表示热平衡态的平均。


---

**2. 推迟格林函数的计算步骤（以谐振子为例）**
考虑一个自由谐振子系统，哈密顿量为：
\[
H = \frac{p^2}{2m} + \frac{1}{2}m\omega_0^2 x^2.
\]
目标是计算坐标算符的推迟格林函数 \( G^R_{xx}(t) \)。

**步骤1：运动方程法**
1. 写出海森堡方程：  
   坐标算符 \( x(t) \) 的时间演化满足：
   \[
   \frac{d^2x(t)}{dt^2} + \omega_0^2 x(t) = 0.
   \]

2. 傅里叶变换到频域：  
   定义 \( x(\omega) = \int_{-\infty}^\infty x(t) e^{i\omega t} dt \)，方程变为：
   \[
   (-\omega^2 + \omega_0^2) x(\omega) = 0.
   \]

3. 格林函数的频域解：  
   引入外源项 \( F(\omega) \)（扰动），方程修改为：
   \[
   (-\omega^2 + \omega_0^2) x(\omega) = F(\omega).
   \]
   推迟格林函数 \( G^R(\omega) \) 满足：
   \[
   x(\omega) = G^R(\omega) F(\omega),
   \]
   解得：
   \[
   G^R(\omega) = \frac{1}{\omega_0^2 - \omega^2 - i\epsilon \omega},
   \]
   其中 \( \epsilon \to 0^+ \) 保证因果性（极点位于下半复平面）。

**步骤2：谱表示法**
推迟格林函数可分解为谱积分：
\[
G^R(\omega) = \int \frac{\rho(\omega')}{\omega - \omega' + i0^+} d\omega',
\]
其中 \( \rho(\omega) \) 是谱密度函数。对于谐振子：
\[
\rho(\omega) = \frac{1}{2m\omega_0} \left[ \delta(\omega - \omega_0) - \delta(\omega + \omega_0) \right].
\]
代入后得到：
\[
G^R(\omega) = \frac{1}{2m\omega_0} \left( \frac{1}{\omega - \omega_0 + i0^+} - \frac{1}{\omega + \omega_0 + i0^+} \right).
\]

---

**3. 开放系统的推迟格林函数（Caldeira-Leggett模型）**
对于主系统与热浴耦合的开放系统，推迟格林函数的计算需考虑耗散效应。

**模型哈密顿量**
\[
H = \frac{p^2}{2m} + V(x) + \sum_j \left( \frac{p_j^2}{2m_j} + \frac{1}{2}m_j \omega_j^2 x_j^2 \right) - x \sum_j c_j x_j.
\]

**步骤1：运动方程与阻尼项**
1. 主系统的有效运动方程：  
   积分出热浴自由度后，主系统的运动方程变为：
   \[
   m\ddot{x}(t) + \int_{-\infty}^t \gamma(t-t') \dot{x}(t') dt' + \frac{\partial V}{\partial x} = \xi(t),
   \]
   其中：
   • 阻尼核：\( \gamma(t) = \sum_j \frac{c_j^2}{m_j \omega_j^2} \cos(\omega_j t) \)

   • 随机力：\( \xi(t) \) 满足量子涨落关联。


2. 傅里叶变换后的方程：  
   频域中方程为：
   \[
   \left[ -m\omega^2 - i\omega \gamma(\omega) + m\omega_0^2 \right] x(\omega) = \xi(\omega).
   \]
   推迟格林函数为：
   \[
   G^R(\omega) = \frac{1}{m(\omega_0^2 - \omega^2) - i\omega \gamma(\omega)}.
   \]

**步骤2：阻尼核与谱密度的关系**
阻尼核的傅里叶变换为：
\[
\gamma(\omega) = \int_{-\infty}^\infty \gamma(t) e^{i\omega t} dt = \sum_j \frac{c_j^2}{m_j \omega_j^2} \cdot \frac{\pi}{2} \left[ \delta(\omega - \omega_j) + \delta(\omega + \omega_j) \right].
\]
结合谱密度 \( J(\omega) = \frac{2}{\pi} \sum_j \frac{c_j^2}{m_j \omega_j} \delta(\omega - \omega_j) \)，可得：
\[
\gamma(\omega) = \frac{2}{\pi} \int_0^\infty \frac{J(\omega')}{\omega'} \cdot \frac{\omega'^2}{\omega'^2 - \omega^2 - i\epsilon \omega} d\omega'.
\]

---

**4. 关键公式总结**
| 物理量                | 表达式                                                                 |
|-----------------------|----------------------------------------------------------------------|
| 自由谐振子的推迟格林函数 | \( G^R(\omega) = \frac{1}{\omega_0^2 - \omega^2 - i\epsilon \omega} \) |
| 开放系统的格林函数      | \( G^R(\omega) = \frac{1}{m(\omega_0^2 - \omega^2) - i\omega \gamma(\omega)} \) |
| 阻尼核与谱密度的关系    | \( \gamma(\omega) = \frac{2}{\pi} \int_0^\infty \frac{J(\omega')}{\omega'} \cdot \frac{\omega'^2}{\omega'^2 - \omega^2 - i\epsilon \omega} d\omega' \) |

---

**5. 物理意义**
1. 极点位置与准粒子寿命：  
   格林函数的极点 \( \omega = \omega_0 - i\Gamma/2 \) 对应系统的准粒子激发，虚部 \( \Gamma \) 表示寿命（耗散速率）。

2. 谱函数的物理信息：  
   格林函数的虚部 \( \text{Im} G^R(\omega) \) 直接给出系统的谱密度，反映能量吸收峰的宽度和位置。

3. 耗散的频率依赖：  
   阻尼核 \( \gamma(\omega) \) 的频率依赖性决定不同频率下系统的耗散强度（如Ohmic、超Ohmic行为）。

---

**结论**
推迟格林函数的计算需结合具体模型（自由系统或开放系统），通过运动方程或谱分解方法完成。在开放系统中，格林函数的形式直接受热浴谱密度 \( J(\omega) \) 的影响，其极点位置和虚部揭示了耗散与量子涨落的本质特性。这一工具在量子输运、非平衡统计和全息对偶中具有广泛应用。
