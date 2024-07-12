@autoHeader:1

# ⛳ 拓扑空间
---

## 邻域
在点集理论中，**邻域**（neighborhood）指一个点集空间中某点“附近”的一个集合。

### 实数上的邻域
设 $a \in R ,  \delta > 0$：
#### δ邻域 
- **点a的δ邻域**：设$δ$是一个正数，则开区间$（a-δ，a+δ）$称为点$a$的$δ$邻域，记作
$$ U \left( a , \delta \right) = \left\{ x |\enspace a - \delta < x < a + \delta \right\}$$
	点a称为这个邻域的中心，$δ$称为这个邻域的半径。  
	由于 $a - \delta < x < a + \delta$ 相当于$| x - a | < \delta$，因此，$$U \left( a , \delta \right) = \left\{ x |\enspace | x - a | < \delta \right\}$$ 表示与点a的距离小于$δ$的一切点$x$的全体。

#### 去心δ邻域 
- **点a的去心δ邻域**：有时我们并不需要邻域中心的值，点a的$δ$邻域去掉中心a后，称为点a的去心$δ$邻域，记作$$ U ^ { \circ } ( a ) \quad 或 \quad \dot { U } ( a )$$ 
	即$$ \dot { U } ( a , \delta ) = \left\{ x  |\enspace 0 < | x - a | < \delta \right\}$$
	这里$0 < | x - a |$表示$x \neq a$。

<p><img src="./pic/领域.png" height="150px"  style="display: block; margin: 0 auto;"/></p>

- 点 𝑎 的 𝛿 **左邻域**：有时把开区间$(a - δ, a)$称为a的**左δ邻域**，$U _ { - } ( a ; \delta ) = ( a - \delta , a )$，简记作：$U _ { - }(a)$  
- 点 𝑎 的 𝛿 **右邻域**：开区间$(a, a + δ)$称为a的**右δ邻域**，$U _ { + } ( a ; \delta ) = ( a , a + \delta )$，简记作：$U _ { + }(a)$

#### 开邻域 & 闭邻域
- 若$x$的邻域同时是$X$中的开集，称其为$x$的**开邻域**；若它同时是$X$中的闭集则称其为$x$的**闭邻域**。

### 拓扑空间中的邻域

>[!note]
>设$X$为拓扑空间，$X$中一点$x$的邻域为$X$的一个子集$N$，使得存在一个$X$的开集$U$，满足 $x \in \small U \subset \small N$。 （不要求 $\small 𝑈$是否是开集，而定义的邻域始终是开集。）

邻域是一个特殊的区间，以点a为中心点任何开区间称为点a的邻域，记作$\small U(a)$。

#### 邻域公理 
假设有拓扑空间$\small 𝑋$，$𝑥∈𝑋$的所有**邻域**的集合称为𝑥的邻域系，记作$𝑁(𝑥)$。

>$U_1$：若集合$A∈N(x)$，且$N(x)\neq \varnothing$，则$x∈A$。  
>
>$U_2$：若集合$A, B∈N(x)$，则$A∩B∈N(x)$。    
>
>$U_3$：若集合$A∈N(x)$，且$A⊆B⊆ X$，则$B∈N(x)$。  
>
>$U_4$：若集合$A∈N(x)$，则存在集合$B∈N(x)$，使$B⊆A$，且$∀y∈B$，$B∈N(y)$。  


- 实际上，从上面四点我们可以建立**拓扑的邻域公理**：  
		假设𝑋是一个集合，又设对每一点$𝑥∈𝑋$都存在一个集合系$𝑁(𝑥)$使得它满足如上四点，则𝑋有唯一的一个拓扑使得对任意$𝑥∈𝑋$，$𝑁(𝑥)$是𝑥的邻域系。

- 这个拓扑中的开集是这样诱导的：  
		其中的开集定义为𝑋的子集𝑈，且如果$𝑥∈𝑈$则$𝑈∈𝑁(𝑥)$。这个拓扑与开集公理定义的拓扑等价。


### 度量空间中的邻域
- 度量空间：$(𝑋,𝜌)$中的一个点$𝑥_0∈𝑋$的邻域通常指的是以$𝑥_0$为心，$𝛿>0$为半径的开球，即

$$𝐵(𝑥_0,𝛿)={𝜌(𝑥,𝑥_0)<𝛿}$$

- 赋范线性空间：$(𝑋, ‖⋅‖)$中的一点的邻域是通过范数决定的度量$𝜌(𝑥,𝑦)=‖𝑥−𝑦‖$给出的。

- Euclid 空间：$𝑅_𝑛$中点𝑥的邻域 $𝑈$一般是用2-范数给出的

$$ B _ { 2 } ( x , \delta ) = \left\{ y \in R ^ { n } : \sum _ { i = 1 } ^ { n } ( x _ { i } - y _ { i } ) ^ { 2 } < \delta ^ { 2 } \right\} $$

### 其他
>[!tip]
>1.  拓扑空间$X$，$X$的子集$A$是开集，当且仅当$A$是其中所有点的邻域。  
>	（显然由此可知，从邻域公理出发可以等价地定义拓扑空间）。
>2. 拓扑空间$X$，$X$的子集$A$和$A°$，$A°$是$A$的开核，当且仅当$A° = \{x | \enspace ∃N∈N(x)，N⊆A\}$。
>3. 拓扑空间$X$，$X$的子集$A$和$A’$，$A’$是$A$的闭包，当且仅当  
>$A’ = \{x | \enspace ∀N∈N(x)，N∩A ≠ \varnothing\}$

## 度量空间
度量空间 (Metric Space)，在数学中是指一个集合，并且该集合中的任意元素之间的距离是可定义的。

>[!note]
>设$\small R$是一个非空集合，$ρ(x，y)$是$\small R$上的二元函数，满足如下条件：
>1. （正定性）$ρ(x,y)≥0$，且 $ρ(x,y)=0$ 当且仅当 $x=y$;
>2. （对称性）$ρ(x,y) = ρ(y,x)$;
>3. （三角不等式）$ρ(x,z) ≤ ρ(x,y) + ρ(y,z)$;  
>
>则称$ρ(x，y)$为两点$x，y$之间的*距离*。  $\small R$按距离$ρ$成为*度量空间*或*距离空间*，记为$(\small R，ρ)$。
>或者称，$\small R$为一个对于度量$ρ$而言的度量空间。  

### 子空间

- 设$\small A$是$\small R$的子集，则$\small A$按$\small R$中的距离$ρ$也成为度量空间，称为$\small R$的(度量) **子空间**。
### 拟距离

- 如果把上述距离的条件(1)改为：  
$$ρ(x，y)≥0 且 ρ(x，x)=0$$
	则称$ρ$为$R$上的**拟距离**。

### 圆盘
在几何中，一个**圆盘**（disk 或 disc）是由平面中一个圆（circle）围成的区域。一个圆只包含**边界**，而一个圆盘包含内部区域。
#### 开圆盘与闭圆盘
不含**边界**的圆盘称为**开圆盘**（open disk），包含**边界**的圆盘称为**闭圆盘**（close disk）。

<center class="half"> 
<img src="./svg/OpenDisk.svg" width="180" style="margin-right:120px"/> 
<img src="./svg/CIRCLE_1.svg"  width="190"/> 
</center>

圆盘是由一个圆周界定的区域。开圆盘是不包含边界圆周的圆盘的**内部**，而闭圆盘是开圆盘加上**边界圆周**。

球是圆盘在度量空间中的推广。不过，球被用来当作一个一般性的概念，以推广到多维空间，在这概念下，圆盘是二维空间（欧几里得平面）中的球。因此，开圆盘是二维的开球，闭圆盘是二维的闭球。

### 开球
开球（Open Ball），是一种基于球面几何的数学理论。开球的研究对象是一个开球面，即一个球面去除其内部点后所得的表面。  
- 开球面的维度为n（n为非负整数），与普通球面相同。

>[!tip] *也许你想知道——实数线：*  
>
>数学上，实数轴就是实数的集合$\mathbb{R}$。  
>
>另外，这一术语通常在R被当作某种空间（诸如拓扑空间、向量空间）的时候使用。实数线具有一个标准拓扑，它可以通过两种等价的方法引入。  
>
>作为拓扑空间，实数线是个1维的拓扑流形。  
>
>它既是可缩空间、局部紧致空间，也是仿紧致空间、第二可数空间。 它还具有标准可微结构，使它成为可微流形（由于可微同构，该拓扑空间只支持一个可微结构） 。

## 开集
在度量空间中，开集的定义可以与实数线的定义相联系。open set（开集）是对实数轴（real line）上开区间（open interval）的拓展。  

直观的说，开集就是不包含边界的集合，可以类比为开区间时，端点不包含在区间范围内。  

对于度量空间不能形象地理解时，可以将欧氏空间的赋值具体化。

例如：设有度量空间 $(X, d)$，有$X \in {\mathbb{R}}^n$，这里赋一个具体的值，使得$n=2$或$n=3$；距离$d(x,y)$ 可以看作欧氏距离中两点之间的距离。  

>[!note]
>*开集*定义：设$U$是度量空间$X$的一个子集。如果对于$U$中的任何$x \in U$，都有一个*以该点为中心的邻域*包含于$U$，则称$A$是度量空间$X$中的一个*开集*。  
>
>也可以这样理解：  
>
>设U是度量空间$(X,d)$的一个子集，对于任意 $x \in U$，都有一个实数 $\varepsilon > 0$，使得$X$中的任意一点到$x$的距离都小于 $\varepsilon$。

对于任意 $x \in X$， 设有一个[[#开球|开球]] $B(x,\varepsilon)$，开球半径为$\varepsilon$，此时$X$中的所有点的集合都在距离$x$的$\varepsilon$的范围内。可以这样理解：
1. 若$X=\mathbb{R}$，那么$B(x,\varepsilon)$就是开区间$(x-\varepsilon, x+\varepsilon)$。
2. 若$X={\mathbb{R}}^2$，那么$B(x, \varepsilon)$就是以$x$为圆心，$\varepsilon$ 为半径的[[#开圆盘与闭圆盘|开圆盘]]。

于是，子集$U$为开集，当且仅当任意$x \in U$，有 $\varepsilon>0$ 使得 $B(x, \varepsilon)$ 完全包括在子集$U$中（如左图）。

<center class="half"> 
<img src="./pic/B(x,ϵ).png" width="350" style="margin-right:120px"/> 
<img src="./pic/开集.png"  width="190"/> 
</center>


>[!tip]
>右图：满足$x^2+y^2=r^2$的点为蓝色，满足 $x^2+y^2 < r^2$ 的点为黄色。黄色的点形成了开集，黄色和蓝色的点的并集则是闭集（boundary set）。

## 闭集
在拓扑空间中，闭集是指其补集为开集的集合。 由此可以引申在度量空间中，如果一个集合所有的极限点都是这个集合中的点，那么这个集合是闭集。

>[!note]
>设$S$为拓扑空间，$S$中开集的补为$S$的闭集。

拓扑空间$S$中的闭集满足：

>[!note]
>- C1： $\varnothing ∈ C$ 并且 $S ∈ C$；  
>- C2： 任意闭集的交集是闭集；  
>- C3： 如果$A_1, A_2 ∈ C$，则有$A_1 \cap A_2 ∈ C$。  

>[!tip]
>也许你想知道 —— 相对补集  
>
> 如果A和B是集合，则在B中的A的相对补集也称为B和A的集合差，其元素属于 B，但不属于 A。   
> 
> A 在 B 中的相对补集通常写作 “B\A”，读作“A在B中的相对补集”。
> 
> <center><img src="./pic/B-A.webp" width="350"/></center>
> 
> 例如：B = {3, 9, 14}，A= {1, 2, 3}，B\A = {9, 14}

## 拓扑空间
>[!note]
>设一个集合$S$和一个[[#开集]]的集合$O$，如果下面的性质成立：
>	- T1： $\varnothing ∈ O$ 并且 $S ∈ O$；  
>	- T2： 任意开集的并集是开集；  
>	- T3： 有限个开集的交集是开集：如果$U_1, U_2 ∈ O$，则有$U_1 ∩ U_2 ∈ O$。  
>
>这时，我们称$𝓞$是$S$上的一个拓扑。 

###  证明
对于定义证明如下：

对于具有标准拓扑的实线，设$S = \mathbb{R}$，根据定义，$O$作为包含所有开集的集合。下面证明$S$是一个拓扑结构。  
#### 1. 证明T1
对于特殊情况，空集$\varnothing$属于$O$（$\varnothing∈ O$），并且$\mathbb{R}$本身就属于$O$，因此T1成立。

#### 2. 证明T2
设$S=∪E_a$，其中每个$E_a$都是开集。

对任一点$x_0∈S$，因为$E_a$是开集，所以存在区间$(c,d)⊆E_a$，且$x_0∈(c,d)$。

因此$x_0∈(c,d)⊆S$，即$x_0$是$S$的内点。由于$S$的任一点都是内点，所以$S$是开集。

#### 3. 证明T3
首先，设$U_1, U_2 ∈ O$。

假设$U_1 ∩ U_2 \neq \varnothing$，如果$x \in U _ { 1 } \cap U _ { 2 }$，则$x$将会存在于 $\enspace] a _ { 1 } , b _ { 1 } [ \subset U _ { 1 }\enspace$以及 $\enspace] a _ { 2 } , b _ { 2 } [ \subset U _ { 2 }\enspace$两个区间中。

此时，使：
$$ ]a _ { 1 } , b _ { 1 }[\enspace \cap \enspace] a _ { 2 } , b _ { 2 }[ \enspace= \enspace ] a , b [$$
其中，$a=min(a_1, a_2)$ 且 $b=min(b_1, b_2)$

因此，$$ x \in \left[ a , b \right] \subset U _ { 1 } \cap U _ { 2 }$$
因此，$U _ { 1 } \cap U _ { 2 }$ 是这些开集的并集，故其也是开集。

>[!tip]
>也许你想知道——欧氏空间：
>
>由所有的 n 元实数组（$x_1, x_2, …, x_n$）构成集合$R^n$，$R^n$中元素$x=(x_1,x_2, …,x_n)$与$y=(y_1, y_2, …, y_n)$之间的距离定义为：
>
>$$ d ( x , y ) = \left[  \sum _ { k = 1 } ^ { n } ( x _ { k } - y _ { k } ) ^ { 2 } \right] ^ { 1 / 2 }$$

### 标准拓扑
一般，我们将 ${\mathbb{R}}^n$ 由度量 $\left( \sum _ { i = 1 } ^ { n } | x _ { i } - y _ { i } | ^ { 2 } \right) ^ { 1 / 2 }$ 产生的拓扑叫做 ${\mathbb{R}}^n$ 的**标准拓扑**。以后但凡使用记号 ${\mathbb{R}}^n$，我们总使用标准拓扑。

### 离散拓扑
离散拓扑（discrete topology）是一类特殊的拓扑，即任何子集都是开集。  
设$S$为任意非空集合，则由$S$的所有子集组成的拓扑称为$S$上的**离散拓扑**。它是$S$上的最细拓扑。由此得到的拓扑空间称为**离散拓扑空间**或**离散空间**。

### 平凡拓扑
平凡拓扑 (trivial topology)， 只有 $\varnothing$ 和 $S$ 是开集。

## 开矩形 Open Rectangle
>[!attention]
>关于 ”open rectangle“ 的译名并不确定，本文采取了直译的方式，如有错误，欢迎指正。

>[!note]
>设$n$为自然数（$n \geq 1$），$a _ { 1 } , \ldots , a _ { n }$ 和 $b _ { 1 } , \ldots , b _ { n }$均为实数，计算笛卡尔乘积如下：
>
>$$ \prod _ { i = 1 } ^ { n } \left( a _ { i } \ldots b _ { i } \right) = ( a _ { 1 } \ldots b _ { 1 } ) \times \cdots \times ( a _ { n } \ldots b _ { n } ) \subseteq R ^ { n }$$
>
>于是 $\prod _ { i = 1 } ^ { n } \left( a _ { i } \ldots b _ { i } \right)$ 就称为*开矩形*，英文表达为 “open rectangle in  ${\mathbb{R}}^n$ ” 或者 “open n-rectangle”。
>-  $\prod _ { i = 1 } ^ { n } \left( a _ { i } \ldots b _ { i } \right)$ 也可以简记为：$( ( a . . b ) )$

- 如果 ${\mathbb{R}}^n$ 是开矩形的并集，则可以通过声明一个集合为开集来拓扑化。


## 邻域基
假设有拓扑空间${\displaystyle X}$，${\displaystyle x\in X}$的所有邻域的集合称为${\displaystyle x}$的邻域系，记作${\displaystyle {\mathcal {N}}(x)}$。

${\displaystyle {\mathcal {N}}(x)}$的一个子集${\displaystyle {\mathcal {U}}(x)}$称为${\displaystyle x}$的一个**邻域基**（neighborhood basis），如果满足：${\displaystyle x}$的每个邻域至少包含${\displaystyle {\mathcal {U}}(x)}$中的一个成员。

如果${\displaystyle {\mathcal {B}}}$是${\displaystyle X}$的拓扑基，那么${\displaystyle {\mathcal {U}}(x)=\{B\in {\mathcal {B}}:x\in B\}}$是${\displaystyle x}$的一个邻域基。

## 第一可数空间
如果拓扑空间${\displaystyle X}$中**任意一点都有**可数的邻域基，我们就称这个空间为**第一可数空间**，或称${\displaystyle C_{1}}$空间、${\displaystyle A_{1}}$空间。例如，度量空间是第一可数空间。

 换言之，对任意 $x∈X$，存在一列包含 $x$ 的开集 $U_1​,U_2​,…$ ，使得对任一开集 $x \in U$，都存在正整数 $n$ 使得 $U_n​⊆U$。

## 第二可数空间
如果一个拓扑空间${\displaystyle X}$有可数的拓扑基，我们就称它是**第二可数空间**，或称**完全可分空间**，也称${\displaystyle C_{2}}$空间或${\displaystyle A_{2}}$空间。    
对于欧氏空间 ${\mathbb{R}}^n$ ，它不仅在每个点$x$处有一个可数邻域基，而且它有一个只包含可数个开集的拓扑基，
$$ B = \left\{ B ( x , r ) | \enspace x \in Q ^ { n } , r \in Q > 0 \right\} $$
这是一个更强的可数性性质，称为**第二可数性公理**。
>[!note]
>第二可数性公理
>如果拓扑空间 $( X , \mathcal{T})$ 有一个可数基，即存在可数个开集$\{U_1,U_2,U_3,…\}$构成$\mathcal{T}$的一个拓扑基，则我们称$X$满足第二可数性公理，或者说它是第二可数的，简称为${\displaystyle A_{2}}$空间。

我们感兴趣的大多数拓扑空间是第二可数的。例如， ${\mathbb{R}}^n$ 是第二可数的，因为它是由可数的邻域基组成的——**开矩形的边长是有理数**，并且所有的点的坐标都是有理数。

显然，每个第二可数空间也是第一可数的，但反之不然。  

总结如下：
- 第二可数空间是第一可数空间，反之未必。
- 第二可数空间是可分空间，反之未必。
- ${\displaystyle C_{2}}$条件要求很强，甚至一些度量空间都可以不是第二可数的，可分的度量空间是第二可数的。
- 第二可数空间是 Lindelof 空间，反之未必。

## Lindelof 空间
我们需要引进**覆盖**的概念。假设${\displaystyle {\mathcal {A}}}$是一个${\displaystyle X}$中集合构成的子集族，${\displaystyle B\in X}$，我们称${\displaystyle {\mathcal {A}}}$是${\displaystyle B}$的一个覆盖（cover），是指${\displaystyle B\subset \bigcup _{A\in {\mathcal {A}}}A}$。

- **开覆盖**
假设${\displaystyle X}$是拓扑空间，我们称${\displaystyle {\mathcal {A}}}$是${\displaystyle B}$的**开覆盖**是指覆盖${\displaystyle {\mathcal {A}}}$中的元素是开集，同样的有闭覆盖的概念。
- **子覆盖**
假设存在${\displaystyle B}$的覆盖${\displaystyle {\mathcal {A}}}$，如果另有非空集族${\displaystyle {\mathcal {A}}'}$满足${\displaystyle {\mathcal {A}}'\subset {\mathcal {A}}}$且${\displaystyle {\mathcal {A}}'}是{\displaystyle B}$的覆盖，我们就称${\displaystyle {\mathcal {A}}'}是{\displaystyle {\mathcal {A}}}$的**子覆盖**。

如果${\displaystyle X}$的每一个开覆盖都有可数的子覆盖，我们就称${\displaystyle X}$是 **Lindelof 空间**。

### 林德勒夫引理 Lindelöf's lemma
设$C$是一组实数集，且该实数集是开集，$S⊆R$是被$C$覆盖的实数集的子集，于是$C$中存在一个可数的子集可以覆盖$S$。

## 商空间
当ρ(x,y)=0时，记x~y，~是R上的一个等价关系，记商集（即等价类全体为D=R/~，在D上作二元函数 ，则 是D上的距离，而(D,)称为R按拟距离ρ导出的商（度量）空间。
度量空间(R,ρ)中的子集A称为有界的，如果对x0∈R，存在常数M，使ρ(x0,x)≤M对A中的一切x成立。
设x0∈R，r>0，则称集合{x|x∈R,ρ(x,x0)<r}为以x0为中心，r为半径的开球，或x0的r邻域，记为O(x0,r)。又设，若对任何x∈A，存在x的某个邻域，则A称为开集；而称开集的补集为闭集。R中包含子集A的最小闭集就称为A的闭包。
商空间 [](https://www.bananaspace.org/wiki/%E5%95%86%E7%A9%BA%E9%97%B4)



## 参考文献
1. [邻域 | 中文数学 Wiki | Fandom](https://math.fandom.com/zh/wiki/%E9%82%BB%E5%9F%9F)
2. [商空间 - 香蕉空间 (bananaspace.org)](https://www.bananaspace.org/wiki/%E5%95%86%E7%A9%BA%E9%97%B4)
3. [实数线_百度百科 (baidu.com)](https://baike.baidu.com/item/%E5%AE%9E%E6%95%B0%E7%BA%BF/8262013)
4. [圆盘-数学百科 (shuxueji.com)](http://www.shuxueji.com/w/48313)
5. [Open Sets | Brilliant Math & Science Wiki](https://brilliant.org/wiki/open-sets/)
6. [集合论的集合符号（Ø，U，{}，∈，...） (rapidtables.org)](https://www.rapidtables.org/zh-CN/math/symbols/Set_Symbols.html)
7. [相对补集_百度百科 (baidu.com)](https://baike.baidu.com/item/%E7%9B%B8%E5%AF%B9%E8%A1%A5%E9%9B%86/942337)
8. [第一可数空间 | 中文数学 Wiki | Fandom](https://math.fandom.com/zh/wiki/%E7%AC%AC%E4%B8%80%E5%8F%AF%E6%95%B0%E7%A9%BA%E9%97%B4)
9. [第二可数空间](http://staff.ustc.edu.cn/~wangzuoq/Courses/22S-Topology/Notes/Lec13.pdf)
10. [覆盖 | 中文数学 Wiki | Fandom](https://math.fandom.com/zh/wiki/%E8%A6%86%E7%9B%96)
11. [Lindelof 空间 | 中文数学 Wiki | Fandom](https://math.fandom.com/zh/wiki/Lindelof_%E7%A9%BA%E9%97%B4)


内容
Introduction
Metrics spaces
Topology spaces:definitions and examples
Convergence and continuity in topological spaces
Bases and sub-bases,induced and co-induced topology
Quotient topology,group actions
Points and sets in topological space
Compactness
Compactness of product space,Tychonoff theorem
Compactness in metric space
Compactness in the space of continuous maps:Arzela-Ascolli theorem
The algebra of functions:Stone-Weierstrass theorem
Countability and Separation Axioms
Urysohn lemma and Urysohn metrization theorem
Tietze extension theorem and applications
Paracompactness and partition of unity
Midterm:Cover Lecture 1-Lecutre 16 1102
Connectedness
Path connecteness
Homotopy and path homotopy
The fundamental group
The fundamental groups of $SAn$(Sn \ge 1$)and applications
Van Kampen's theorem
Covering spaces
The classification of covering spaces
Brouwer's fixed point theorem;Brouwer's invariance of domain theorem
Jordan curve theorem
Classification of curves;Knots and links
Topology of compact surfaces
Classification of compact surfaces