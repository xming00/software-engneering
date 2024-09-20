# Tree定義
是由$\geq1$個節點(nodes)所形成之集合，不可以為空，滿足:
1. 至少有1個特殊節點，稱為Root
2. 其餘Nodes分成: $T_1,T_2,...,T_m$之互斥(disjoint)集合，而$T_1$~$T_m$ 稱為Root的子樹(subtrees)
## 相關術語
1. Node's Degree (分支度)
2. Leaf(樹葉)
3. Non-Leaf
4. Child and Parent
5. sibling
6. Ancestors
7. Node's level 值
8. Tree's Degree (degree of a tree)=Max{Node's degree}
9. Tree's Height (or Depth) = Max{Node's level}
10. Forest 
    Def: 是由$\geq0$棵互斥tree所形成的集合
    Note: Forest 可以為空 (Binary tree 也可以為空)

# Tree的4種表示方式
## 利用 Link list 直接表示
![[Pasted image 20240908223533.png]]
## 分析
最大缺點在於極度浪費link space
說明: 假設 n 個Nodes, Tree's Degree =k，則總共link總數$=n\times k$條，其中有用的(link$\neq$Null )有N-1條
浪費的(Null links)數目有$nk-(n-1)$條
$\Rightarrow$浪費比例=$\frac{nk-(n-1)}{nk}=\frac{n(k-1)+1}{nk}=\frac{n(k-1)}{nk}=\frac{k-1}{k}$(k=2會最少)
## Tree 化成Binary Tree 之後再表示 

## "child-sibling"方法 (左兒子，右兄弟)
![[Pasted image 20240908225131.png]]

## 括號法
作法: 以父($子_1,子_2,...,子_n$)括號方式表達父點與子點間的組成關係，且可以Nested
![[Pasted image 20240908225409.png]]
\<Ans\> A(B(EF)C(GHI)D(J))
例子:
A(B(CD(E))F(GH)I(JK(L))M) 轉成樹(Tree)
![[Pasted image 20240908231948.png]]


# Binary Tree定義，與Tree比較
## Def
可以為空，若不為空，則滿足:
1. 有root及左右子樹
2. 左右子樹也是Binary Tree
## 與Tree比較
| Tree                    | Binary Tree                  |
| ----------------------- | ---------------------------- |
| 不可以為空                   | 可以為空                         |
| Node's degree$\geq$ 0即可 | 0$\leq$Node's degree$\leq$ 2 |
| 子樹之間無次序/方向之分            | 子樹有左右之分                      |
## Binary tree 之3個基本定理(令Root level=1)
### 定理一
二元樹中第i level 之最多node數=$2^i-1$個 (i$\geq$ 1)
#### 


# Binary Tree 4種類


# Binary Tree 2種表示方式


# B.T. 的Traversal及應用(前中後序及level-ordered)


# Binary search tree


# Heap


# Thread Binary Tree



# Tree轉B.T.，Forest轉B.T.


# n個node可形成之B同B.T.個數


# Disjoint sets定義，表示，Union，Find運作探討

