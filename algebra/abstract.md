# 域，线性空间

## 域

* 同态

* 域

  * 域的同态只有单射

    * $\phi : F \to E \rArr F \cong E 的子域$

  * 域的特征

    * $$
      F = \begin{cases}
      0 & F / \mathbb{Q} \\
      p > 0 & F /\mathbb{F}_p
      \end{cases}
      $$

    * $\mathbb{Q}, \mathbb{F}_p$ : 素域（没有非平凡子域）

* 域扩张

  * $E / F$

  * 维数：$[E:F] := dim_F E$

  * 有限扩张

    * $[E:F]$ 有限

  * 有限生成扩张

    * 设 $S \subseteq E$, 考虑 $E$ 中包含 $S$ 和 $F$ 的最小子域 $F(S)$，称为在 $F$ 上由 $S$ 生成的域

    * $$
      F(S) = \bigcap_{\substack{F' \text{ 是 E 的子域} \\ F \cup S \subseteq F'} } F'
      $$

    * 若 $S$ 有限，$E = F(S)$，则称 $E / F$ 是有限生成的

    * 若对 $E$ 的任意有限子集，$F(S) \ne E$，则称 $E / F$ 是无限生成的

  * 代数扩张

    * 代数/代数元
      * 若 $u \in E$ 满足 $f(u) = 0$，其中 $f \in F[x]$，则称 $u$ 在 $F$ 上代数，或 $u$ 是 $F$ 上的代数元。
    * 若 $\forall u \in E$，$u$ 总是 $F$ 上的代数元，则称 $E$ 是 $F$ 上的代数扩张。
    * 若 $\exists u \in E$，使得 $u$ 不是任何 $f \in F[x]$ 的根，则称 $E$ 是**超越扩张**。

  * 有限扩张一定是有限生成扩张，但反之未必

  * 有限扩张一定是代数扩张，但反之未必

  * 有限生成的代数扩张是有限扩张

## Galois 群

* $Gal (E / F) := \{\sigma \in Aut (E) \mid \sigma|_f = id_F \}$

* 对称群 $S$
* 置换群 $G$

* 自同构群
  * $Aut(E) := \{ \sigma \in S(E) | \sigma 是E上自同构 \}$​
  * $Aut(E)$ 叫 $E$ 的自同构群

* $E/F$ 优先扩张 -> $Gal(E/F)$ 为有限群
* $F' = Inv (Gal (E/F))$, Q1 : $F'$ 是否等于 $F$？ Ans : 否
* $G \subseteq Aut(E), F = Inv(G), G' = Gal(E/F)$，$G$ 有限，则 $E/F$ 是有限扩张。G2：$G'$ 是否等于 $G$？Ans：是（**Artin 定理**）



# 环，模

Paolo Aluffi

Algebra Notes from the underground

## 环

* 环 $(R, +, \cdot), 0$

* 交换环

* 例子：

  * $\Z$、$Z_m$
  * $\Q$、$\R$、$\C$……所有的域
  * $F[x]$
  * 线性空间$V$，$End(V) = \{ \phi : V \to V | \phi 线性 \}$
    * 取基 $V \cong F^n $，$End(V) \cong M_n(F)$
    * 非交换环
  
  * $R = m \Z, \ m \in \N, m \ge 2$ （？）
    * 没有单位
  
  * $\Z[i]$  ，Gauss 整数环
  * $\Z(\sqrt D$，$D$ 无平方因子的整数。
    * Pell 方程 $x ^ 2 - D y ^ 2 = N$
  
  * $\Z(\xi_m)$,  $\xi_m = e^{\frac{2 \pi i}{m}}$
    * 分圆域
    * FLT
    * 环上可能没有唯一分解定理
    * -> 理想
  
  * $X$ ：集合，$R$：环
    * $R^x := \{ f : X \to R \}$
  
  * 设 $G$ 是有限群，$F$ 是一个域，$R = Span_F(G)$
    * $a = \sum_{g \in G} a_g g$   , $a_g \in F$
    * $b = \sum_{h \in G} b_h h$   , $a_g \in F$
    * $a \cdot b = \sum (a_g b_h) (g h)$
    * 则 $(R, +, \cdot)$ 是个环，且存在单位，$1_F$
    * 记为$F[G]$，$G$ 的群代数
    * 另一视角 （卷积）
      * $a : (G \to F) : (g \mapsto a_g) $
      * $b : (G \to F) : (h \mapsto b_h)$
      * $(a \cdot b)_k = \sum_{g \in G} a_g \cdot b_{g^{-1} k}$
  
  * Quiver 表示
    *  有向图
      * 有限
      * 不含定向圈
      * Path Q
      * $F$ ： 域
      * $F[Q] : Span\{ Q 的所有道路 \}$
      * 若头尾对不上，乘后变为 0
      * $q_R=\sum_i e_i$
      * 有单位，未必交换
  
  * 四元数

## 模

* 定义：

  * $R$：环，$M$：集合
  * $+ : M \times M \to M$
  * $\cdot : R \times M \to M$
  * 满足
    * xxx
    * $a(bx) = (ab)x$.  $\forall a b \in R, x \in M$
    * 分配律
      * $a(x+y) = ax + ay$
      * $(a+b)x = ax + bx$
  * 则称 $M$ 是一个**左 R 模**
  * 右 R 模：$M \times R \to M$
    * 若 R 交换，则左右等价
  * 若 R 是幺环，且 $1_R x = x, \forall x \in M$，则称 M 是一个幺模
  * 若 R，S 是两个环
    * $\cdot_R : R \times  M\to M$
    * $\cdot_S : M \times S \to M$
    * M 既是左 R 模又是右 S 模，且 $(ax)b = a (xb)$
    * 则称 M 是一个 $(R, S)$-双模

* 例：

  * 域上的线性空间 $F^n$
  * $\Z \times Z_m \to \Z_m, (a, x) \mapsto a  x$ 
    * Abel 群：交换群
    * 所有 Abel 群都是 $\Z$ 模 $\Z \times G \to G$
      * $(a, g) \mapsto ag$
  * $R = \R[t]$，$M$ 是一个 $\R$ 线性空间
    * $R \times M \to M$
    * $(f(t), x) \mapsto M$
    * 线性映射的多项式
    * 一元多项式环的模 <-> M 上的线性变换

  * $M_n(R)$，R交换环



# 群，群作用





# Galois 理论
