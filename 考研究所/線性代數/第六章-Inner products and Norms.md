$V:$ 向量空間

## 定義
>Let $V$ be a vectors space with Field $F=$($C$ or $R$) an inner product on $V$ is a functions from $V\times V\rightarrow F$，donoted by < , >，satisfying for all $x,y,z\in V$ and $c\in F$
>1. $<x+z,y>=<x,y>+<z,y>$
>2. $<cx,y>=c<x,y>$
>3. $<x,y>=\overline{<y,x>}$(共軛)
>4. $<x,x>>0$ if $x\neq0$
## Ex 1
 ![[Pasted image 20240913215549.png]]
### Ex 2
 ![[Pasted image 20240913215610.png]]
![[Pasted image 20240913215616.png]]
### Ex 3
![[Pasted image 20240913215632.png]]
## 定義
>$V:$ an inner product space
>1. $x,y\in V$ is said to be perpendicular or orthogonal if $<x,y>=0$ $(x\perp y)$
>2. $S\subset V$ is orthogonal if $<x,y>=0$ for all $x,y\in S$
>3. $S\subset V$ is orthonormal if $S$ is orthogonal. and $||x||=1$ for all $x\in S$ 
>4. Let $x\in V$，the length or norm of x is defined to be $||x||=\sqrt{<x,x>}$
### 例子
![[Pasted image 20240913221013.png]]
### 例子2
$H=$ the set of complex-valued continuous functions on $[0, 2\pi]$

$f,g\in H$ $<f,g>=\frac{1}{2\pi}\int^{2\pi}_0f(t)\overline{g(t)}dt$
$t\in[0,2\pi]\ f(t)\in C$

---
$S=\{f_n(t):\ f_n(t)=e^{int}=cosnt+isinnt\}\ n\in Z$
Claim: $S$ is orthonormal.
$<f_n(t),f_n(t)>=\frac{1}{2\pi}\int^{2\pi}_{0}e^{int}e^{-int}dt=1$
$n\neq m$
$<f_n(t),f_m)(t)>$ $=\frac{1}{2\pi}\int^{2\pi}{0}e^{int}e^{-int}dt$
$=\frac{1}{2\pi}\int^{2\in}_{0}e^{i(n-m)t}dt$
$=\frac{1}{2\pi}\int^{2\pi}_0cos(n-m)t+isin(n-m)tdt$
$=\frac{1}{2\pi}\int^{2\pi}_0cos(n-m)t+\frac{i}{2\pi}\int^{2\pi}_0sin(n-m)tdt$
$=0$

## Thm 6.1
>$V:$ an inner product space
>For all $x,y,z\in V$ and $c\in F$
>$\Rightarrow$ 
>1. $<x,y+z>=<x,y>+<x,z>$
>2. $<x,cy>=\bar c<x,y>$
>3. $<x,0>=<0,x>=0$
>4. $<x,x>=0\Leftrightarrow x=0$
>5. Given $y$ and $z$ if $<x,y>=<x,z>$ for all $x\in V$，then $y=z$. 
>   Consequently, if $<x,y>=0$ for all $x\in V$, then y=0.
>

### 證明 (v)
$<y-z,y-z>$
(i)$=<y-z,y>+<y-z, -z>$
$-z=(-1)z$
$=<y-z,y>-<y-z,z>$
$=0$
Let $y-z=x$ (由已知)$\Rightarrow<y-z,y-z>=0$
由(iv) $y-z=0\Rightarrow y=z$

## Thm 6.2
>1. $||cx||=|c|||x||$
>2. $|<x,y>|\leq||x||\ ||y||$ (Cauchy-Schwang inequality) (等式何時成立?)
>3. $||x+y||\leq ||x||+||y||$ (Triangle Inequality)
>4. 若$x\perp y\Rightarrow||x+y||^2=||x||^2+||y||^2$ (畢氏定理)

1. $V=R^2$ $x=(a_1,b_1)\ y=(a_2,b_2)$
$(a_1a_2+b_1b_2)^2\leq(a_1^2+b_1^2)(a_2^2+b_2^2)$
2. $V=C[0,1]$ $<f,g>=\int^1_0f(t)g(t)dt$ (x is $f(t)$；y is $g(t)$)
$(\int^1_0f(t)g(t)dt)^2\leq (\int^1_0f^2(t)dt)(\int^1_0g^2(t)dt)$
3. $V=M_{n\times n}(R)$
相對的$C-S不等式?$

### 證明1
$c\in F$
$<x-cy,x-cy>$
$=<x+x>+<-cy,x>+<x,-cy>+<-cy,-cy>$
$=<x,x>-c<y,x>-\bar c<x,y>+ |c|^2<y,y>$
1. Let $y\neq 0$，choose
   $c=\frac{<x,y>}{<y,y>}$
$\Rightarrow ||x-cy||^2=<x,x>-\frac{|<x,y>^2|}{<y,y>}-\frac{|<x,y>^2|}{<y,y>}+\frac{|<x,y>|^2}{<y,y>^2}<y,y>$
$=<x,x>-\frac{|<x,y>|^2}{<y,y>}\geq0$
$\Rightarrow ||x||^2-\frac{|<x,y>|^2}{<||y||>}\geq0$
2. $y=0\Rightarrow ok!$

### 證明2
$<x+y,x+y>=<x,x>+<y,x>+<x,y>+<y,y>\leq ||x||^2+2||x||\ ||y||+||y||^2$
$=(||x||+||y||)^2$


# 
![[Pasted image 20240914084605.png]]
## Def: orthonormal basis
: 彼此互相垂直，長度為1
Ex: $V=R^3$，$\beta=\{e_1,e_2,e_3\}$ is an orthonormal basis.
### 問: 
Given an inner product space, 此空間是否$\exists$ an orthonormal basis.
Yes $(Thm6.5)$
Why and how? (為什麼一定有?怎麼找?) 

## Thm6.3
>$V:$ inner product set
$\{v_1,...,v_k\}=S:$ orthogonal set of nonzero vectors
$W=$ span($S$)
Then if $w\in W$，then $w=\sum^k_{i=1}\frac{<w,v_i>}{||v_i||^2}v_i$

### 證明
$w=\sum^k_{i=1}a_iv_i$
$=a_1v_1+a_2v_2+...+a_kv_k$
$<w,v_j>=<a_jv_j,v_j>$
$=a_j<v_j,v_j>$
$\Rightarrow a_j=\frac{<w,v_j>}{||v_j||^2}$

### Cor
$S:$ orthonormal
then $a_j=<w,v_j>$
### Cor2
$S$ is linearly independant
#### pf
$\sum^k_{i=1}a_iv_i=0$ (Thm6.3)$\Rightarrow a_i=0$ for all $i$
![[Pasted image 20240914091655.png]]

## Thm6.4 (Gram Schmidt) (answers why and how)
$V:$ inner product space
$\{v_1,v_2,...,v_k\}$ is linear independant.
$w_1=v_1$
$w_j=v_j-\sum^{j-1}_{i=1}\frac{<v_j,w_i>}{||w_i||^2}w_i\ \ 2\leq j\leq k$
$=v_1-v_j$ 投影在$w_i$ ，$1\leq i\leq j-1$，之分量向量
(GS)$\Rightarrow$
1. $\{w_1,w_2,...,w_k\}:$ orthogonal + nonzeros
2. span $\{v_1,v_2,...,v_k\}=$ span$\{w_1,w_2,...,w_k\}$ 


### Pf: Prove by Induction on k
1. $k=1\Rightarrow$ (i) and (ii) are satisfied
2. 假設$k=j-1$，(i)+(ii) 是對的
   $\Rightarrow$ $k=j$ 時(i)+(ii)也是對的
   $w_j=v_j-\sum$
   $<w_j,w_l>$，$l=1$，$j-1$
   $=<v_j-\sum^{j-1}_{i=1}w_i,w_l>$
   $=<v_j,w_l>-<\frac{<v_j,w_l>}{||w_l||^2}w_l,w_l>$
   $=<v_j,w_l>-<v_j,w_l>=0$
   說明$w_j\neq0$
   (如果$w_j=0$$\Rightarrow v_j$ 可以寫成$\{v_i\}^{j-1}_{i=1}$的線性組合(用到induction假設))
   $\Rightarrow$ 當$k=j\Rightarrow$ (i)是對的
   $\Rightarrow k=j\Rightarrow$ (ii)是對的(Trivial)

## Thm6.5
>dim($v$)$<\infty$ $V:$ inner product space
>$\Rightarrow$
>1. $\exists$ an orthonormal basis $\beta=\{v_1,v_2,...,v_n\}$
>2. If $x\in V$，then $x=\sum^n_{i=1}<x,v_i>v_i$

## 定義
> 1. $\beta=\{v_1,..v_n...\}$ be an orthonormal set in $V$
>    Let $x\in V$ .  Then $<x,v_i>=$ the Fourier coefficients of $x$ realative to $\beta$
>    $= x$投影在$V_i$的分量
> 2. Let $S\subset V$
>    Define $S^{\perp}=$ the orthogonal complement of $S$ in $V$ 
>    $=\{x\in V:\ <x,y>=0$ for all   $y\in S\}$ 

### Fact
1. $S^\perp$ is subspace (prove yourself!)
2. $S\bigcap S^\perp=\{0\}$ ，where $S$ is a subspace.

#### pf of (ii)
$0 \in S\bigcap S^\perp$
$x\neq0$，$x\in S\bigcap S^\perp$
$\Rightarrow$ $<x,x>=0$
$\Rightarrow x=0\Rightarrow(\rightarrow\leftarrow)$


### (i)例子
$V=H=$ the set of continuous，complex-valued functions on $[0,2\pi]$
$<f,g>=\frac{1}{2\pi}\int^{2\pi}_0f(t)\overline{g(t)}dt$
$\beta=\{f_n(t)=e^{int}:n\in Z\}$ : orthonormal set
$<f(t),f_n(t)>$
$=\frac{1}{2\pi}\int^{2\pi}_0f(t)e^{-int}dt$
$=$ the $n$th fourier coefficient of $f$ (relative to $\beta$)
#### 傅立葉分析
$f(x)=(?)\sum^\infty_{n=-\infty}<f,f_n>f_n(x)$ (高微)
### (ii)例子
$S={0}\Rightarrow$ $S^{\perp}=V$
$S=V$，$\Rightarrow S^{\perp}=\{0\}.$
$V=R^3$ $S=l$
$S^\perp=$ 過原點和$l\perp$的平面
![[Pasted image 20240914104550.png]]
![[Pasted image 20240914111711.png]]
![[Pasted image 20240914111715.png]]

## Thm6.6
> $V:$ inner, dim($v$)$<\infty$
> $W\subset V$，a subspace. Let $y \in V$
> $\Rightarrow$
> 1. $\exists!\ u\in W$ and $z\in W^\perp$ such that $y=u+z$
> 2. Let $\{v_1,...,v_k\}$ be an orthonormal basis for $V$.  Then $u=\sum^k_{i=1}<y,v_i>v_i$
>    $\Rightarrow||u||^2=\sum^k_{i=1}|<y,v_i>|^2$
>    $<u,u>=\sum^k_{i=1}<<y,v_i>v_i,<y,v_i>v_i>$
 
### 證明
Let $u=\sum^k_{i=1}<y,v_i>v_i\in W$
Let $z=y-u$
Claim: $z\in W^\perp\Leftrightarrow$ $<z,v_i>$ for all $i=1,2,...,k$
$<z,v_i>=<y-u,v_i>=<y,v_i>-<u,v_i>$
$=<y,v_i>-<<y,v_i>v_i,v_i>$
$=<y,v_i>-<y,v_i><v_i,v_i>=0$
$\Rightarrow x\in W$，then $<z,x>=0\Rightarrow z\in W^\perp$

Let $y=u+z=u'+z'$，$u,u'\in W$ and $z,z'\in W$
$\Rightarrow u-u'=z'-z\in W\bigcap W^\perp=\{0\}$
### 應用
1. $||y-u||<||y-x||$ for any $x\in W$. The equality holds only if $x=u$. ($u$ is the best "approximation" to $y$ in $W$)
點到面最短的距離就是垂足的距離
#### 證明
$||y-x||=||y-u+u-x||$   *$(y-u\in W^\perp,\ u-x\in W)$*
*(畢氏定理)*$=||y-u||^2+||u-x||^2\geq||y-u||^2$

### 應用2: Bessel Inequality
$||y||^2\geq\sum^k_{i=1}|<y,v_i>|^2=u^2$
![[Pasted image 20240914174200.png]]

### Thm6.7
$\Rightarrow$
1. $V=W\oplus W^\perp$ (習題)
2. dim($V$)=dim($W$)+dim($W^{\perp}$)
$u=\sum^k_{i=1}<y,v_i>v_i$
 
### Fact
$\frac{\pi^2}{6}\sum^\infty_{n=1}\frac{1}{n^2}$
#### 應用例子
V=H (作用在0~$2\pi$的連續函數)
$<f,g>=\frac{1}{2\pi}\int^{2\pi}_0f(x)\overline{g(t)}dt$
$f(t)=1||f||=1$
$y\rightarrow f(t)=t$
$||y||^2=<f,f>=\frac{1}{2\pi}\int^{2\pi}_0t^2dt$
$=(\frac{t^3}{3}|^{2\pi}_{0})\frac{1}{2\pi}=\frac{4\pi^2}{3}$

---
$S_n=\{f_k(t)=e^{ikt},\ -n\leq k\leq n\}$
$<t,f_k(t)>=\frac{1}{2\pi}\int^{2\pi}_0te^{-ikt}dt$
![[Pasted image 20240914200232.png]]
$\frac{1}{2\pi}\int^{2\pi}_0te^{-ikt}dt=\frac{1}{2\pi}[\frac{te^{-ikt}}{-ik}+\frac{e^{-ikt}}{k^2}]|^{2\pi}_0$ *(後項削掉，e是週期函數)*
$=\frac{1\times 2\pi}{2\pi\times-ik}$ $=\frac{1}{-ik}=<f,f_k(t)>$，$k\neq0$
$k=0\Rightarrow<f,f_0(t)>=\pi$
$\frac{4\pi^2}{3}\geq2\sum^n_{i=1}\frac{1}{k^2}+\pi^2$
$\frac{\pi^2}{6}\geq\sum^n_{k=1}\frac{1}{k^2}$
$\Rightarrow\frac{\pi}{6}\geq\sum^\infty_{k=1}\frac{1}{k^2}=\sum^\infty_{1}{n^2}$
註
$f(t)=t=\sum^{\infty}_\infty<f,f_n>f_n(t)$ (高微)



# The Adjoint of Linear Operator
## 問題:
$V:$ Inner product space
$dim(v)<\infty$
$T:V\xrightarrow{linear}V$
Define $T^*$，the adjoint operator of $T$
## 定義: Adjoint
> $T^*$ is a linear operator from $v$ to $v$ satisfying the following.
> For all $x,y\in V$，we have $<T(x),y>=<x,T^*(y)>$

> Is such definition well-defined?
1. Existence of $T^*$
2. Unique of $T^*$
3. linear?


## Thm6.8
>Let $g:V\rightarrow F$ be linear. Then $\exists! y\in V$ such that $g(x)=<x,y>$
 (Representation of linear functional)
### 例子
$g(x,y)=x+y$
$g:R^2\rightarrow R$
### 證明
Let $\beta=\{v_1,...,v_n\}$ be an orthonomal basis for $V$ 
$x=\sum^n_{i=1}a_iv_i$
$=\sum^n_{i=1}<x,v_i>v_i$

$g(x)=g(\sum^n_{i=1}a_iv_i)=\sum^n_{i=1}a_ig(v_i)$
$=\sum^n_{i=1}<x,v_i>g(v_i)$
$=<x,\sum^n_{i=1}\overline{g(v_i)}v_i>$
Let $y= \sum^n_{i=1}\overline{g(v_i)}v_i$
$=<x,y>$

唯一: $\exists y,y'$ such that 
$g(x)=<x,y>=<x,y'>$
$\Leftrightarrow<x,y-y'>=0$
$x\in  V$
$\Rightarrow y-y'=0\Rightarrow y=y'$

## Thm6.9
Such def. is well-defined.
### 證明
1. Existence: (利用Thm6.8)
   Let $y$ be arbitraily fixed. Define
   $g(x)=<T(x),y>$ ($g:V\rightarrow F$)
	1. $g$和$y$有關
	2. $g$ is linear  (pf hint: T本身是線性)
(由Thm6.8)$\Rightarrow$ $\exists!z\in V$ such that $g(x)=<T(x),y>=$(Thm6.8)$<x,z>$
$y\in V\rightarrow \exists!z\in V$ such that
Define a function $T^*$ such that $T^*(y)=z$
Hence $<T(x),y>=<x,T^*(y)>$ for all $x,y\in V$
2. Uniquences: 
   Suppose $T^*$，$T_1:V\rightarrow V$
   such that $<T(x),y>=<x,T^*(y)>=<x,T_1(y)>$
   $\Rightarrow<x,T^*(y)-T_1(y)>=0$ for all $x,y\in V$
   $\Rightarrow T^*(y)=T_1(y)$ for all $y\in V$
   $\Rightarrow T^*=T$
3. Linear:
   Wanted: $T^*(cy_1+y_2)=cT^*(y_1)+T^*(y_2)$
   $\Rightarrow <x,T^*(cy_1+y_2)>=<x,cT^*(y_1)+T^*(y_2)>$ For all $x$
   $<x,T^*(cy_1+y_2)>$ (特殊證明技巧)
   $=<T(x),cy_1+y_2>$
   $=\bar{c}<T(x),y_1>+<T(x),y_2>$
   $=\bar{c}<x_1,T^*(y_1)>+<x,T^*(y_2)>$
   $=<x,cT^*(y_1)+T^*(y_2)>$

## Thm6.10
問: 如何找$T^*$
>Let $\beta=\{v_1,...,v_n\}$ be an orthonormal basis for $V$. Then $[T^*]_\beta=([T]_\beta)^*$ ($\Leftrightarrow B=A^*$)
### 證明
Let $A=[T]_\beta$ and $B=[T^*]_\beta$
$B_{ij}=<T^*(v_j),v_i>$
($T^*(v_j)$)$=<>v_1+<>v_2+...+<,v_i>v_i+...+<>v_n$
$=\overline{<v_i,T^*(v_j)>}$
$=\overline{<T(v_i),v_j>}$
$=\overline{A_{ji}}$
(adjoint)$=(A^*)_{ij}$ for all $i,j$
$\Rightarrow B=A^*$

### Remark
1. If $\beta$ is not an orthonormal, then the theorem is not true! (why? 找一反例)
2. Cor $(L_A)^*=L_{A^*}$|
   $L_A(x)=A_x$
   $(L_A)^*=L_{A^*}$
   $L_{A^*}(x)=A^*x$ (Thm6.10)
   (Hint: Needed: $[(L_A)^*]_\beta=[L_{A^*}]_\beta$)
   $[L_A]_\beta=A$
   $\beta=$ the standard basis
3. dim($V$)$=\infty$，$T^*$不見得存在(\#24)
## 例子
$T: F^2\rightarrow F^2$
$T(a_1,a_2)=(2ia_1-3a_2,a_1+a_2)$
$[T]_{\beta}$，$\beta=\{e_1,e_2\}$
(1,0)
$T(e_1)=(2i,1)=2ie_1+e_2=<T(e_1),e_1>e_1$
(0,1)
$T(e_2)=(-3,1)$
$A=\begin{pmatrix}<T(e_1),e_1>&<T(e_2),e_1>\\<T(e_1),e_2>&<T(e_2),e_2>\\\end{pmatrix}$
$A=\begin{pmatrix}2i&-3\\1&1\\\end{pmatrix}$
$[T^*]_\beta=$*(Thm3.10)* $\begin{pmatrix}-2i&1\\-3&1\\\end{pmatrix}$
$\Rightarrow T^*(a_1,a_2)$
$=(-2ia_1+a_2,-3a_1+a_2)$
## Thm6.11 ($T^*$的運算性質)
> 1. $(T+U)^*=T^*+U^*$
> 2. $(cT)^*=\bar{c}T^*$
> 3. $(TU)^*=U^*T^*$
> 4. $T^{**}=T$
> 5. $I^*=I$
### Cor
$T\rightarrow A$
$U\rightarrow B$
(換成矩陣也對)
### 證明
#### 4
Wanted: $T^{**}=T\Leftrightarrow<x,T^{**}(y)>=<x,T(y)>$ for all $x,y\in V$
$<x,T^{**}(y)>=<T^*(x),y>$
$=\overline{<y,T^*(x)>}=\overline{<T(y),x>}$
$=<x,T(y)>$ for all $x,y$
$\Rightarrow T^{**}(y)=T(y)$ for all $y$
$\Rightarrow T^{**}=T$




## 應用
1. Least Square Problems
2. Find "minimum" solution to $Ax=b$
### Data Fitting
$(t_i,y_i),\ i=1,2,...,m$
問: Find a "best" line to represent those data 
![[Pasted image 20240916064613.png]]
What is a-best?
$E=$ 全部的誤差
$\sum^n_{i=1}(y_i-(t_i-d))^2$
Goal: E is a minimum
#### 1. 微積分方法(23*)
找$c$ 和$d$ such that E 最小
$c\rightarrow x$，$d\rightarrow y$
$t_i\rightarrow a_i$
$y_i\rightarrow b_i$
$f(x,y)=\sum^n_{i=1}(b_i-a_ix-y)^2$
求絕對最小值
#### 2. Linear Algebra's Method
$A=\begin{pmatrix}t_1&1\\t_2&1\\...\\t_m&1\\\end{pmatrix}$，$x=\begin{pmatrix}c\\d\\\end{pmatrix}$，$b=\begin{pmatrix}y_1\\y_2\\...\\y_m\\\end{pmatrix}$
 二次多項式
 $A=\begin{pmatrix}t_1^2&t_1&1\\t_2^2&t_2&1\\...\\t_m^2&t_m&1\\\end{pmatrix}$，$x=\begin{pmatrix}a\\b\\c\\\end{pmatrix}$，$b=\begin{pmatrix}y_1\\y_2\\...\\y_m\\\end{pmatrix}$

#### 應用
##### 問: 
Given $A\in M_{m\times n}(F)$ and $b\in F^m$，find an $x_0\in R^n$ such that $||Ax_0-b||$ is a minimum
##### 例子
Given a set $\{(t_i,y_i)\}^m_{i=1}$ of measurements, find a "best" polynomial of degree $n-1$ to represent such set of measurements.
![[Pasted image 20240916070732.png]]
這類問題稱為least square problems
解:
  
Step1: 將$b$投影到$W=R(A)$之子空間得$u$
Step2. $u=Ax_0$，$x_0$即為解
Step3. 若rank($A$)$=n$，則有唯一解$x_0=(A^*A)^{-1}A^*b$

2. Claim: $x_0$ is a solution to the problem. 
Wanted: $||Ax_0-b1||\leq ||Ax-b||$ for any $x\in F^n$
##### pf
$||Ax-b||=||Ax_0-b+Ax-Ax_0||$
$=||Ax_0-b||^2+||Ax-Ax_0||^2\geq ||Ax_0-b||^2$
##### Pf 3
$b-Ax_0\perp W=R(A)$
$\Rightarrow<Ax,b-Ax_0>$ for all $x\in F^n$
$\Rightarrow<x,A^*(b-Ax_0)>=0$ ，$x\in F^n$
$[(L_A)^*=L_{A^*}]$
$\Rightarrow A^*(b-Ax_0)=0$
$A^*Ax_0=A^*b$
(Recall: $A^*A\in M_{n\times n}(F)$) *$A:m\times n$，$A^*:n\times m$*
If rank($A^*A$)$=n$，then $A^*A$ is inventible
$\Rightarrow x_0=(A^*A)^{-1}A^*b$
![[Pasted image 20240916142250.png]]
##### Lemma1
Given $A\in M_{m\times n}(F)$，then $<Ax,y>_m=<x,A^*y>_n$ (內積維度m，n)

###### pf
$<Ax,y>_m=y^*Ax=(y^*A)x=(A^*y)^*x=<x,A^*y>_n$
($(AB)^*=B^*A^*$， $A^{**}=A$)
$<a,b>=b^*a=\sum^n_{i=1}a_i\bar{b_i}$
$a=\begin{pmatrix}a_1\\...\\a_n\\\end{pmatrix}$
$b=\begin{pmatrix}b_1\\...\\b_n\\\end{pmatrix}$
$b^*=(\bar{b_1},\bar{b_2},...,\bar{b_n})$







##### Lemma2
Given $A\in M_{m\times n}(F)$，if $rank(A)=n$，then rank$(A^*A)=n$
###### pf
Recall: Dimension Theorem
$n=Nullity(A)+rank(A)$
$=Nullity(A^*A)+rank(A^*A)$
只要證 $N(A)=N(A^*A)$
If $x\in N(A)$ then $Ax=0$
$\Rightarrow A^*Ax=0\Rightarrow x\in N(A^*A)$
$\Rightarrow N(A)\subset N(A^*A)$
If $x\in N(A^*A)$，then $A^*Ax=0$
$0=<x,A^*Ax>=<Ax,Ax>=||Ax||^2$
$\Rightarrow Ax=0\Rightarrow x\in N(A)$
$\Rightarrow  N(A^*A)\subset N(A)$


##### Remark
$t_i$，$i=1,2,...,m$. be all distinct. assume $m\geq n$
$\Rightarrow rank(A)=n$

### Data Analys
(Hilbent Huang Transform)
### Finding the minimum solution of $Ax=b$

問: Given a consistant system $Ax=b$，find a solution S so that $A\in M_{m\times n}$ 
$||s||\leq||x||$ for any $x$ satisfying $Ax=b$

解:
1. 找在一解$x$ (i.e. $Ax=b$)
2. 將$x$ 投影到$Range(A^*)$
3. $S$ 即為唯一的最小解
4. 實作上如何找$S$
![[Pasted image 20240916142721.png]]
##### 3. Why?
a. $S:$ 最小解
$s=x+v$，
$s\in Range(A^*)$
$v\in N(A)$
$\Rightarrow Ax=A(s+v)$
$b=As+Av=As$
$\Rightarrow s$是解
Let $x$ be any sol. of $Ax=b$
$\Rightarrow x-s\in N(A)\Rightarrow \exists x_0\in N(A)$ such that
$x-s=x_0$$\Rightarrow x=s+x_0\ (s\perp x_0)$
*(畢)* $\Rightarrow$ $||x||^2=||s||^2+||x_0||^2\geq||s||^2$
$\Rightarrow$ $s:$ 最小解
b. Let x, be another solution of $Ax=b$
Let $s_1$ be such that $x_1=s_1+v_1$, where $s_1\in Range(A^*)$ and $v_1\in N(A)$
Wanted: $S=S_1$
$\Rightarrow S-S_1$，$\in N(A) \begin{bmatrix}As=b\\As_1=b\\\end{bmatrix}=W^\perp$
$s-s_1\in Range(A^*)=W$
$\Rightarrow s-s_1\in W^\perp\bigcap W=\{0\}$
$\Rightarrow s=s_1$
![[Pasted image 20240916152721.png]]
##### 實作上如何找S

$As=AA^*x_1$
$b=AA^*x_1$
Step1: 找任一$x_1$，滿足$AA^*x_1=b$
$AA^*x=b$
Step2: $S=A^*x_1$
###### Remark
$AA^*\in M_{m\times m}(F)$
1. If rank($AA^*$)$=m$
$\Rightarrow s-A^*(AA^*)^{-1}b$
2. If rank($A$)$=m$，then rank($AA^*$)$=m$
![[Pasted image 20240916152711.png]]

#### Lemma3 
Let $A\in M_{m\times n}(F)$
$\Rightarrow$
1. $N(A)=$ (Range$(A^*)$)$^\perp$
2. $N(A)^{\perp}=$ Range($A^{*}$)
3. $F^n=$ Range($A^*$)$\oplus N(A)$
##### Pf of 1
$x\in F^n$
$x\in N(A)$
$\Rightarrow Ax=0$
$<Ax,y>=0$ for all $y\in F^m$
$\Rightarrow <x,A^*y>=0$ for all $y\in F^m$
$\Rightarrow x\in (Range(A^*))^\perp$
(也可回推)
$\Rightarrow N(A)=(Range(A^*))^\perp$

 
# Normal and Self-adjoint Operators

可對角線化?
只要知道長相就可以知道可不可對角線化
Normal: $AA^*=A^*A$
$A$ 可對角線化$\Leftrightarrow$ $A$ is normal
## Lemma
> dim($V$)$<\infty$，$V:$ inner product space
> If $T$ has an eigenvector, so does $T^*$

### 證明
$\exists v\neq0$，such that $Tv=\lambda v$，
$\lambda\in F\Rightarrow$$(T-\lambda I)v=0$
$0=<(T-\lambda I)v,y>$ for any $y\in V$
$=<v,(T-\lambda I)^*y>$
$=<v,(T^*-(\lambda I)^*)y>$
$=<v,(T^*-\bar{\lambda}I)y>$ for any $y\in V$
$\Rightarrow N(T^*-\bar{\lambda}I)\neq \phi$ *(Dimension Thm.)*
$\exists u\neq 0$ such that
$(T^*-\bar{\lambda}I)u=0$
$u$ is an e.v. of $T^*$

## Thm 6.14(Schur)
> Suppose the $CP$ of $T$ splits. Then $T$ can be triangularized. More specifically, $\exists$ an orthonormal basis $\gamma$ such that $[T]_\gamma$ is coppen triangular.

### Remark
1. 若$F=C\Rightarrow$ 任一定義在有限維內積空間的算子皆可三角形化
2. 即若$A\in M_{m\times m}(C)$，則$A$可三角形化，更正確說。$\exists Q:$ unitary such that $U=Q^*AQ$，where $Q^*=Q^{-1}$ and $U$ 是上三角形矩陣
3. Matrix version: $A\in M_{n\times n}(C)$
4. $T$ 可對角化的必要條件
   If $[T]_\gamma:$ diagonal
   then $TT^*=T^*T$
5. If $T^*T=TT^*\Rightarrow T:$ diagonalizable
6. $T$ is normal $\Leftrightarrow[T]_\gamma$，
   $\gamma:$orthonormal basis, is normal

## Def's 
$T:$ normal if $TT^*=T^*T$ (算子)
$A:$ normal if $AA^*=A^*A$



### pf
Let dim($V$)$=n$
We prove by the math induction
1. $n=1$ (對)
2. Suppose the theorem holds
true for n-1
(由Lemma)$\Rightarrow \exists z\neq0$ unit vector
such that $T^*z=\lambda z$
Let $w=$ Span$\{z\}$ $=\{cz:c\in F\}$
$dim(w)=1$ is dim($W^\perp$)$=n-1$
Claim: $W^\perp$ is T-invaniant
$[T:W^\perp\rightarrow W^\perp]$
Wanted: $y\in W^\perp\Rightarrow T(y)\in W^\perp$
$y\in W^\perp\Rightarrow<y,cz>=0\Rightarrow \bar c<y,z>=0$
$<T(y),cz>=<y,T^*(cz)>$
$\bar c<y,T^*(z)>=\bar<y,\lambda z>$
$=\overline{\lambda c}<y,z>=0$
The $CP$ of $T_{W^\perp}$ is splits
(因為 $CP$ of $T_v$ splits +  $CP$ of $T_{W^\perp}$ diveides that of $T_v$)
*(Math Induction)* $\exists\beta:$ orthonormal such that
$[T_{W^\perp}]_\beta$ is upper triangular

$V=W\oplus W^\perp$
![[Pasted image 20240916162247.png]]


## Thm6.15
$T:$ normal
1. $||T(x)||=||T^*(x)||$
2. $T-cI$ is normal for any $c\in F$
3. If $T(x)=\lambda x$，$x\neq 0$，$\lambda\in F$，then $T^*(x)=\bar{\lambda}x$
4. If $T(x_1)=\lambda_1x_1$ ，$T(x_2)=\lambda_2x_2$， $x_1\neq0$，$x_2\neq0$，and $\lambda_1\neq\lambda_2\Rightarrow$ $x_1\perp x_2$
 
### Pf of 1
$||T(x)||^2=<T(x),T(x)>$
$=<x,T^*T(x)>=$ *(normal)* $<x,TT^*(x)>$
$=<T^*(x),T^*(x)>=||T^*(x)||^2$
### Pf of 2
Obvious! (Since $(CI)^*=\bar c I$)
### Pf of 3
$T(x)=\lambda x\Rightarrow(T-\lambda I)(x)=0$
$0=||(T-\lambda I)(x)||=$*(i)* $||(T-\lambda I)^*x||$
$=||(T^*-\bar\lambda I)(x)||$
$\Rightarrow(T^*-\lambda I)(x)=0\Rightarrow T^*(x)=\bar\lambda x$
### Pf of 4
$\lambda_1<x_1,x_2>=<\lambda_1x_1,x_2>=<T(x_1),x_2>$
$=<x,T^*(x_2)>=$ *(iii)* $<x_1,\bar{\lambda_2}x_2>$
$=\lambda_2<x_1,x_2>\Rightarrow(\lambda_1-\lambda_2)<x_1,x_2>=0$
$\Rightarrow <x_1,x_2>=0\Rightarrow x_1\perp x_2$

## Thm6.16 
dim($V$)$<\infty$: $V:$ Complex
inner product space then $T$ is normal $\Leftrightarrow$ $\exists r:$ orthonormal basis s.t. $[T]_\gamma$ is diagonal.
### remark
1. dim($V$)$<\infty$ (必要)
   Ex: 反例
   $S=\{f_n(t): n\in Z\}$
   $f_n(t)=e^{in5}$
   $<f_n,f_n>=\frac{1}{2\pi}\int^{2\pi}_0f_(t)\overline{f_m(t)}dt$
   $V=span S$
   dim($V$) 不是有限
   $T:V\rightarrow V$
   $T(f)=f_1f$
   有限維算adjoint
![[Pasted image 20240916180143.png]]
   What is $T^*$?
   $<T(f_n),f_m>$
$=<f_n,T^*(f_m)>$
Wanted$=<f_n,U(f_m)>$
$\forall n,m\in Z$
For any $n,m\in Z$
$<f_n,T^*(f_m)>$
$=<T(f_n),f_m>$
$=<f_{n+1},f_m>$
$=\delta_{n+1,m}=\{\begin{matrix}0，& m\neq n+1\\1，&m=n+1\\\end{matrix}.$
$=\delta_{n,m-1}=\{\begin{matrix}0，&m-1\neq n\\1，&m-1=n\\\end{matrix}.$
$=<f_n,f_{m-1}>=$*Wanted*$<f_n,U(f_m)>$
$U(f)=f_{-1}f$ $\Rightarrow T^*=U$
$\Rightarrow TT^*(f)=T^*T(f)=I(f)$
Claim: Such T has no eigenvectors
$T(f)=\lambda f$，where $f\not\equiv0$
$f\in V$
$T(f)=\lambda f$， where $f\not\equiv0$
$f\in V\Rightarrow f=\sum^m_{i=n}a_if_i$，where $n,m\in Z$
and $a_m\neq0\Rightarrow\sum^m_{i=n} a_iT(f_i)=\lambda \sum^m_{i=n}a_if_i$
$\Rightarrow\sum a_if_{i+1}=\lambda\sum a_if_i$
$a_mf_{m+1}+$剩項$=右邊$
$f_{m+1}=\frac{1}{a_m}(其他f_i表示)$


2. $F=C$(必要)
   $A=\begin{pmatrix}cos\theta&-sin\theta\\sin\theta&cos\theta\\\end{pmatrix}\in M_{2\times 2}(R)$ is normal
   $A^*=\begin{pmatrix}cos\theta&sin\theta\\-sin\theta&cos\theta\\\end{pmatrix}=\begin{pmatrix}cos(-\theta)&-sin(-\theta)\\sin(-\theta)&cos(-\theta)\\\end{pmatrix}$
   $AA^*=I=A^*A$ ($A$不可對角線化)

---
$A=\begin{pmatrix}cos\theta&-sin\theta\\sin\theta&cos\theta\\\end{pmatrix}\in M_{2\times 2}(C)$ is normal
$\Rightarrow A$ 可對角線化

1. Matrix version
$A\in M_{n\times n}(C) L_A: F^n\rightarrow F^n$
$A$ is normal $\Leftrightarrow$ $\exists$ an orthonormal basis $\beta=\{v_1,v_2,...,v_n\}$
s.t $Q^{-1}AQ=D$
where $Q=(v_1,v_2,...v_n)$
In fact $Q^{-1}=Q^*$
($Q^*Q=QQ^*=I$)


4. 找到orthonormal basis
![[Pasted image 20240916174359.png]]




### pf:
由Thm6.14.
$\Rightarrow\exists \gamma:$ orthonormal
$\gamma=\{v_1,v_2,...,v_n\}$
s.t. $[T]_\gamma:$ upper triangular
Let $A=[T]_{\gamma}$
$T(v_1)=A_{11}v_1$ *($A_{11}\ is\ e.v$，$v_1\ is\ e.v.$)*
$T(v_2)=A_{12}v_1+A_{21}v_2$
![[Pasted image 20240916173104.png]]
$A_{12}=0$
$A_{12}=<T(v_2),v_1>$
$=<v_2,T^*(v_1)>$
$=<v_2,\overline{A_{11}}v_1>$

$A_{11}<v_2,v_1>=0$ ($v_1\perp v_2$)
同理: $T(v_3)=A_{13}v_1+A_{23}v_2+A_{33}v_3$
claim: $A_{13}=A_{23}=0$
$A_{23}=<T(v_3),v_2>=<v_3,T^*(v_2)>$
$=<v_3,\overline{A_{22}}v_2>=A_{22}<v_3,v_2>=0$


## 定義
1. $T:$ self-adjoint(Hermitian)
	$\Leftrightarrow T^*=T$
2. A: self adjoint(Hermitian)
   $\Leftrightarrow A^*=A$
### 例子
self-adjoint$\Rightarrow$ Normal
($T^*T=TT^*$)
real symmetric $A:$ 

## Thm6.17 (How about $F=R$)
$F=R$
>Then $T$ is self-adjoint$\Leftrightarrow \exists$ an orthonormal basis $\beta=\{$eigenvectors$\}$
### 證明
$(\Rightarrow)$ From Lemma，the $CP$ of $T$ splits.
代Schur Thm
$\Rightarrow \beta:$ orthonormal s.t.
![[Pasted image 20240916215526.png]]
$(\Leftarrow)$
$\Rightarrow[T]_\beta=D$，a diagonal.
$\Rightarrow D_{ii}=$ the eigenvalues $\in R$
$\Rightarrow D$ self-adjoint. $\Rightarrow T:$ self-adjoint.


### Remark
1. $A\in M_{n\times n}(R)$
	$A^t=A$ (self-adjoint)
2. Matrix Version


## Lemma: 
$T:$ self-adjoint
$\Rightarrow$
1. If $T$ has an e.v. $\lambda$，then $\lambda \in R$
2. Indeed，all eigenvalue exist and，hence，all real.
### 證明1
$T(x)=\lambda x$，where $x\neq0$
$T^*(x)=\bar{\lambda}x$ (因為$T$ normal)
($x\neq0$)$\Rightarrow \lambda=\bar{\lambda}$$\Rightarrow \lambda$ is real
### 證明2
Let $\beta:$ orthonormal basis
Let $[T]_\beta=A\in M_{n\times n}(C)$
$\Rightarrow$ the $CP$ of $A$ splits
$=$ the $CP$ of $T$
$T:$ self-adjoint $\Rightarrow A:$ self-adjoint
$\Rightarrow T$ has eigenvalue that are all real


# Unitary and Orthognal Operators
Recall $Q=(v_1,v_2,...,v_n)$
$\{v_i\}_{i=1}^n$: orthonormal basis
$Q^{-1}=Q^*$
## 定義
> 1. $F=C$，$T:$ unitary if $T^{-1}=T^*$ (i.e. $TT^*=T^*T=I$)
> 2. $F=R$. $T:$ orthogonal...

## Thm6.18
TFAE(下面全部等價)
(a) $T^*T=TT^*=I$
(b) $<T(x),T(y)>=<x,y>$ for all $x,y\in V$ (保角加(保長))
(c) $\forall \beta:$ orthonormal basis 
$\Rightarrow T(\beta):$ orthonormal basis
$T(\beta)=\{T(v_1),...,T(v_n)\}$
(d) $\exists \beta$，orthonormal basis$\Rightarrow$ $T(\beta)$: orthonormal basis
(e) $||T(x)||=||x||$ for all $x\in V$ (保長)
($T\rightarrow 矩陣A$)

### 證明
### $(1)\Rightarrow(2)$
$<T(x),T(y)>=<x,T^*T(y)>$
(1)$=<x,y>$ $\forall x,y\in V$
### $(2)\Rightarrow(3)$
$<T(v_i),T(v_j)>$
*(2)*$=<v_j,v_j>$
$=\delta_{ij}=\{\begin{matrix}1&i=j\\0&i\neq j\\\end{matrix}.$
### $(3)\Rightarrow(4)$
Trivial
### $(4)\Rightarrow(5)$
Let $\beta=\{v_1,...,v_n\}$
Let $x=\sum^n_{i=1}\alpha_iv_i$
$||T(x)||^2=<T(x),T(x)>$
$=<\sum^n_{i=1}\alpha_iT(v_i),\sum^n_{i=1}\alpha_iT(v_i)>$
$=\sum^n_{i=1}<\alpha_iT(v_i),\alpha_iT(v_i)>$
$=\sum^n_{i=1}|\alpha_i|^2<T(v_i),T(v_i)>$
*(4)*$=\sum^n_{i=1}|\alpha_i|^2=<x,x>=||x||^2$
### $(5)\Rightarrow(1)$
$T^*T=I$
$<x,T^*T(y)>=<x,I(y)>$ for $\forall x,y$
$\Leftrightarrow$
$<x,(I-T^*T)y>=0$ $\forall x,y$
Note that $(I-T^*T)^*=I^*-T^*T^{**}=I-T^*T$
#### Lemma 
>Let $U$ be self-adjoint and $<x,Ux>=0\Rightarrow U=0$ *(零函數)*
##### 證明
$U:$ self-adjoint. $\exists\beta=\{$eigenvectors$\}$
$=$ orthonormal basis
Let $v\in \beta$ $<v,V(v)>=0=<v,\lambda v>=\bar{\lambda}<v,v>$
 $\bar{\lambda}=\lambda=0\Rightarrow U(v)=\lambda v=0$

Claim:  $I-T^*T=0$ (零函數)
$\Rightarrow$ self-adjoint
if $<x,(T^*T-I)x>=0$ then we are done!

Check: $<x,(T^*T-I)x>=<x,T^*T(x)>-<x,x>$
$=<T(x),T(x)>-<x,x>$
*(已知)*$=0$

## Def
$A\in M_{n\times n}(C)$
$A^*A=AA^*=I$
$\Rightarrow A:$ unitary matrix
$A\in M_{n\times n}(R)$
$A^*A=AA^*=I$
$\Rightarrow A:$ orthonormal


## Cor 1
$T:$ self-adjoint+orthogonal
$\Leftrightarrow$
$\exists \beta=\{e:$ eigenvectors$\}=$ orthonormal basis and $|\lambda|=1$，$\lambda:$ any eigenvalue of T
($\lambda=1$ or $\lambda=-1$)
### Pf of Cor1
$(\Rightarrow)$ 由之前定理
$\exists \beta=\{v_1,...,v_n\}$
$=$ orthonormal basis
$=\{$ eigenvectors$\}$
$T(v_i)=\lambda_iv_i$
$||T(v)||=||\lambda_iv_i||=||\lambda_i||||v||=||v||$
$\Rightarrow|\lambda_i|=1$
$(\Leftarrow)$ 之前定理
$\Rightarrow T:$ self-adjoint
$\Rightarrow T:$ orthogonal $\Leftrightarrow T^*T=I=TT^*$
$=$ Need to be proved

## Cor2
$F=C$
$T:$ unitary
$\Leftrightarrow$
$\exists\beta=\{$ eigenvectors$\}$
$=$ orthonormal basis
and
$|\lambda|=1$，$\lambda:$ any eigenvector of $T$

## Thm 6.19、20、21
自行閱讀


## 應用
### 2nd Derivative Test
$f:$ $D\subset R^2\rightarrow R$ : smooth
$a:$ critical point. 
$f_x(a)=0$ ，$f_y(a)=0$
$f(x)=x^3$ $f'(0)=0$

可推廣到
$f:R^n\rightarrow R$

---
1. $f: R^n\rightarrow R$ 求極值問題
2.  The classification of Quadratic family
### $f: R^n\rightarrow R$ 求極值問題
![[Pasted image 20240917225311.png]]
![[Pasted image 20240917225320.png]]
![[Pasted image 20240917225327.png]]


2nd Derivative Test
>$f:R^n\rightarrow R$
>$f:$夠 smooth
>$(\Rightarrow H$:$ symmetric$)$
>$a=(a_1,a_2,...,a_n)$ is a $CP$ of $f$
>($f_i(a)=0$，here $f_i=\frac{\partial f}{\partial x_i}$)
>Let $H=(f_{ij}(a))_{n\times n}$
>Here $f_{ij}(a)=\frac{\partial^2f}{\partial x_j\partial x_i}$
>$=$ Hessian matrix $f$ at $a$
>$\Rightarrow$
>1. $\lambda_i > 0$ for all $i$ *($\lambda_i$ is evs of $H$)*
>   $\Rightarrow f(a)$ is a local min.
>2. $\lambda_i < 0$ for all $i$
>   $\Rightarrow f(a)$ is a local max.
>3. $\exists \lambda_i,\lambda_j$ such that $\lambda_i$，$\lambda_j<0$
>   $\Rightarrow a$ is a saddle point.
>4. Otherwise, the test fails.

### 證明
$u=(u_1,u_2,...,u_n)$，$\sum^n_{i=1}u_i^2=1$
$f_u=<f_1,f_2,...,f_n>u$
$=f_1u_1+f_2u_2+...+f_nu_n$
$\Delta f_u=<f_{11}u_1+f_{21}u_2+...+f_{n1}u_n,...>$
![[Pasted image 20240917214935.png]]
$f_{uu}(a,b)=u^tHu$
$H=(f_{ij}(a))$



![[Pasted image 20240917222655.png]]

##  The classification of Quadratic family

$ax^2+bxy+cy^2+dx+ey+f=0$
$\rightarrow$ 平移消去一次項
$a'x^2+b'xy+c'y^2+f'=0$
$(x,y)\begin{pmatrix}a'&\frac{b'}{2}\\\frac{b'}{2}&c'\\\end{pmatrix}\begin{pmatrix}x\\y\\\end{pmatrix}+f=0$
$ax^2+by^2+cz^2+dxy+eyz+fzx=g$
$\Leftrightarrow$
$(x,y,z)H\begin{pmatrix}x\\y\\z\\\end{pmatrix}=f$
$H=\begin{pmatrix}a&\frac{d}{2}&\frac{f}{2}\\\frac{d}{2}&d&\frac{e}{2}\\\frac{f}{2}&\frac{d}{2}&c\\\end{pmatrix}Q$
n=2
$ax^2+2bxy+cy^2=f$
$H=\begin{pmatrix}a&b\\b&c\\\end{pmatrix}$
$(x,y)H\begin{pmatrix}x\\y\\\end{pmatrix}=f$
$\exists Q:$orthogonal
$Q^tHQ=D=\begin{pmatrix}\lambda_1&0\\0&\lambda_2\\\end{pmatrix}$
$H=QDQ^t$
$(x,y)QD(Q^t\begin{pmatrix}x\\y\\\end{pmatrix})=f$
$(x',y')D\begin{pmatrix}x'\\y'\\\end{pmatrix}=f$
$Q^t\begin{pmatrix}x\\y\\\end{pmatrix}=\begin{pmatrix}x'\\y'\\\end{pmatrix}$
$\lambda_1(x')^2+\lambda_2(y')^2=f$
旋轉$=\begin{pmatrix}cos\theta&-sin\theta\\sin\theta&cos\theta\\\end{pmatrix}=orthogonal$
$AA^t=I$
## Thm 6.2?
$A\in M_{2\times 2}(R)$ $A:$ orthogonal
$\Rightarrow A:$ 旋轉or 反射
![[Pasted image 20240917224655.png]]

![[Pasted image 20240917225243.png]]

# Orthogonal Projections and the Spoctral Theorem

## 定義
1. $T:V\rightarrow V$ is called a projection on $W_1$，along $W_2$ if $\exists w_1,w_2$，subspaces, such that $v=w_1\oplus w_2$ and
   $f\ x=u+v,u\in W,v\in W_2$
   then $T(x)=u$ 
![[Pasted image 20240918095733.png]]
2. $T:V\rightarrow V:$ inner projuct space
   $T$ is an orthogonal projection. if
   1. $T$ is a projection
   2. $R(T)^\perp=N(T)$ and $R(T)=N^\perp(T)$
![[Pasted image 20240918100112.png]]
### Facts
1. $W_1=R(T)$ and $W_2=N(T)$
2. $T$ is a projection $\Leftrightarrow T^2=T$
   自己證

## Thm6.24
dim($V$)$<\infty$，$V:$ inner product space
$T$ is an orthogonal projection
$\Leftrightarrow$ ($\exists T^*:$exists)  $T^2=T=T^*$
$(\Leftarrow)$
自己練習
$(\Rightarrow)$
1. $T^2=T$
2. $T=T^*$ $\Leftrightarrow$$<X,T(y)>=<T(x),y>$ for all $x,y\in W$
wanted : $<x,T(y)>=<x,T(y)>$
Let $x=x_1+x_2$，$x_1\in R(T)$，$x_2\in N(T)$
$y=y_1+y_2$，$y_1\in R(T)$，$y_2\in N(T)$

$<x,T(y)>=<x_1+x_2,T(y_1+y_2)>$
$=<x_1+x_2,y_1>$
$=<x_1,y_1>$

---
$<T(x),y>=<T(x_1+x_2),y_1+y_2>$
$=<x_1,y_1+y_2>=<x_1,y_1>$
$T:$ orthogonal projection
$T$ 是否對角線化?
$[T]_\beta:\exists\beta:$ orthonormal basis 
$\rightarrow=[\ ]?$
$T:$ ev's(?)
$T:$ projection可否對角線化?
$T:$ ev's (?)
## Thm6.25 (The Spectral Thm)
>dim($T$)$<\infty$. $V:$ inner product space
$T:$ 1. Normal if $F=C$
or 2. Self-adjoint if $F=R$

($\Rightarrow \exists$ orthonormal basis $=\{eigenvectors\}$
spectrum=${all\ ev's}$
spectral 的形容詞

>Let $\lambda_i,i=1,2,...,k$，be all distinct eigenvalue of $T$. Then
>$\Rightarrow$ 1. $V=E_{\lambda_1}\oplus E_{\lambda_2}\oplus ...\oplus E_{\lambda_k}$ and $E_{\lambda_i}\perp E_{\lambda_j}$ if $i\neq j$
>2. $T=\sum^k_{i=1}\lambda_iP_i$，where $P_i$ are orthogonal projections on $E_{\lambda_i}$ along $E_{\lambda}^\perp$

---
### 證明
Let $x\in V$，$x=u_1+...+u_k$，where $u_i\in E_{\lambda_i}$ $T(x)=\sum^k_{i=1}T(u_i)$
$=\sum^k_{i=1}\lambda_iu_i$
$\sum^k_{i=1}\lambda_iP_i(x)$
$T\Rightarrow \sum^k_{i=1}\lambda_iP_i$
 ![[Pasted image 20240918105741.png]]


# Singular Value Decompisition
$T: V\rightarrow V$
($前V:\beta$，$後V:\gamma$)
$\exists$ an orthonormal basis $\beta=\{$eigenvectors$\}$
$T:V\rightarrow W$

---
$A:F^n\rightarrow F^m$
$A\in M_{m\times n}(F)$

## Matrix version for Singular value decompisition
## Thm6.27(?)
Let $A\in M_{m\times n}(F)$
1. rank($A$)$=k$
$\Rightarrow$
$\exists U=(u_1,u_2,...,u_n)$ and $V=(v_1,v_2,...,v_n)$，$U,V:$ unitary
such that 
$V_{m\times m}^* A_{m\times n}U_{n\times n}=\sum\rightarrow m\times n=\begin{pmatrix}\lambda_1&&0\\&\lambda_k&\\0&&0\\\end{pmatrix}_{m\times n}$，
where $\lambda_i>0$，$i=1,2,...,k$，and $\lambda^2$，$i=1,2,...,k$，are nonzero eigenvalues of $A^*A$，
$A^*Au_i=\{\begin{matrix}\lambda_i^2u_i，&i=1,2,...k\\0u_i，&i=k+1,...,n\\\end{matrix}.$
($u_i$ are eigenvectors of $A^*A$)

### Remark
1. $\lambda_i$ are called singular value of $A$
2. $\sum$ is called a SVD of $A$
3. $I_n$ the proof, one can see how we can contract $v_i$
4. $k\leq min\{m,n\}$
5. rank($A$)$=k$$\Rightarrow$ rank($A^*A$)$=k$ ($A^*A$ 方陣) $=k$
6. $A^*A$ ev's $k$個是正，有$n-k$個是0
#### Pf of 6
Claim: $\lambda_i$: ev's of $A^*A$
$\Rightarrow \lambda_i\geq 0$
$\lambda_i<x,x>=<\lambda_ix,x>=<A^*Ax,x>$
(eigenvector)
$<Ax,Ax>\geq 0$
$\Rightarrow \lambda_i>0$

$A^*A:$ self-adjoint
$\Rightarrow\exists U=(u_1,...,u_n),\ \{u_i\}=\{eigenvectors\}$，
$U:$ unitary such that
$U^*A^*AU=\begin{pmatrix}\lambda_1^2&&&&0\\&&\lambda_k^2&&\\&&&0&\\&0&&&0\\\end{pmatrix}$
(tips: $U^*A^*=W^*$ ，$AU=W$)

$W^*=\begin{pmatrix}w_1^*\\w_2^*\\...\\w_n^*\\\end{pmatrix}$

Let $W_{m\times n}=A_{m\times n}U_{n\times n}=(w_1,w_2,...,w_n,0,0,0,0)$
$<w_i,w_i>=\{\begin{matrix}\lambda_i^2&1\leq i\leq k\\0&k < i \leq n\\\end{matrix}.$ 

$\begin{matrix}<w_i,w_j>=0&i\neq j\\\end{matrix}.$
以下談如何找V
想法: $AU=W$
$V^*AU=V^*W=\sum$
(希望要得到)
$V=(v_1,v_2,...,v_m)$
$\begin{pmatrix}v_1^*\\v_2^*\\...\\v_m^*\\\end{pmatrix}\begin{pmatrix}w_1&w_2&...&w_n\\\end{pmatrix}=\begin{pmatrix}\lambda_1&&&0\\&\lambda_k&&\\&&0&\\0&&&0\\\end{pmatrix}$
$<\frac{w_1}{\lambda_1},w_1>=\lambda_1$
$<w_1,w_1>=\lambda_1^2$


$v_i=\frac{w_i}{\lambda_i}$，$1\leq i \leq k$
$v_i$，$k\leq i\leq m$
Extend $\{v_1,...,v_k\}$ so that $\{v_1,...,v_k,v_{k+1},...,v_m\}$ is an orthonormal basis for $F^m$
*Check*
$<v_i,w_i>\{\begin{matrix}=\lambda_i,&i=1,2,...,k\\=0&k<i\leq n\\\end{matrix}.$
$<v_j,w_j>=0$， $i\neq j$
### Thm
$A\in M_{m\times n}(F)$
$\Rightarrow \exists SVD$
$\beta=\{u_1,u_2,...,u_n\}:$ orthonormal basis for $F^n$ 
$\gamma=\{v_1,v_2,...,v_m\}:$ orthonormal basis for $F^m$
### Remark:
$k\leq min\{m,n\}$
$2\times 100$ rank最多是2

## Thm6.26(算子版本)
$AU=V\sum$
$A_{1\times 1}(u_1,u_2,...,u_n)_{1\times n}=(v_1,...,v_m)_{1\times m}\begin{pmatrix}\lambda_1&&0\\&\lambda_k&\\0&&0\\\end{pmatrix}_{m\times n}$
Block multiplication
$\Rightarrow (Au_1,Au_2,...,Au_n)=(\lambda_1v_1,\lambda_2v_2,...,\lambda_k v_k,0,0)$
$Au_i=\{\begin{matrix}\lambda_iv_i，&1\leq i\leq k\\0v_i，& k\leq i\leq n\\\end{matrix}$

## Summary
SVD:
$T:V\rightarrow W$
$A:F^n\rightarrow F^m$
$\Rightarrow \exists\beta=\{u_1,u_2,...,u_n\},\ \gamma=\{v_1,v_2,...,v_m\}$
orthonormal basis
such that
$T(u_i)=\lambda_iv_i$ or $Au_i=\lambda_iv_i$ $i=1,2,...,n$
$V^*AU=\sum$

Here:
$\lambda_i=\{\begin{matrix}\sqrt{\rho_i},&1\leq i\leq k\\0,&k<\leq n\\\end{matrix}$
$\rho_i(\leq 0)$ are eigenvalues of $T(A)$
$u_i:$ are eigenvectors of $T^*T(A^*A)$
$v_i=\frac{w_i}{\lambda_i}, i=1,2,...,k$
$(w_1,...,w_k,...,w_i)=W=AU$
$U=(u_1,u_2,...,u_n)$

### Remarks:
1. $v_j\perp v_i$，$k+1\leq j\leq m$，$1\leq i\leq k$ 
   $||v_j||=1$
2. span$\{u_{k+1},...,u_n\}=N(A)$
   $N(A)^\perp=$ span$\{u_1,...,u_k\}$
   $F^n=N(T)\oplus N(A)^\perp$
3. Range($A$)$=$ span$\{v_1,v_2,...,v_k\}$
   Range(A)$^\perp$
   $=$ span$\{v_{k+1},...,v_m\}$
## Example1
$A\in M_{2\times 2}(R):$ inventible
$S=$單位圓
$A(S)=$

---
### Sol
Rank($A$)$=2$
 ![[Pasted image 20240918150904.png]]
$A(u)=A(a_1u_1+a_2u_2)=a_1Au_1+a_2Au_2$
*(SVD)*$=a_1\lambda_1v_1+a_2\lambda_2v_2$
*($x'=a_1\lambda_1$，$y'=a_2\lambda_2$)*
![[Pasted image 20240918150909.png]]
## Pseudo inverse
$T:V\rightarrow W$
想法: 
$N(T)^\perp\oplus N(T)=V$ 
*(N(T) 不是0)*
$T:N(T)^\perp\rightarrow$ Range($T$)
$L=T_{1N(T)^\perp}$
($L$ is 1-1 and onto)

$T^\dagger:$ pseudo inverse
$T^\dagger:$ $W\rightarrow V$
$T^\dagger$ is called the pseudo inverse of $T$
$W=$ Range($T$)$\oplus$ Range($T$)$^\perp$
$T^\dagger(y)=\{\begin{matrix}L^{-1}(y),&y\in \texttt{Range}(T)\\0,&y\in \texttt{Range}(T)^\perp\\\end{matrix}$

### Remark
如此的$T^\dagger:W\rightarrow V$是唯一的
稱 peseudo inverse of $T$
1. 若$V=W$，$Ker(T)=0$，$\Rightarrow T^\dagger=T^{-1}$
2. $V=N(T)\oplus N(T)^\perp$
3. $W=\texttt{Range}(T)\oplus \texttt{Range}(T)^\perp$

### 2個問題
1. How to compute the pesudo inverse?
   (SVD)
2. Applications?

Thm6.12&6.13
LSP minimum problem
$A_{m\times n}x=b$
$z=A^{\dagger}b$

### How to compute $T^\dagger$?
$SVD:N(T),N(T)^\perp$
$Range(T),Range(T)^\perp$
是一清二楚
Recall: SVD
$\exists \beta=\{u_1,...,u_n\}$
$\gamma=\{v_1,...,v_m\}$
orthonormal basis
$T(u_i)=\lambda_iv_i$
$\lambda_i^2:T^*T$的eigenvalues
($\lambda_i:T$的singular values.)
$u_i:T^*T$相對於$\lambda_i^2$的eigenvectors
$v_i:$?
$rank(T)=k$
$\lambda_i>0,i=1,2,...,k$
$\lambda_i=0,k+1\leq i\leq n$.
(Summarize) $SVD\Leftrightarrow V^*AU=\sum$
$U=(u_1,...,u_n),V=(v_1,...,v_m)$
$\sum=\begin{pmatrix}\lambda_1&&0\\&\lambda_k&0\\0&&0\\\end{pmatrix}$
$\Rightarrow 2由\texttt{SVD},U^*T^\dagger V=\Lambda=\begin{pmatrix}\frac{1}{\lambda_1}&&\\&\frac{1}{\lambda_k}&\\0&&0\\\end{pmatrix}$
$\Rightarrow T^\dagger=U\Lambda V^*$

$\Rightarrow N(T)=$ span$\{u_{k+1},...,u_n\}$
$N(T)^\perp=$ span$\{u_1,...,u_k\}$
$\texttt{Range}(T)=\texttt{span}(v_1,...,v_k)$
$Range(T)^\perp=\texttt{span}\{v_{k+1},...,v_m\}$
$T^\dagger(v_i)=\{\begin{matrix}\frac{1}{\lambda_i}u_i,&1\leq i\leq k\\0&k+1\leq i\leq m\\\end{matrix}$

### ex. 3(c)
$A=\begin{pmatrix}1&1\\0&1\\1&0\\1&1\\\end{pmatrix}_{4\times 2}$
$A^\dagger=?$
$A^*A=\begin{pmatrix}1&0&1&1\\1&1&0&1\\\end{pmatrix}\begin{pmatrix}1&1\\0&1\\1&0\\1&1\\\end{pmatrix}$$=\begin{pmatrix}3&2\\2&3\\\end{pmatrix}$ rank$(A^*A)=2$
$\begin{vmatrix}3-\lambda&2\\2&3-\lambda\\\end{vmatrix}=\lambda^2-6\lambda+9-4=(\lambda-5)(\lambda-1)=0$
$A^*A-5I=\begin{pmatrix}-2&2\\2&-2\\\end{pmatrix}\Rightarrow u_1=\begin{pmatrix}\frac{1}{\sqrt{2}}\\\frac{1}{\sqrt{2}}\\\end{pmatrix}$
$A^*A-1I=\begin{pmatrix}2&2\\2&2\\\end{pmatrix}\Rightarrow u_2=\begin{pmatrix}\frac{1}{\sqrt{2}}\\-\frac{1}{\sqrt{2}}\\\end{pmatrix}$
$U=\begin{pmatrix}\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\\frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{2}}\\\end{pmatrix}$

### Recall
$U^*A^*A_{m\times n}U_{n\times n}=\begin{pmatrix}\lambda_1^2&&0\\&\lambda_k^2&\\0&&0\\\end{pmatrix}$
找V
$W^*W=\begin{pmatrix}\lambda_1^2&&0\\&\lambda_k^2&\\0&&0\\\end{pmatrix}$
$V^*W=V^*AU=\sum$
$W=(w_1,...,w_n)$
$<w_i,w_i>=\lambda_i^2$
$<w_j,w_i>=0$
Wanted: $<w_i,v_i>=\lambda_i$，$i=1,2,...,k$.
$v_i=\frac{w_i}{\lambda_i},i=1,2,...,k$ 

#### Summary: 如何找$v_i$
$v_i=\frac{w_i}{\lambda_i},i=1,2,...,k$
只要確保$v_{k+1},...,v_{m}$ 使得$\{v_1,...,v_m\}$ 是 orthonormal basis
$W=AU=\begin{pmatrix}1&1\\0&1\\1&0\\1&1\\\end{pmatrix}\begin{pmatrix}\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\\frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{2}}\\\end{pmatrix}$
$=\begin{pmatrix}\frac{1}{\sqrt{2}}&0\\\frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{2}}\\\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\\sqrt{2}&0\\\end{pmatrix}$$=(w_1,w_2)$
$v_1=\frac{w_1}{\sqrt{5}},v_2=\frac{w_2}{\sqrt{1}}=w_2$
singular values of $A$ $\sqrt{5},\sqrt{1}$
$V=(v_1,v_2)$
$A^\dagger= U\Lambda V^*$
## Thm 6.?? 應用
1. If $A_{m\times n}x=b$ is consistent, $z=A^\dagger b$ is the unique minimum solution 
(i.e.
if $Ay=b$, then $||z||\leq||y||$)
\[Thm6.13\]
2. If $Ax=b$ is inconsistent, then $z$ is the unique solution of the minimum error.
(i.e. $||Az-b||\leq||Ay-b||$ for any $y\in R^n$)
\[Thm6.12\]

























