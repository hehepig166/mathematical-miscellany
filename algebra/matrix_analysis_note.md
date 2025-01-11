# 杂

## 子式

### 顺序主子式

## 对角化

* $A = P \Lambda P^{-1}$
* 方法：
  * 特征值 -> $\Lambda$
  * 对应的特征向量，单位化 -> $P$​
* 判别
  * $\lambda E - A$ 的初等因子都是 $\lambda$ 的一次式


# 变换

## 线性空间（$V_F$）

* $V = \{\alpha, \beta, \dots\}, F$
  * 加法封闭
  * 数乘封闭
* 子空间
  * 若 $W_F$ 为 $V_F$ 的子空间，则
  * $\forall \alpha, \beta \in W, \alpha + \beta \in W$
  * $\forall k \in F, \alpha \in W, k\alpha \in W$
* $span\{\alpha_1, \alpha_2, \dots, \alpha_m\}$
* 维数：极大大线性无关组的大小
* 基、坐标
* 基变换、坐标变换（过渡矩阵）
* 维数公式
* 直和
  * 定义：$V_1, V_2$ 是 $V$ 的子空间，若 $V_1 + V_2$ 中任意元素的分解式 $\alpha = (\alpha \in V_1) + (\alpha \in V_2)$ 唯一，则称 $V_1 + V_2$ 为直和，记为 $V_1 \oplus V_2$.
  * $V_1 + V_2 = \{\alpha_1 + \alpha_2 | \alpha_1 \in V_1, \alpha_2 \in V_2\}$ 
  * 以下等价
    * $V_1 + V_2$ 是直和
    * 零向量分解式唯一
    * $V_1 \cap V_2 = \empty$
    * $V_1$ 的一组基与 $V_2$ 的一组基的并是 $V_1 + V_2$ 的一组基
    * $dim (V_1 + V_2) = dim(V_1) + dim(V_2)$

* 直和补

## 线性变换

* $T : V_F \rarr V_F$
  * （满足线性性， $\forall \alpha, \beta \in V, \forall k \in F$）
  * $T(\alpha + \beta) = T(\alpha) + T(\beta)$
  * $T(k\alpha) = k T(\alpha)$
* 线性变换的矩阵
  * 定义
    * $V_F$ 的一组基 $(\alpha_1, \dots, \alpha_n)$
    * $T(\alpha_1, \dots, \alpha_n) := (T\alpha_1, \dots, T \alpha_n)$
    * $T(\alpha_1, \dots, \alpha_n) = (\alpha_1, \dots, \alpha_n) A_{n \times n}$
    * 称 $A$ 为线性变换 $T$ 在基 $(\alpha_1, \dots, \alpha_n)$ 下的矩阵
  * 给定 $T$，基 $\lrArr$ 矩阵
  * 给定基，$T$ $\lrArr$​ 矩阵
* 线性变换的过渡矩阵
* 核 $Ker T$、像 $Im T$​
  * $\forall x \in Ker T, T x = 0$
  * 线性空间 $V$ 的基 $(\alpha_1, \dots, \alpha_n)$，线性变换 $T \alpha = \alpha A$，$rank A = r$，则
  * $dim (Ker T) = n - r$
  * $dim (Im T) = r$

* 不变子空间
  * $T(W) \subseteq W$​

* $T : V \rarr V, (Im T + Ker T = V \lrArr Im T \oplus Ker T)$
* $Im T + Ker T = V \rArr Im T^2 = Im T$

## 内积空间

* 定义（实内积空间）
  * $V$：实线性空间
  * $\forall \alpha, \beta \in V$，存在唯一 $r \in \R$ 与之对应，记作 $(\alpha, \beta) = r$
  * 对称性
    * $(\alpha, \beta) = (\beta, \alpha)$
  * 线性性
    * $(k\alpha, \beta) = k (\alpha, \beta)$
    * $(\alpha + \beta, \gamma) = (\alpha, \gamma) + (\beta, \gamma)$
  * 非负性
    * $(\alpha, \alpha) \ge 0$
    * $(\alpha, \alpha) = 0 \lrArr \alpha = 0$​
* 度量矩阵
* 标准内积（度量矩阵为单位阵）
* $(\alpha, \beta) = x^\top A y$
* 过渡矩阵
  * 基 $\alpha$ -> 度量矩阵 $A$，基 $\beta$ -> 度量矩阵 $B$
  * $B = P^\top A P$
  * $P$ 为基 $\alpha$ 到 $\beta$​ 的过度矩阵

## 柯西不等式

* $|(x, y)| \le ||x|| ||y||$
* 取等当且仅当 $x$，$y$ 线性相关

## 正交变换

* 内积空间中保长度的线性变换
  * $(T \alpha, T \alpha) = (\alpha, \alpha)$
* 性质
  * $(T \alpha, T \beta) = (\alpha, \beta)$​

## 对称变换

* $(T\alpha, \beta) = (\alpha, T \beta)$

# 矩阵性质

## 可逆

## 满秩

## 正交

## 对称

## 正定

* 实数域 -> 正定一定是实对称的

## 对角

## 上三角

## 单位上三角

## 幂等

$A ^ 2 = A$

## 幂零

$\exist k, A^k = 0$



# 矩阵关系

## 相似

$A = P B P^{-1}$

## 合同

$A = Q^\top B Q$

# 特殊矩阵

## 过渡矩阵

### 基 $(\alpha_1, \dots, \alpha_n)$ 到 $(\beta_1, \dots, \beta_n)$的过渡矩阵（基变换矩阵）

* $P$ 使得 $(\beta_1, \dots, \beta_n) = (\alpha_1, \dots, \alpha_n)P$

* 坐标变换公式
  * 基 $\{\alpha\}$ -> 坐标 $x \in \R^{n \times 1}$，基 $\{\beta\}$ -> 坐标 $y \in \R^{n \times 1}$
  * $(\alpha_1, \dots, \alpha_n)x = (\beta_1, \dots, \beta_n)y = (\alpha_1, \dots, \alpha_n)Py$
  * $x = Py$
  * $y = P^{-1} x$

### 线性变换的矩阵的过渡矩阵

* $V_F$ 中的线性变换 $T$ 在两个基 $(\alpha_1, \dots, \alpha_n)$ 与 $(\beta_1, \dots, \beta_n)$ 下的矩阵为 $A, B$
* $P$ 使得 $B = P^{-1} A P$
* 基的过渡矩阵 $P$​ 即为线性变换矩阵的过渡矩阵
  
  * $A \sim B$
  * $T \alpha = \alpha A$
  * $T \beta = \beta B$
  * $\beta = \alpha P$
  * $$
    \begin{aligned}
    T \beta
    &= \beta B = \alpha P B \\
    &= (T\alpha) P = \alpha A P
    \end{aligned}
    $$
  *  $B = P^{-1} A P$​

### 内积空间度量矩阵的过度矩阵

* 基 $\alpha$ -> 度量矩阵 $A$，基 $\beta$ -> 度量矩阵 $B$
* $B = P^\top A P$
* $P$ 为基 $\alpha$ 到 $\beta$ 的过度矩阵



## Householder 矩阵（初等反射变换）

* 定义
  * $\omega_{n \times 1} \in \R^n, ||\omega|| = 1$
  * $H_\omega = E - 2 \omega \omega^\top$

* 性质
  * $H_\omega \omega = -\omega$
  * $\forall x \perp w, H_\omega x = x$

# 若当标准型!!

### 行列式因子 D

### 不变因子 d

​	称 $\lambda E - A$ 的不变因子为 $A$ 的不变因子

### 初等因子（组）

## （$\lambda$​​ 阵）等价标准型

## 若当标准型

初等因子 -> 若当块 -> 拼成若当标准型



# 广义逆!!

* 定义（实）
  * $AXA = A$
  * $XAX = X$
  * $(AX)^\top = AX$
  * $(XA)^\top = XA$
* $A^+$ 存在且唯一
* 性质
  * 若 $A$ 可逆，则 $A^+ = A^{-1}$
  * $(A ^ +) ^ + = A$
  * $(A^\top)^+ = (A^+)^\top$​
  * $rank(A^+) = rank(A^+A) = rank(AA^+) = rank(A)$
  * $A^+ = (A^\top A)^+ A^\top = A^\top (AA^\top)^+$​
  * R：像集
    * $R(AA^+) = R(A)$
    * $R(A^+A) = R(A^+) = R(A^\top)$​
  * $(A^\top A)^+ = A^+ (A^\top)^+$
  * $A$ 为实对称方阵时，$AA^+ = A^+A$
  * 
* 求法1
  * 满秩分解 $A = BC$
  * $A^+ = C^\top (C C^\top)^{-1} (B^\top B)^{-1} B^\top$

## （矛盾）方程组通解

* $Ax = b$ 有解 $\lrArr$ $AA^+b = b$

* 通解：有解 -> 解 / 无解 -> 最小二乘解
* $x = A^+b + (E - A^+ A) y$，  $\forall y$

# 矩阵分解

## LR 分解

* $A = LR$

* $L$ ：单位下三角
* $R$ ：可逆上三角
* 分解唯一
* 并不是所有矩阵都有 LR 分解（需要各阶顺序主子式均不等于零）
* 求法
  * 法1：使用行变换化成上三角
  * 法2：$(A | E) \rarr (R | L^{-1})$

例：
$$
\pmatrix{1 & 2 & 3 \\ 2 & 5 & 1 \\ 3 & 2 & 5} = \pmatrix{1 & 0 & 0 \\ 2 & 1 & 0 \\ 3 & -4 & 1 } \pmatrix{1 & 2 & 3 \\ 0 & 1 & -5 \\ 0 & 0 & -24}
$$

### LDU 分解

* $A = LDU$

* $L$ ：单位下三角
* $D$ ：对角矩阵
* $U$ ：单位上三角
* **分解唯一**
* 求法：把 LR 分解的 R 单位化即可

例：
$$
\pmatrix{1 & 2 & 3 \\ 2 & 5 & 1 \\ 3 & 2 & 5} = \pmatrix{1 & 0 & 0 \\ 2 & 1 & 0 \\ 3 & -4 & 1 } \pmatrix{1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -24} \pmatrix{1 & 2 & 3 \\ 0 & 1 & -5 \\ 0 & 0 & 1}
$$

### Crout 分解（LU分解）

* $A = LU$

* $L$ ：可逆下三角
* $U$ ：单位上三角
* **分解唯一**
* 求法：把 LDU 分解的 LD 合并即可

### Cholesky 分解

* 条件：$A$ 正定
* $A = G G^\top$
* $G$​ ：对角元素均为正数的下三角矩阵
* **分解唯一**
* 求法：
  * $G = L D^{\frac{1}{2}}$
  * 证明：
    * $A = A^\top$
    * $LDU = A = A^\top = U^\top D^\top L^\top = U^\top D L^\top$
    * 因 LDU 分解唯一，所以 $L = U^\top$​

例：

## 满秩分解

* 设 $rank(A) = r, A_{m \times n}$
* $A = BC$
* $B_{m \times r}$ 列满秩
* $C_{r \times n}$ 行满秩
* **不唯一**
* 求法：
  * 初等行变换 $A \rarr $ 行阶梯 $\pmatrix{C \\ 0} = PA$
  * $\pmatrix{B & 0} = P^{-1}$

例1：
$$
\pmatrix{1 & -3 & -6 \\2 & 3 & -2 \\ -3 & 0 & -4} = \pmatrix{1 & 0 \\ 2 & 9 \\ -3 & -9} \pmatrix{1 & -3 & -6 \\ 0 & 1 & \frac{14}{9}}
$$
例2：
$$
\pmatrix{2 & 1 \\ 1 & 1 \\ 2 & 1}
$$


### QR 分解（正交满秩分解）

* $A = QR$
* $Q$ ：列满秩且正交（即$Q^\top Q = E$）
* $R$ ：行满秩
* **不唯一**
* 求法：
  * 先进行满秩分解 $A = BC$
  * 将 B 看作列向量组，将其正交单位化，作为 $Q$，同时得到 $R$
  * $B = (\beta_1, \dots, \beta_r) = (e_1, \dots, e_r) R$​

例1：
$$
\begin{aligned}
\pmatrix{1 & -3 & -6 \\2 & 3 & -2 \\ -3 & 0 & -4}
&= (\pmatrix{1 & -5 \\ 2 & 4 \\ -3 & 1} \pmatrix{\frac{1}{\sqrt 14} & 0 \\ 0 & \frac{1}{\sqrt 42}}) (\pmatrix{\sqrt 14 & 0 \\ 0 & \sqrt 42} \pmatrix{1 & \frac{45}{14} \\ 0 & \frac{9}{14}} \pmatrix{1 & -3 & -6 \\ 0 & 1 & \frac{14}{9}}) \\
&= QR
\end{aligned}
$$
例2：
$$
\pmatrix{2 & 1 \\ 1 & 1 \\ 2 & 1}
$$


## 谱分解

* $A = \sum_i \lambda_i A_i$​
* **不唯一**
* 求法
  * $A = P \Lambda P^{-1}$
  * $P = (\alpha_1, \dots, \alpha_n)$
  * $P^{-1} = (\beta_1, \dots, \beta_n)^\top$
  * $A_i = \alpha_i \beta_i^\top$​
* 性质 $A_i A_j \ne 0 \lrArr i = j$

例：
$$
\pmatrix{3 & 0 & 1 \\ 0 & 2 & 0 \\ 1 & 0 & 3}
$$

* $P = \pmatrix{1 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & -1 & 0}$
* $P^{-1} = \frac{1}{2}\pmatrix{1 & 0 & 1 \\ 1 & 0 & -1 \\ 0 & 2 & 0}$
* $\Lambda = \pmatrix{4 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2}$
* ..

## 奇异值分解（SVD分解）

* $A = U \Sigma V^\top$
* $U$ ：正交
* $V$ ：正交
* $\Sigma$​​ ：奇异值对角矩阵
* 求法
  * $A_{m \times n}$
  * 求 $A^\top A$ 的非零特征值，并（由大到小）排序，得到$D_{r \times r} = diag(\sqrt \lambda_1, \dots, \sqrt \lambda_r)$，从而 $\Sigma = \pmatrix{D & 0 \\ 0 & 0}_{m \times n}$
  * 将 $A^\top A$ 对角化，求正交矩阵 $V$ 使得 $V^\top A^\top A V = \pmatrix{D ^ 2 & 0 \\ 0 & 0}$
  * 对 $V$ 分块，取前 $r$ 列 $V = \pmatrix{(V_1)_{m \times r} & V_2}$，该 $V_1$ 即为最终的 $V$ 矩阵
  * $U = A V_1 D^{-1}$​
    * $A = AVV^\top = AV_1 V_1^\top = AV_1 D^{-1} DV_1^\top$
  * 得到 $A = U\Sigma V_1^\top$
  
* **不唯一**

例1：
$$
\pmatrix{1 & 1 \\ 1 & -2 \\ 2 & 1}
$$
例2：
$$
\pmatrix{1 & -1 & 1 \\ -2 & 2 & -2}
$$


# 矩阵分析

## 零化多项式

定义：$A_{n\times n}$，$\phi(\lambda) = a_0 \lambda ^ n + a_1 \lambda ^{n - 1} + \dots + a_{n-1} \lambda + a_n $，使得 $ \phi(A) = 0 $

## 特征多项式

定义：$f(\lambda) = |\lambda E - A|$

注：$f(A) = 0$，$f(\lambda)$ 是 $A$ 的零化多项式

## 最小多项式

定义：$m_A(\lambda)$，首1、次数最低的零化多项式

定理：$m_A(\lambda)$ 的根 $\lrArr$ $A$ 的特征值

注：$m_A(\lambda)$ 不一定等于 $f(\lambda)$​，（重根）

推论：$A \sim \Lambda (= J_A)$  $\lrArr $  $m_A$ 无重根

## 矩阵的极限



## 矩阵函数

$f(A) = \sum a_i A ^ i$

法1：若当标准型

* 若当块单独算
* 拼起来

法2：多项式（ $f(\lambda) \mod m_A(\lambda)$）

## 一阶线性常微分方程组

$$
\frac{d}{dt} x(t) = A x(t) + f(t) \\
x(0)
$$

通解
$$
\begin{aligned}
	x(t)
	&= e^{At} x(0) + e^{At}\int_0^t e^{-Au} f(u) du \\
	&= e^{At} x(0) + \int_0^t e^{A(t-u)} f(u) d
\end{aligned}
$$


# end

# 疑问

* 当 $A$ 不可对角化时，$m_A$​ 是多少（怎么求）？
* 线性变换 $A, B$，$A$ 到 $B$ 的过渡矩阵 $P$，是 $P^{-1} A P = B$ 还是 $PA = B$ 还是 $AP = B$ ？
* 对角化 $A = P B P^{-1}$，线性变化过渡矩阵 $B = P^{-1} A P$