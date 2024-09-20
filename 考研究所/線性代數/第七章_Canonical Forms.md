
矩陣最簡潔的樣子
1. 對角線化
1. $\exists \beta=\{\texttt{eigenvectors}\}$
2. $CP$ of splits $gm(\lambda)=am(\lambda)$
3. $\texttt{Normal.}\ F=C$
4. $self-adjoint\ F=R$

# Jardon Canonical Form
不可對角線化的最簡樣子
## Ex
$A=\begin{pmatrix}1&1\\0&1\\\end{pmatrix}$
$CP=(\lambda-1)^2$
$am(\lambda=1)=2$
$A-1I=\begin{pmatrix}0&1\\0&0\\\end{pmatrix}$
$\texttt{rank}(A-I)=1$
$N(A-I)=1$
$\texttt{gm}(\lambda=1)=1$
## Ex2
$A=\begin{pmatrix}2&1&&0\\&&\\0&&&1\\&&&2\\\end{pmatrix}_{100\times 100}$
$CP=(\lambda-2)^{100}$
$A-2I=\begin{pmatrix}0&1&&0\\&&&1\\0&&&0\\\end{pmatrix}_{10^4\times10^4}$
$\texttt{rank}(A-2I)=99$
$\texttt{Nullity}(A-2I)=1=\texttt{gm}(\lambda=2)$
## 定義
$A_i=\begin{pmatrix}\lambda_i&1&&0\\&&&\\&&&1\\0&&&\lambda_i\\\end{pmatrix}$

A is called Jordan block
2. The matrix $A$ of the form
![[Pasted image 20240919105612.png]]
is called a Jordan Canonical Form, where $A_i$ are Jordan blocks
結論: 若$CP$ of A 可一次分解，則$\exists\beta$ a basis such that $[L_A]_\beta=$ a Jordan $CF$
2. 或$\beta=\{v_1,v_2,...,v_n\}$ such that $Q^{-1}AQ=$ a Jordan $CF$, where $Q=(v_1,v_2,...,v_n)$

## Ex
$T:$$\exists\beta=\{v_1,v_2,...,v_8\}$
$[T]_\beta=$
![[Pasted image 20240919163945.png]]
$A_1,A_2,A_3,A_4$ are Jordan Block.
$CP$ of $T=(\lambda-2)^4(\lambda-3)^2\lambda^2$
問:
1. 那些$v_i$是eigenvectors?
2. 不是eigenvectors 的$v_i$又有哪些性質?
$Tv_1=2v_1$
$\Leftrightarrow$
$(T-2I)v_1=0$
$T(v_2)=v_1+2v_2$
$\Rightarrow (T-2I)v_2=v_1$
$\Rightarrow (T-2I)^2v_2=0$
$T(v_3)=v_2+2v_3$
$\Rightarrow(T-2I)v_3=v_2$
$\Rightarrow(T-2I)^3v_3=0$
$(T-2I)v_4=0$

## Main Results
$T:$$CP$ of T $splits$
$\Rightarrow\exists\beta=\{\texttt{generalized eigenvectors}\}$ an ordered basis such that.
$[T]_\beta=$ a Jordan Canonical Form

問題
1. Why?
2. How?

## 定義
1. $v\neq0$ is a generalized eigenvector of $T$ if $\exists\lambda\in F$, and a $P\in N$ such that $(T-\lambda I)^P(v)=0$
2. Let $K_\lambda=\{v\in V:\exists m \in N$ such that $(T-\lambda I)^m(v)=0\}$. Then $K_\lambda$ is called the generalized eigenspace of $T$ coresponding to $\lambda$
$(T-\lambda I)(v)=0\Leftrightarrow T(v)=\lambda v$

## Ramarks
1. $\lambda$ is an eigenvalue of $T$ (since for $k$ being the smallest positive integer such that $(T-\lambda I)^k(v)=0,$ then $(T-\lambda I)^{k-1}(v)$ is an eigenvalue of $\lambda$
2. If $p=1$, then $v$ is an eigenvectors of $T$.

已知
$(T-\lambda I)^k(v)=0$
$(T-\lambda I)((T-\lambda I)^{k-1})(v)=0$
$(T-\lambda I)(u)=0$ $\Leftrightarrow T(u)=\lambda u$

## 目的
1. $\texttt{dim}(K_\lambda)=\texttt{am}(\lambda)$ *(Thm7.1-Thm7.4)*
2. $\beta=\{\texttt{generalized eigenvectors}\}$

## 例子
![[Pasted image 20240919175130.png]]
![[Pasted image 20240919175138.png]]
## 定義
>1. Let $v$ be a generalized eigenvector with coresponding eigenvalue $\lambda$. Let $p$ be the smallest positive integer such that $(T-\lambda I)^p(v)=0$. Then $\{(T-\lambda I)^{p-1}(v),(T-\lambda I)^{p-2}...,(T-\lambda I)(v),v\}$ is called a cycle of a generalized eigenvectors coresponding to $\lambda$. We say that the length of the cycle is $p$
>2. $(T-\lambda I)^{p-1}(v)$ and $v$ are called the initial vector and end vector of the cycle respectively.

## Recall:
* generalized eigenvectors generialized eigenspaces
* a cycle of generalized $k_\lambda$ eigenvectors
* $\beta=\{$ cycles of generalized ev's$\}$ 
![[Pasted image 20240920143615.png]]

## Fact:
1. $\gamma$ is linearly independant
2. Let $\gamma_i$ be "disjoint" cycles. Then $\bigcup r_i$ is linearly independant.
   (此處"disjoint"是指將不同的cycles 之initial vectors 收集所成的集合是linear independant)又此處$r_i$所對應的eigenvalue皆為$\lambda$
3. Let $\beta=\{\texttt{disjoint cycles of generalize eigenvectors } \texttt{with responding to }\lambda$
   Then $\beta$ is a basis for $K_\lambda$  (why?)
4. Let $\lambda_{i_1}\ i=1,2,...,k$，be distinct eigenvalues of $T$. Then we can do $1.$~$3.$ for each $K_{\lambda_i}$
5. $V=K_{\lambda_1}\oplus K_{\lambda_2}\oplus ...\oplus K_{\lambda_k}$
   $\beta=\bigcup^k_{i=1}\beta_i$ is a Jordan canonical basis for $V$.
 

#### 證明 1
$\sum^{p-1}_{i=0}a_i(T-\lambda I)^i(x)=0$
Wanted: $a_i=0$ , for all $i=0,1,...,p-1$
$a_{p-1}(T-\lambda I)^{p-1}(x)+...+a_1(T-\lambda I)^1(x)+a_0x=0$
*(兩邊作用$(T-\lambda I)^{p-1}$)*$\Rightarrow a_0(T-\lambda I)^{p-1}(x)=0$$\Rightarrow a_0=0$
 同理，$a_i=0$ for all $0\leq i \leq p-1$

#### 證明2
基本同證明1

## Summary
Let $A\in M_{n\times n}(C)$. Then $\exists\beta=$ a Jordan Canonical basis $=\bigcup\beta_i=\{$ cycles of generalized eigenvector$\}$
such that $[L_A]_\beta=Q^{-1}AQ=$ a Jordan Canonical form
$Q=(\beta)=$ 由$\beta$排出來的矩陣。

![[Pasted image 20240920153756.png]]

how: 如何找$Q$ , $\beta$  such that $A\rightarrow J$
 





























































