---
math: true
---

### AdS/CFT
在弦理论和黑洞物理的研究中，AdS/CFT对偶（反德西特空间/共形场论对偶）是一个极为重要的理论框架，它建立了引力理论与量子场论之间的深刻联系。通过研究在特定黑洞背景下的物理过程，有望进一步揭示AdS/CFT对偶的本质，加深对引力和量子场论统一描述的理解。具体到本文，通过向近极端D1 - D5 - P黑弦投掷标量场这一过程，尝试重新发现AdS/CFT对偶关系，同时计算标量场的吸收截面，这对于理解黑洞的霍金辐射以及黑洞与周围量子场的相互作用具有重要意义 ，也有助于探索量子引力的相关问题。

### 详细步骤
1. **设定研究背景与目标**
    - **度规引入**：研究对象为近极端D1 - D5 - P黑弦，其度规表达式为：
\[
\begin{align*}
ds^2&=(f_1f_5)^{-1/2}\left[-dt^2 + d\varphi^2+\frac{r_0^2}{r^2}(\cosh\sigma dt+\sinh\sigma d\varphi)^2\right]\\
&+(f_1f_5)^{1/2}\left[\frac{dr^2}{1 - r_0^2/r^2}+r^2d\Omega_3^2\right]
\end{align*}
\]
并设定参数条件\(r_0 \ll r_1, r_5\)，这会导致较低的霍金温度\(T_H\)，同时假设\(\cosh\sigma, r_1/r_5 \sim O(1)\)。其中\(f_1,f_5\)可能是与该黑弦相关的函数（文中未详细说明其具体形式，但不影响后续波动方程等推导过程 ）。
    - **研究目标**：计算低能量标量场（满足\(\omega r_5 \ll 1\)）的吸收截面，并且假设标量\(\chi\)在\(\varphi\)方向和3 - 球面上的动量为零。
    - **引入关键参数**：定义\(T_L = \frac{1}{2\pi}\frac{r_0e^{\sigma}}{r_1r_5}\)和\(T_R = \frac{1}{2\pi}\frac{r_0e^{-\sigma}}{r_1r_5}\)，它们将是对偶CFT中的左右移动温度，且与霍金温度\(T_H\)满足\(\frac{2}{T_H} = \frac{1}{T_L} + \frac{1}{T_R}\) 。
2. **引力计算 - 推导波动方程**
    - 对于形式为\(\chi = e^{-i\omega t}R(r)\)的标量场，在上述度规下，根据波动方程\(\square\chi = 0\)，经过复杂的计算和推导（涉及度规张量、协变导数等广义相对论相关运算 ），可得到：
\(\left( \frac{h}{r^3} \frac{d}{dr}hr^3\frac{d}{dr} + \omega^2f \right)R = 0\)
其中\(f = \left( 1 + \frac{r_1^2}{r^2} \right)\left( 1 + \frac{r_5^2}{r^2} \right)\left( 1 + \frac{r_0^2\sinh^2\sigma}{r^2} \right)\)，\(h = 1 - \frac{r_0^2}{r^2}\) 。此时该方程本质上可视为一维量子力学问题。
    - 为了更好地理解散射过程，通过定义\(\chi(r) = \frac{1}{\sqrt{r(r^2 - r_0^2)}}\psi(r)\)对波动方程进行变换，得到\(\left( -\frac{d^2}{dr^2} + V(r) \right)\chi = 0\)。虽然\(V(r)\)的表达式复杂，但可知它在视界\(r = r_0\)附近类似势阱，在无穷远处衰减，中间存在凸起，形似普通的薛定谔方程，意味着该过程是通过势的散射。
3. **引力计算 - 求解波动方程**
    - **确定求解策略**：为计算吸收截面，需求解波动方程并比较入射、透射和反射波的系数。采用的策略是在“近”和“远”区域分别近似求解方程，然后在中间的“匹配区域”将解进行匹配。其中，“远”区域定义为\(r \gg r_0\)；“近”区域定义为\(r \ll r_{1,5}\)且\(r \ll 1/\omega\)；“匹配区域”为\(r_0 \ll r_m \ll r_{1,5}\)。
    - **推导解的形式**：
        - 在远区域，波动方程的通解是贝塞尔函数的线性组合，即\(R_{far} = r^{-3/2}\sqrt{\frac{\pi\omega r}{2}}[AJ_1(\omega r) + BY_1(\omega r)]\) 。
        - 在近区域，通解为\(R_{near} = \left( \tilde{A}h^{-i(a + b)/2} + \tilde{B}h^{+i(a + b)/2} \right){}_2F_1(-ia, -ib, 1 - ia - ib, h)\)，其中\(a = \frac{\omega}{4\pi T_R}\)，\(b = \frac{\omega}{4\pi T_L}\)。
    - **应用边界条件与匹配解**：根据在视界\(r = r_0\)处波纯向内的边界条件，可确定\(\tilde{B} = 0\)。然后在匹配区域分别展开\(R_{near}\)和\(R_{far}\)：
        - \(R_{near} \approx \frac{\tilde{A}\Gamma(1 - ia - ib)}{\Gamma(1 - ia)\Gamma(1 - ib)} + O(\frac{r_0^2}{r^2})\) 。
        - \(R_{far} \approx \frac{A}{\sqrt{\pi}}\frac{2}{\sqrt{2\omega^{3/2}}} + B - terms\) 。通过匹配展开式中的项，得到\(\sqrt{\frac{\pi\omega^3}{2}}A = \tilde{A}\frac{\Gamma(1 - ia - ib)}{\Gamma(1 - ia)\Gamma(1 - ib)}\) 。
4. **引力计算 - 计算通量与吸收比**
    - **定义通量**：将二阶波动方程的Wronskian解释为守恒通量\(F \equiv \frac{1}{2i}\left( hr^3R^*\partial_rR - cc \right)\)，且\(\frac{dF}{dr} = 0\) 。
    - **计算通量值**：
        - 对远区域解在无穷远处展开\(R_{far} \approx \frac{1}{2r^{3/2}}\left( e^{i\omega r}\left( Ae^{-3\pi i/4} - Be^{-i\pi/4} \right) + e^{-i\omega r}\left( Ae^{3\pi i/4} - Be^{i\pi/4} \right) \right)\)，从而得到入射通量\(F_{in} = -\omega|\frac{A}{2}|^2\) 。
        - 使用相同公式计算通过视界的通量，得到吸收通量\(F_{abs} = -r_0^2(a + b)|\tilde{A}|^2\) 。
    - **计算吸收通量比**：由此可得吸收通量的比值\(R_{abs} = \frac{F_{abs}}{F_{in}} = \frac{\omega4\pi^2(r_1^2r_5^2)}{4}\frac{1}{e^{\omega/T_H} - 1}\frac{1}{(e^{\omega/2T_L} - 1)(e^{\omega/2T_R} - 1)}\) 。
5. **计算吸收截面（灰体因子）**
    - 由于之前计算的\(R_{abs}\)是霍金辐射中出现的灰体因子（差一个因子），考虑到所研究的球面波与平面波的关系\(e^{-i\omega z} = K e^{-i\omega r}\frac{1}{r^{3/2}}Y_{000} + \cdots\)（其中\(Y_{000}\)是\(S^3\)上的s - 波球谐函数，\(K = \sqrt{\frac{4\pi}{\omega^3}}\) ），通过\(\sigma_{abs} = |K|^2R_{abs}\)计算得到平面波的吸收截面，即灰体因子。 最终得到的吸收截面表达式综合了黑洞的几何参数（\(r_1, r_5, r_0\)）、标量场的能量\(\omega\)以及与对偶CFT温度（\(T_L, T_R, T_H\)）相关的项，完整地描述了标量场在近极端D1 - D5 - P黑弦背景下的吸收特性。 
