---
math: true
---

# 从对偶共形场论看吸收截面：AdS/CFT的奇妙应用
在探索量子引力和黑洞奥秘的旅程中，AdS/CFT对偶是一个强大而神奇的工具。今天，就让我们深入这个领域，一起看看如何从对偶共形场论（CFT）的角度来推导吸收截面，揭开其中隐藏的物理规律。

## 走进二维共形场论
在开始这段奇妙之旅前，我们得先了解一下共形场论的基础知识，特别是二维共形场论（2d CFT）。

想象一个二维的欧几里得平面\(R^2\)，上面有两个坐标\(x_1\)和\(x_2\)。为了方便研究，我们引入了复坐标\(z = x_1 + ix_2\)和\(\overline{z} = x_1 - ix_2\) ，平面上的度规可以简洁地写成\(ds^2 = (dx_1)^2 + (dx_2)^2 = dz d\overline{z}\) 。

共形变换在这个二维世界里有着特殊的地位，它是一种能让度规在整体缩放的情况下保持形式不变的坐标变换，即\(ds^2 = dz d\overline{z} \to e^{\sigma(w, \overline{w})}dw d\overline{w}\) 。经过一番推导可以发现，二维共形变换其实就等同于全纯坐标变换，这意味着变换函数得是全纯函数，比如\(f = f(w)\) ，\(\overline{f} = \overline{f}(\overline{w})\) 。这种全纯映射构成的共形群是无限维的，和高维空间中有限维的共形群\(SO(d, 2)\)（\(d > 2\)）截然不同。

有一个非常重要的共形变换，就是把平面映射到圆柱上。通过\(z = e^{-iw/R}\)和\(\overline{z} = e^{i\overline{w}/R}\)这个变换，我们就可以把平面和圆柱联系起来。在这个变换下，\(w\)坐标如果变化\(2\pi R\) ，就相当于在圆柱上绕了一圈回到原点，即\(w \sim w + 2\pi R\) 。如果把\(w\)拆分成实坐标\(w = \sigma_1 + i\sigma_2\) ，那么\(\sigma_1 \sim \sigma_1 + 2\pi R\)形成了圆柱的圆周方向，而\(\sigma_2\)则是无限延伸的。

从经典理论角度看，如果一个量子场论（QFT）的作用量在共形变换下保持不变，那么这个QFT就具有共形对称性。像自由无质量标量场的作用量\(S = \int d^2z\partial\varphi\overline{\partial}\varphi\)（这里\(\partial = \partial_z\) ，\(\overline{\partial} = \partial_{\overline{z}}\) ），在进行无穷小坐标变换\(z \to w(z)\)时，通过简单验证就能发现，测量中的雅可比行列式会和\(\partial\varphi = \frac{dw}{dz}\partial_w\varphi\)中出现的因子相互抵消，这就体现了它的共形对称性。然而，自由有质量标量场就不具备这种性质，这表明共形场论的一个重要特点：不能有任何有量纲的参数，因为这些参数会破坏共形变换中的尺度变换对称性。

但要注意，经典的共形不变性并不一定能保证量子层面的共形不变性。拿QCD举例，当把所有夸克质量设为零时，它在经典情况下具有尺度不变性，可一旦进行量子化，就需要引入调节器，这会导致出现有量纲的QCD尺度\(\Lambda_{QCD}\) ，从而使QCD在量子层面失去共形不变性。所以，我们现在说的CFT，一般指的是量子层面的。

在CFT里，局部算子可分为主要算子和后代算子。主要算子的变换遵循这样的规律：\(O^{\prime}(w, \overline{w}) = (\frac{dw}{dz})^{-h}(\frac{d\overline{w}}{d\overline{z}})^{-\overline{h}}O(z, \overline{z})\) ，这里的\((h, \overline{h})\)被称为共形权重。还有常用的记号\(\Delta = h + \overline{h}\) ，表示标度维度，它决定了在坐标缩放\((x_1, x_2) \to (\lambda x_1, \lambda x_2)\) （也就是\(\delta z = \lambda z\) ，\(\delta\overline{z} = \lambda\overline{z}\) ）时，算子的变换因子\(\lambda^{-\Delta}\) ；\(s = h - \overline{h}\)表示螺旋度，在旋转变换\((x_1, x_2) \to (x_1 - \lambda x_2, x_2 + \lambda x_1)\) （即\(\delta z = \lambda z\) ，\(\delta\overline{z} = -\lambda\overline{z}\) ）下，算子的变换因子是\(\lambda^{-s}\) ，而\(\vert s \vert = \vert h - \overline{h} \vert\)就是算子的自旋，和自由场论里洛伦兹指标的数量相对应。后代算子是通过对主要算子进行共形变换得到的，虽然它的变换规律比主要算子复杂，但也是由对称性完全确定的。正是因为所有局部算子都能归为这两类，才保证了关联函数在共形群下能够协变变换。比如平面上的两点函数\(\langle O_1(z_1, \overline{z_1})O_2(z_2, \overline{z_2})\rangle\) ，就一定具有\(\frac{C_{12}}{(z_1 - z_2)^{2h}(\overline{z_1} - \overline{z_2})^{2\overline{h}}}\)的形式，这里\(h = h_1 = h_2\) ，\(\overline{h} = \overline{h_1} = \overline{h_2}\) ，\(C_{12}\)是和场的归一化有关的常数。要是两个场的共形权重不一样，这个两点函数就会等于零。从路径积分的角度看，\(\langle O_1(z_1, \overline{z_1})O_2(z_2, \overline{z_2})\rangle\)（在归一化的前提下）可以写成\(\int D\Phi O_1(z_1, \overline{z_1})O_2(z_2, \overline{z_2})e^{-S[\Phi]}\) ，在算子语言里，它又等于\(_{line}\langle 0|O_1(z_1, \overline{z_1})O_2(z_2, \overline{z_2})|0\rangle_{line}\) ，这里\(|0\rangle_{line}\)是理论在无限直线（可以想象成\(Im z = 0\)轴）上的真空态。

## 有限温度下的二维共形场论
我们知道，有限温度下的QFT和欧几里得QFT在圆柱上的情况有着紧密联系，虚时间是周期性的。在CFT里，这种关系体现得非常明显。

通过\(w = iR\log z\)这个变换，再结合主要算子的变换规律（13.12），我们就能轻松推导出圆柱上的关联函数\(\langle O_{cyl}(w_1, \overline{w_1})O_{cyl}(w_2, \overline{w_2})\rangle \sim \frac{R^{-2h}}{\sin^{2h}(\frac{w_1 - w_2}{2R})}\frac{R^{-2\overline{h}}}{\sin^{2\overline{h}}(\frac{\overline{w_1} - \overline{w_2}}{2R})}\) （通常会省略“cyl”下标）。这个关联函数有两个很有趣的特点：一是它在圆柱的周期性\(w_1 \sim w_1 + 2\pi R\)下保持不变；二是在短距离情况下，也就是\(w_1 \to w_2\)时，它和平面上的关联函数\(\frac{C_{12}}{(w_1 - w_2)^{2h}(\overline{w_1} - \overline{w_2})^{2\overline{h}}}\)有着相同的奇点。实际上，根据QFT的理论，短距离行为是由真空关联函数决定的，而且这两个条件就能唯一确定这个函数（在假设无穷远处行为的情况下，甚至不需要指数映射就能推导出来）。

从洛伦兹的角度来看，对圆柱关联函数的解释有多种方式。如果把\(w = \sigma_1 + i\sigma_2\) ，当把\(\sigma_2\)当作“时间”进行维克旋转，令\(\sigma_2 = it\)时，得到的是洛伦兹圆柱\(S^1×Time\)上的理论，不过这个和有限温度没什么关系。而要得到有限温度的理论，我们需要进行另一种维克旋转，令\(\sigma_1 = it\) ，这样\(w \to i(t + x)\) ，\(\overline{w} = i(t - x)\) （注意在洛伦兹特征下，\(w\)和\(\overline{w}\)不再是复共轭关系），此时理论在虚时间上具有周期性\(t \sim t + 2\pi iR\) 。和有限温度的周期性\(t \sim t + i\beta\) （\(\beta = T^{-1}\) ）对比，就能得出\(\beta = T^{-1} = 2\pi R\) 。由此，我们可以得到有限温度下洛伦兹关联函数\(G_{\beta}(t - i\epsilon, x) = Tr e^{-\beta H}O(t - i\epsilon, x)O(0, 0) \sim (-1)^{h+\overline{h}}\frac{(\pi T)^{2h}}{\sinh^{2h}(\pi T(t + x))}\frac{(\pi T)^{2\overline{h}}}{\sinh^{2\overline{h}}(\pi T(t - x))}\) 。

这里给大家留两个小练习，可以试着证明一下（13.16）式，也就是平面上两点函数的形式；再推导一下（13.20）式，别忘了把缺失的系数也算出来哦，这能帮助大家更好地理解其中的原理。

## 吸收截面的推导过程
现在，我们回到吸收截面的推导上。之前在研究近极端黑弦时，通过引力计算得到了吸收截面\(\sigma_{abs} \sim \coth(\frac{\omega}{4T_H})\) 。

根据AdS/CFT对偶的神奇理论，我们可以把近地平线的几何用一个温度为\(T = T_H\)的1 + 1维CFT来代替，这个CFT就像是生活在AdS₃边界的一个虚拟“膜”上。这个边界其实就是我们在引力计算时的匹配位置，处于\(r_0 \ll r \ll r_{1,5}\)这个范围。

可能有人会问，这是哪种CFT呢？其实，我们这里只关注它的温度依赖性，整体因子在一定程度上也能匹配，不过会有一个常数的不确定性。我们不需要确切知道是哪种具体的CFT，只要了解它的一些一般性质就行，比如温度值，还有具有特定共形权重的算子的存在情况。目前已知的微观CFT大多来自弦理论，因为弦理论是量子引力的候选理论，但原则上，其他量子引力的UV完备理论也可能对应不同的CFT。在弦理论的相关例子中，如果知道了CFT的微观定义，就能在吸收计算中匹配系数，而且结果还很准确呢。

接下来，我们假设体标量场\(\chi\)和CFT算子\(O\)耦合，这样就给CFT添加了一个相互作用项\(S_{int} = \int dt dx O(t, x)\chi(t, x, r = 0)\) 。在这个式子中，\(O\)是CFT算子，\(\chi(r = 0)\)就是体场在CFT所在虚拟膜上的值，我们把它当作经典源。这里假设CFT的空间方向是展开的，用\(x \in (-\infty, \infty)\)表示（之前也叫\(\varphi\) ），当然，\(S^1\)版本的情况在一些额外假设下也能处理。同时，我们还假设这个源和CFT的耦合比较弱，这样就能用微扰的方法来处理这个相互作用项。

计算吸收截面时，我们设\(\chi = e^{-i\omega t}R(r)\) ，那么\(S_{int} \propto \int dt dx O(t, x)e^{-i\omega t}\) 。根据费米黄金规则，从初始态\(\vert i\rangle\)到末态\(\vert f\rangle\)的跃迁振幅\(M_{i \to f} \sim \langle f|\int dt dx O(t, x)e^{-i\omega t}|i\rangle\) 。总吸收率\(\Gamma_{abs}\)是对末态求和，再对初始态用热系综求平均，即\(\Gamma_{abs} \sim \sum_{i,f} e^{-\beta E_i}\int dt_1 dx_1 dt_2 dx_2 e^{-i\omega(t_1 - t_2)}\langle i|O(t_2, x_2)|f\rangle\langle f|O(t_1, x_1)|i\rangle\) 。对末态的求和相当于单位算符，所以忽略一个整体的体积因子（可以看作动量守恒的狄拉克函数\(\delta(0)\) ），\(\Gamma_{abs} \sim \int dt dx e^{-i\omega t}\sum_{i} e^{-\beta E_i}\langle i|O(t, x)O(0, 0)|i\rangle\) ，而这个求和就是热两点函数的定义，所以\(\Gamma_{abs} \sim \int dt dx G_{\beta}(t - i\epsilon, x)e^{-i\omega t}\) 。

之前我们已经算出了热关联函数\(G_{\beta}(t - i\epsilon, x)\) ，对它进行傅里叶变换时，利用积分公式\(\int dy e^{-i\omega y}(-1)^{h}(\frac{\pi T}{\sinh[\pi T(y \pm i\epsilon)]})^{2h} = \frac{(2\pi T)^{2h - 1}}{\Gamma(2h)}e^{\pm\omega/2T}|\Gamma(h + i\frac{\omega}{2\pi T})|^{2}\) ，先假设左右动量独立进行傅里叶变换，再令\(\omega_L = \omega_R = \omega\) 。吸收率是吸收和发射的差值，这对应着两种不同的\(i\epsilon\) 处方（大家可以思考一下为什么哦），最后就能得到\(\sigma_{abs} \sim \Gamma_{abs} - \Gamma_{emit} \sim \int dt dx e^{-i\omega t}[G(t - i\epsilon, \varphi) - G(t + i\epsilon, \varphi)] \sim \frac{2(2\pi T)^{2(h+\overline{h}) - 2}}{\Gamma(2h)\Gamma(2\overline{h})}\sinh(\frac{\omega}{2T})|\Gamma(h + i\frac{\omega}{4\pi T})\Gamma(\overline{h} + i\frac{\omega}{4\pi T})|^{2}\) 。当我们令\(h = \overline{h} = 1\) ，再利用\(|\Gamma(1 + ix)|^{2} = \frac{\pi x}{\sinh(\pi x)}\)这个等式，就能发现这个结果和之前引力计算的答案（13.25）是相符的。为什么要选\(h = \overline{h} = 1\)呢？目前只是为了让结果符合，一般来说，权重是由体场的质量和自旋决定的，对于无质量体场，\(h = \overline{h} = 1\)是正确的选择，之后我们还会更系统地讨论这个问题。

## 解耦：AdS/CFT的关键极限
前面几节的讨论有一个很重要的结论：在引力计算中，我们假设的近极端但非完全极端的情况，使得近地平线的自由度和渐近平坦远区域的场之间存在一定的耦合；在CFT中，也假设了引力场和CFT场之间是弱耦合的。

当我们让\(T_H \to 0\)时，就进入了Maldacena解耦极限。在这个极限下，远区域和近区域就会解耦。这时，我们可以完全忽略渐近平坦部分的计算，从而得到（3d版本的）AdS/CFT对应关系：\(AdS_3 \times S_3\)中的引力理论完全等同于AdS₃边界上的\(CFT_2\) 。

CFT具有UV完备性，这意味着这种对偶不仅能描述低能有效引力，还定义了\(AdS_3 \times S_3\)上的UV完备引力理论。在现代AdS/CFT的研究中，“远区域”的作用越来越小，我们甚至可以直接忽略它。


