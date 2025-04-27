# 加速观者与Unruh效应

## 引言
在现代物理学的研究中，加速观者与Unruh效应是广义相对论和量子场论交叉领域的重要课题，它们揭示了时空与量子现象之间的深刻联系。

## 恒加速粒子
在二维的Minkowski空间中，取自然单位制，坐标表示为\(x^{\mu} = (t, x)\)，度规\(\eta_{\mu\nu} = \begin{pmatrix} +1 & 0 \\ 0 & -1 \end{pmatrix}\)。四速度\(u^{\mu} = \frac{dx^{\mu}}{d\tau} = \gamma(1, v)\)，且满足\(\eta_{\mu\nu}u^{\mu}u^{\nu} = 1\)；四加速度\(a^{\mu} = \frac{du^{\mu}}{d\tau}\)，同时\(\eta_{\mu\nu}a^{\mu}u^{\nu} = 0\)。

考虑随加速粒子的共动系\(\xi^{\mu} = (\tau, 0)\)，此时\(u^{\mu} = (1, 0)\)。由正交关系\(\eta_{00}a^{0}u^{0} + \eta_{11}a^{1}u^{1} = 0\)可推出\(a^{0} = 0\)，即\(a^{\mu} = (0, a)\)，且\(\eta_{\mu\nu}a^{\mu}a^{\nu} = -a^{2}\)。

引入光锥系\(u = t - x\)，\(v = t + x\)，\(ds^{2} = dudv\)，度规变为\(g_{\mu\nu} = \begin{pmatrix} 0 & \frac{1}{2} \\ \frac{1}{2} & 0 \end{pmatrix}\)。根据四速度和四加速度表达式\((g_{01} + g_{10})\frac{du}{d\tau}\frac{dv}{d\tau} = 1\)，\(\dot{u}\dot{v} = 1\)；\((g_{01} + g_{10})\frac{d^{2}u}{d\tau^{2}}\frac{dv}{d\tau} = 1\)，\(\ddot{u}\ddot{v} = -a^{2}\)，其中一个解为\(u = -\frac{1}{a}e^{a\tau}\)，\(v = \frac{1}{a}e^{a\tau}\)。

由此可得\(t = \frac{u + v}{2} = \frac{1}{2a}(e^{a\tau} - e^{-a\tau}) = \frac{1}{a}\sinh(a\tau)\)，\(x = \frac{v - u}{2} = \frac{1}{2a}(e^{a\tau} + e^{-a\tau}) = \frac{1}{a}\cosh(a\tau)\)，这表明加速粒子的世界线是一条双曲线\(x^{2} - t^{2} = \frac{1}{a^{2}}\)，另一组解则代表了另一支双曲线。

## 加速观者与Rindler时空
观测者的标架场沿着观测者的世界线做费米 - 沃克尔移动，利用每个固有时时刻的类空超曲面建立观测者的坐标网格。设\(OP = OP_0 + P_0P\)，加速观者的标架为\(e_{\xi_0} = \cosh(a\tau)e_t + \sinh(a\tau)e_x\)，\(e_{\xi_1} = \sinh(a\tau)e_t + \cosh(a\tau)e_x\)。

对上式对坐标基投影，得到\(t = (\frac{1}{a} + \xi_1)\sinh(a\tau) + \xi_0\cosh(a\tau)\)，\(x = (\frac{1}{a} + \xi_1)\cosh(a\tau) + \xi_0\sinh(a\tau)\)。

当\(\xi_0 = 0\)时，\(t = (\frac{1}{a} + \xi_1)\sinh(a\tau)\)，\(x = (\frac{1}{a} + \xi_1)\cosh(a\tau)\)，确定了坐标曲线\(\frac{t}{x} = \tanh(a\tau)\)，\(x^{2} - t^{2} = (\frac{1}{a} + \xi_1)^{2}\)。又因为\(\frac{t_0}{x_0} = \tanh(a\xi_0)\)，所以相对于匀加速粒子的类空超曲面上的事件点都在经过粒子时间点和坐标原点的直线上。

对于观测者\(\tau = \xi_0\)，度规\(ds^{2} = (1 + a\xi_1)^{2}d\xi_0^{2} - d\xi_1^{2}\)，可以看到惯性力的出现。常定义新坐标使度规共形平坦，\(ds^{2} = \Omega^{2}(\xi_0, \xi_1)[(d\xi_0)^{2} - (d\xi_1)^{2}]\)。

在光锥系\(\tilde{u} = \xi^0 - \xi^1\)，\(\tilde{v} = \xi^0 + \xi^1\)下，\(ds^{2} = \Omega^{2}(\tilde{u}, \tilde{v})d\tilde{u}d\tilde{v}\)；对于闵氏时空\(ds^{2} = dudv\)。满足\(u = u(\tilde{u})\)，\(v = v(\tilde{v})\)，且\(u = 0\)时，\(\tilde{u} \to \infty\)；\(v = 0\)时，\(\tilde{v} \to \infty\)；\(u < 0\)，\(v > 0\)。令\(u = -\frac{1}{a}e^{-a\tilde{u}}\)，\(v = \frac{1}{a}e^{a\tilde{v}}\)，则\(ds^{2} = e^{2a\xi^1}[(d\xi^0)^{2} - (d\xi^1)^{2}]\)，得到\(t(\xi^0, \xi^1) = \frac{1}{a}e^{a\xi^1}\sinh(a\xi^0)\)，\(x(\xi^0, \xi^1) = \frac{1}{a}e^{a\xi^1}\cosh(a\xi^0)\)，称为right Rindler wedge（覆盖了四分之一的平坦时空）。其对应的克氏符\(\Gamma^{\xi_1}_{\xi_0 \xi_0} = \Gamma^{\xi_0}_{\xi_0 \xi_1}=\Gamma^{\xi_1}_{\xi_1 \xi_1}=a\)以及Riemann曲率\(R^{\sigma}_{\rho \mu \nu} = 0\)，说明它是Riemann平坦的。

## Unruh效应
考虑无质量的标量场，其作用量为\(S = \frac{1}{2} \int g^{\mu \nu} \partial_{\mu} \partial_{\nu} \Phi \ d^{2}x\)，作用量是共形不变的，即\(\sqrt{-g'} = \Omega^{2} \sqrt{-g}\)，\(g'^{\mu \nu} = \Omega^{-2} g^{\mu \nu}\)，所以\(S' = S\)，两个时空对应的运动方程相同，\((\frac{\partial^{2}}{\partial t^{2}} - \frac{\partial^{2}}{\partial x^{2}})\Phi = 0\)，\((\frac{\partial^{2}}{\partial {\xi^0}^{2}} - \frac{\partial^{2}}{\partial {\xi^1}^{2}})\Phi = 0\)。

将场展开为正向运动和负向运动\(\hat{\Phi}_R = \int_{0}^{\infty} \frac{dk}{\sqrt{4 \pi k}} \hat{a}^+ e^{+ik(t - x)} + \int_{0}^{\infty} \frac{dk}{\sqrt{4 \pi k}} \hat{a}^- e^{-ik(t - x)}\)，\(\hat{\Phi}_L = \int_{0}^{\infty} \frac{dk}{\sqrt{4 \pi k}} \hat{a}^+ e^{+ik(t + x)} + \int_{0}^{\infty} \frac{dk}{\sqrt{4 \pi k}} \hat{a}^- e^{-ik(t + x)}\)，即\(\hat{\Phi}_R = \int_{0}^{\infty} \frac{d\omega}{\sqrt{4 \pi \omega}} (\hat{a}^-_{\omega} e^{-i\omega u} + \hat{a}^+_{\omega} e^{i\omega u}) = \int_{0}^{\infty} \frac{d\Omega}{\sqrt{4 \pi \Omega}} (\hat{b}^-_{\Omega} e^{-i\Omega \tilde{u}} + \hat{b}^+_{\Omega} e^{i\Omega \tilde{u}})\)，其中\(\hat{a}\)和\(\hat{b}\)分别代表两个时空中的算符，且\(\hat{a}^-_{\omega} |0_M \rangle = 0\)，\(\hat{b}^-_{\Omega} | 0_R \rangle = 0\)。

联系这两个算符的是Bogolyubov变换\(\hat{b}^-_{\Omega}= \int_{0}^{\infty} d\omega (\alpha_{\Omega\omega}\hat{a}^-_{\omega} - \beta_{\Omega\omega} \hat{a}^+_{\omega})\)，可以求得\(\alpha_{\Omega \omega} = \frac{1}{2 \pi a} \sqrt{\frac{\Omega}{\omega}} e^{\pi \omega / 2a}e^{i(\Omega/a)\ln(\omega/a)}\Gamma(- \frac{i\Omega}{\omega})\)，\(\beta_{\Omega \omega} = -\frac{1}{2 \pi a} \sqrt{\frac{\Omega}{\omega}} e^{-\pi \omega / 2a}e^{i(\Omega/a)\ln(\omega/a)}\Gamma(- \frac{i\Omega}{\omega})\)。

加速时空测得闵氏时空的平均粒子数为\(n_{\Omega}= \frac{1}{V} \langle 0 | \hat{b}^+_{\Omega} \hat{b}^-_{\Omega} |0\rangle_M =\frac{1}{V} \int d\omega {|\beta_{\Omega \omega }|^2} = \frac{1}{e^{2\pi \Omega/a} - 1}\)，满足B - E分布，对应的温度称为Unruh温度\(T = \frac{a}{2 \pi}\)，这表明真空态的选取依赖于时空。

## Hawking辐射
考虑Schwarzschild黑洞，在近视界对度规展开，定义\(r - r_s = \frac{\tilde{x}^2}{4 r_s}\)，\(\tilde{x} \to 0\)，则\(1 - \frac{r_s}{r} = \frac{\tilde{x}^2}{4 r_s^2 + \tilde{x}^2} \approx (\frac{\tilde{x}}{2 r_s})^2\)，\(ds^{2} = (\frac{\tilde{x}}{2 r_s})^2 dt^{2} - d\tilde{x}^{2} + r_s^{2} d\Omega^{2}\)。

引入坐标变换\(\tilde{x} = e^{x / 2 r_s}\)，则\(ds^{2} = (\frac{1}{2 r_s})^2 e^{x/ r_s}( dt^{2} - d x^{2} )+ r_s^{2} d\Omega^{2}\)。与Rindler时空比较\(ds^{2} = e^{2a \xi^1} [(d\xi^0)^2 - (d\xi^1)^2]\)，相当于时空度规变成了局部的Rindler时空，对应的加速度称为黑洞的表面引力\(a = \frac{1}{2 r_s}\)，进而得到Hawking温度\(T = \frac{1}{4 \pi r_s}\)。

## 结论
通过对恒加速粒子、加速观者与Rindler时空、Unruh效应以及Hawking辐射的研究，我们深入了解了时空、加速度与量子场之间的相互作用。Unruh效应揭示了加速观者会观测到原本真空态的热辐射，而Hawking辐射则表明黑洞也具有热性质，这些理论成果为统一广义相对论和量子场论提供了重要的线索和方向，也为进一步探索宇宙的奥秘奠定了基础。未来的研究可以在此基础上，深入探讨相关理论在更广泛物理情境下的应用和拓展。 


