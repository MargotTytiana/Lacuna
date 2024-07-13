@autoHeader:1

# 拓扑空间
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

# 开矩形 Open Rectangle
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


# 邻域基
假设有拓扑空间${\displaystyle X}$，${\displaystyle x\in X}$的所有邻域的集合称为${\displaystyle x}$的邻域系，记作${\displaystyle {\mathcal {N}}(x)}$。

${\displaystyle {\mathcal {N}}(x)}$的一个子集${\displaystyle {\mathcal {U}}(x)}$称为${\displaystyle x}$的一个**邻域基**（neighborhood basis），如果满足：${\displaystyle x}$的每个邻域至少包含${\displaystyle {\mathcal {U}}(x)}$中的一个成员。

如果${\displaystyle {\mathcal {B}}}$是${\displaystyle X}$的拓扑基，那么${\displaystyle {\mathcal {U}}(x)=\{B\in {\mathcal {B}}:x\in B\}}$是${\displaystyle x}$的一个邻域基。

# 第一可数空间
如果拓扑空间${\displaystyle X}$中**任意一点都有**可数的邻域基，我们就称这个空间为**第一可数空间**，或称${\displaystyle C_{1}}$空间、${\displaystyle A_{1}}$空间。例如，度量空间是第一可数空间。

 换言之，对任意 $x∈X$，存在一列包含 $x$ 的开集 $U_1​,U_2​,…$ ，使得对任一开集 $x \in U$，都存在正整数 $n$ 使得 $U_n​⊆U$。

# 第二可数空间
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

# Lindelof 空间
我们需要引进**覆盖**的概念。假设${\displaystyle {\mathcal {A}}}$是一个${\displaystyle X}$中集合构成的子集族，${\displaystyle B\in X}$，我们称${\displaystyle {\mathcal {A}}}$是${\displaystyle B}$的一个覆盖（cover），是指${\displaystyle B\subset \bigcup _{A\in {\mathcal {A}}}A}$。

- **开覆盖**
假设${\displaystyle X}$是拓扑空间，我们称${\displaystyle {\mathcal {A}}}$是${\displaystyle B}$的**开覆盖**是指覆盖${\displaystyle {\mathcal {A}}}$中的元素是开集，同样的有闭覆盖的概念。
- **子覆盖**
假设存在${\displaystyle B}$的覆盖${\displaystyle {\mathcal {A}}}$，如果另有非空集族${\displaystyle {\mathcal {A}}'}$满足${\displaystyle {\mathcal {A}}'\subset {\mathcal {A}}}$且${\displaystyle {\mathcal {A}}'}是{\displaystyle B}$的覆盖，我们就称${\displaystyle {\mathcal {A}}'}是{\displaystyle {\mathcal {A}}}$的**子覆盖**。

如果${\displaystyle X}$的每一个开覆盖都有可数的子覆盖，我们就称${\displaystyle X}$是 **Lindelof 空间**。

### 林德勒夫引理 Lindelöf's lemma
设$C$是一组实数集，且该实数集是开集，$S⊆R$是被$C$覆盖的实数集的子集，于是$C$中存在一个可数的子集可以覆盖$S$。

# 商空间
当ρ(x,y)=0时，记x~y，~是R上的一个等价关系，记商集（即等价类全体为D=R/~，在D上作二元函数 ，则 是D上的距离，而(D,)称为R按拟距离ρ导出的商（度量）空间。
度量空间(R,ρ)中的子集A称为有界的，如果对x0∈R，存在常数M，使ρ(x0,x)≤M对A中的一切x成立。
设x0∈R，r>0，则称集合{x|x∈R,ρ(x,x0)<r}为以x0为中心，r为半径的开球，或x0的r邻域，记为O(x0,r)。又设，若对任何x∈A，存在x的某个邻域，则A称为开集；而称开集的补集为闭集。R中包含子集A的最小闭集就称为A的闭包。
商空间 [](https://www.bananaspace.org/wiki/%E5%95%86%E7%A9%BA%E9%97%B4)



# 参考文献
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