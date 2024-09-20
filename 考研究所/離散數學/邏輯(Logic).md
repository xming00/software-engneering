# 定義 : 
**Proposition(命題)**
> A proposition is a declaration that is  either true or false, but not both.

**Truth Value**
> The truth value of a true (of false, respectively) proposition is True ( or False, respectively) and denoted by $T$ (or $F$, respectively).
## 例子
Which of the following statements are propositions? What are the truth value(真值) of those propositions?
a. Taipei is the capital of Taiwan 
T
b. 2+3=5
T
c. 5+7=10
F
d. x+2=11
(X)
e. Good morning!
(X)
f. Where are you going?
(X)
g. Give me money.
(X)

# 
Propositional Variables are variables that represent propositions. e.g. $p,q,r,s,...$.

The area of logic that deals with propositions is  called propositional Calcullus.

# Compound Propositions
> propositions that are formed from existing propositions using **Logical Operators**.

## 定義
### Negation Operator ($\bar a$) 
 >Let $p$ be a proposition. $\bar p$，the negation of $p$，is the statement "It is not the case of p."
 >$\bar p$ is read "not p"
 >The truth value of $\bar p$ is the opposite of the truth value of p.
#### 例子
$p=$ "Today is Friday"
$\bar p=$ "It is not the case of today is Friday."
$=$ "Today is not Friday."
#### Truth Table(真值表)

| $p$ | $\bar p$ |
| --- | -------- |
| T   | F        |
| F   | T        |

### Conjunction Operator ($\wedge$, AND)
> Let $p$ and $q$ be propositions.
> $p\wedge q$，the conjuction of $p$ and $q$ ，is the proposition "p and q."
> $p\wedge q$ is true when both p and q are true., and false otherwise.

#### Truth Table

| $p$ | $q$ | $p\wedge q$ |
| --- | --- | ----------- |
| T   | T   | T           |
| T   | F   | F           |
| F   | T   | F           |
| F   | F   | F           |
### Disjunction Operators ($\vee$，OR)
> Let $p$ and $q$ are propositions. $p\vee q$, the disjunction of $p$ and $q$, is the proposition "$p$ or $q$"
> $p\vee q$ is false when both p and q are false and true otherwise.

#### Truth Table

| $p$ | $q$ | $p\vee q$ |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | T         |
| F   | T   | T         |
| F   | F   | F         |
### 例子
$p=$ "Today is Friday"
$q=$ "It is raining."
$r=$ "There is a dog in the classroom"
$p\wedge q=$ "Today is Friday and it is rainning."
$p\vee q=$ "Today is Friday or it is rainning"
$p\wedge q\wedge r=$ "Today is Friday and it is raining and there is a dog in the classroom"
$p\vee q\vee r=$ "Today is Friday or it is raining or there is a dog in the classroom"
### Remark
$\wedge$: 像乘法(在二元的世界)
$\vee$: 像加法(在二元的世界)

### Exclusive OR ($\oplus$ 互斥或)
#### Truth Table

| $p$ | $q$ | $p\oplus q$ |
| --- | --- | ----------- |
| T   | T   | F           |
| T   | F   | T           |
| F   | T   | T           |
| F   | F   | F           |

### Conditional Operator ($\rightarrow$)
$p\rightarrow q$ conditional statement
(若p則q)
(無因果關係)
(只是對錯的組合關係)
#### 例子
If you attend the class every time, you get 100 in the course.

| $p$ | $q$ | $p\rightarrow q$ |
| --- | --- | ---------------- |
| T   | T   | T                |
| T   | F   | F                |
| F   | T   | T                |
| F   | F   | T                |
#### 例子2
If $2+3=4$，then $x=x+1$
If $2+3=5$，then $x=x+1$
sol: 
$p=$"$2+3=4.$"
$q=$"$2+3=5.$"
$r=$"$x=x+1.$"

$p\rightarrow r$
$q\rightarrow r$

#### 真值表

| $p$ | $q$ | $\bar p$ | $\bar q$ | $p\rightarrow q$ | $q\rightarrow p$ | $p\rightarrow \bar q$ | $\bar q\rightarrow\bar p$ |
| --- | --- | -------- | -------- | ---------------- | ---------------- | --------------------- | ------------------------- |
| T   | T   | F        | F        | T                | T                | F                     | T                         |
| T   | F   | F        | T        | F                | T                | T                     | F                         |
| F   | T   | T        | F        | T                | F                | T                     | T                         |
| F   | F   | T        | T        | T                | T                | T                     | T                         |
$p\rightarrow q\equiv \bar q\rightarrow\bar p$

### Biconditional Operator($\leftrightarrow$)
$p\leftrightarrow q\equiv (p\rightarrow q)\wedge (q\rightarrow p)$

| $p$ | $q$ | $p\rightarrow q$ | $q\rightarrow p$ | $(p\rightarrow q)\wedge(q\rightarrow p)$ |
| --- | --- | ---------------- | ---------------- | ---------------------------------------- |
| T   | T   | T                | T                | T                                        |
| T   | F   | F                | T                | F                                        |
| F   | T   | T                | F                | F                                        |
| F   | F   | T                | T                | T                                        |

## 優先權
$\wedge,\vee,\bar a, \rightarrow, \leftarrow$

| operator          | priority |
| ----------------- | -------- |
| $\bar a$          | 1        |
| $\wedge$          | 2        |
| $\vee$            | 3        |
| $\rightarrow$     | 4        |
| $\leftrightarrow$ | 5        |
### 例子
$p\vee q\rightarrow p\wedge q$

| p   | q   | r   | $p\vee q$ | $p\wedge r$ | $p\vee q\rightarrow p\wedge q$ |
| --- | --- | --- | --------- | ----------- | ------------------------------ |
| T   | T   | T   | T         | T           | T                              |
| T   | T   | F   | T         | F           | F                              |
| T   | F   | T   | T         | T           | T                              |
| T   | F   | F   | T         | F           | F                              |
| F   | T   | T   | T         | F           | F                              |
| F   | T   | F   | T         | F           | F                              |
| F   | F   | T   | F         | F           | T                              |
| F   | F   | F   | F         | F           | T                              |

### 問題
Q1. What is the number of rows in the truth table for a compound proposition with n different variables?
Q2: How many possible truth tables are for compound proposition with n different variables.

Ex: How can this sentence be translated into a logical express?
1.
"You can access the Interent from campus only if you are a computer science major or you are not a freshman."
$p=$ "You can access the Internet from the campus"
$q=$ "You are a computer science majoor"
$s=$ "You are a freshman."
"p only if q."$\equiv$"if p, then q"
$p \rightarrow q\vee \bar r$
2.
"You cannot ride the roller coaster if you are under 4 feet tall unless you are older than 16 years old."
$q=$ "you can ride..."
$r=$ "you are under 4 feet."
$s=$ "you are older than 16..."
$r\wedge \bar s\rightarrow \bar q$

### Logic puzzles
There are two kinds of inhabitants in an island, knights and knaves. Knights always tell the true, and knaves always lie.
A: "B is a knight."
B: "Both of them are opposite types."
sol: 1. Assume A is a kight. $\Rightarrow$ B is a knight. ($\rightarrow\leftarrow$)
2. Assume A is a knave.$\Rightarrow$ B is knave.
## Bit Operations
String: a sequence of 0 or 1.
The length of a bit string.
the # of 0 or 1 in the string.

01010111
11000011
### Bitwise OR:  11010111
### Bitwise AND: 01000011
### Bitwise XOR: 10010100

# Propositional Equivalences(公式推演)
## 定義
> A compound proposition is always true (or false, resp.) is called a tautology(or contradiction, resp.)

> A compound proposition is neither a tautology nor a contradiction is called a contingency.

## 例子
Let $p$ be a proposition.
$p\wedge \bar p$，$p\vee\bar p$

| $p$ | $\bar p$ | $p\wedge \bar p$ | $p\vee\bar p$<br> |
| --- | -------- | ---------------- | ----------------- |
| T   | F        | F                | T                 |
| F   | T        | F                | T                 |

## 定義
> Two compound propositions $p$ and $q$ are called. logical equivalent. if $p\leftrightarrow q$ is a tautology, and is denoted as $p\equiv q$.

## 例子
$p\rightarrow q$，$\bar q\rightarrow \bar p$

| $p$ | $q$ | $\bar p$ | $\bar q$ | $p\rightarrow q$ | $\bar q\rightarrow\bar p$ |
| --- | --- | -------- | -------- | ---------------- | ------------------------- |
| T   | T   | F        | F        | T                | T                         |
| T   | F   | F        | T        | F                | F                         |
| F   | T   | T        | F        | T                | T                         |
| F   | F   | T        | T        | T                | T                         |

## De Morgan Laws
$\overline{A\bigcup B}=\bar A\bigcap \bar B$
1. $\overline{(p\vee q)}\equiv \bar p \wedge \bar q$
2. $\overline{(p\wedge)q}\equiv\bar p \vee \bar q$
#### Proof

| $p$ | $q$ | $\bar p$ | $\bar q$ | $p \vee q$ | $\overline{(p\vee q)}$ | $\bar p \wedge \bar q$ | $\overline{(p\vee q)}\leftrightarrow\bar p \wedge \bar q$ |
| --- | --- | -------- | -------- | ---------- | ---------------------- | ---------------------- | --------------------------------------------------------- |
| T   | T   | F        | F        | T          | F                      | F                      | T                                                         |
| T   | F   | F        | T        | T          | F                      | F                      | T                                                         |
| F   | T   | T        | F        | T          | F                      | F                      | T                                                         |
| F   | F   | T        | T        | F          | T                      | T                      | T                                                         |

## 結合律
$(p\wedge q)\wedge r\equiv p\wedge(q\wedge r)$

| p   | q   | r   |     |
| --- | --- | --- | --- |
| T   | T   | T   |     |
| T   | T   | F   |     |
| T   | F   | T   |     |
| T   | F   | F   |     |
| F   | T   | T   |     |
| F   | T   | F   |     |
| F   | F   | T   |     |
| F   | F   | F   |     |
## 交換律
$p\wedge q\equiv q\wedge p$
$(p\vee q)\vee r \equiv p\vee(q\vee r)$
$\equiv p\vee q\vee r$
$p\vee q\equiv q\vee p$

## Identity laws
$p\wedge T\equiv p$
$p\vee F\equiv p$
## Domination laws
$p\vee T\equiv T$
$p\wedge F\equiv F$
## Idempotent laws
$p\wedge p\equiv p$
$p\vee p\equiv p$
## Double negation
$\bar{\bar{p}}\equiv p$
## Commtative laws 
$p\vee q\equiv q \vee p$
$p\wedge q \equiv q\wedge p$
## Associative law
$(p\vee q)\vee r \equiv p\vee(q\vee r)$
$(p\wedge q)\wedge r\equiv p\wedge (q\wedge r)$

## Distributive laws
$p\wedge (p\vee r)\equiv (p\wedge q)\vee (p\wedge r)$
$p\vee(q\wedge r)\equiv (p\vee q)\wedge(p\vee r)$

## De Morgan laws
1. $\overline{(p\vee q)}\equiv \bar p \wedge \bar q$
2. $\overline{(p\wedge)q}\equiv\bar p \vee \bar q$

## Absorption laws
$p\vee (p\wedge q)\equiv p$
$p\wedge(p\vee q)\equiv p$
## Nogation
$p\vee \bar p\equiv T$
$p\wedge \bar p\equiv F$

## 延伸
$p_1\wedge p_2...\wedge p_n\equiv \wedge^n_{i=1}p_i$
$p_1\vee p_2...\vee p_n\equiv \vee^n_{i=1}p_i$
$\overline{(\wedge^n_{i=1})p_i}\equiv \vee^n_{i=1}\overline{p_i}$
$\overline{(\vee^n_{i=1})p_i}\equiv \wedge^n_{i=1}\overline{p_i}$ 

## Conditional Statement
$p\rightarrow q\equiv \bar{q}\rightarrow \bar{p}$
$p\rightarrow q\equiv\bar{p}\vee q$
$(p\rightarrow q)\wedge(p\rightarrow r)\equiv p\rightarrow(q\wedge r)$
$(p\rightarrow r)\wedge(q\rightarrow r)\equiv(p\vee q)\rightarrow r$

## Bi-conditional Statements
$p\leftrightarrow q\equiv (p\rightarrow q)\wedge(q\rightarrow p)$
$p\leftrightarrow q\equiv (p\wedge q)\vee(\bar{p}\wedge \bar{q})$
$p\leftrightarrow q\equiv\bar{p}\leftrightarrow \bar{q}$

# 代數運算
$\overline{(p\rightarrow q)}\equiv p\wedge \bar{q}$
## 證明方法
1. Truth Table(Low)
2. 用公式


## 例子
$\overline{p\vee(\bar{p}\wedge q))}$
![[Pasted image 20240910163332.png]]

## 例子2
Show that $(p\wedge q)\rightarrow (p\vee q)$ is a tautology.
 ![[Pasted image 20240910163337.png]]

# Predicate Logic 述詞邏輯
把命題用變數的概念來取代
單純看函數時不代表命題

## Universal Quantifier
是否全部是
$\equiv P(x_1)\wedge P(x_2)\wedge...\wedge P(x_n)$
(亦然)

## Existential Quantifier
有沒有
$\equiv P(x_1)\vee P(x_2)\vee...\vee P(x_n)$


$\equiv \overline{(P(x_1)\vee P(x_2)\vee...\vee P(x_n))}$
$\equiv \overline{P(x_1)}\wedge\overline{P(x_2)}\wedge...\wedge\overline{P(x_n)}$
$\equiv \forall x(\overline{P(x)})$


### 交換律
#### 兩個Quantifier 應用
### 結合律
### 分配律

### 優先權



# 證明

前提都要對，結論才對
三段論證法
$(p\rightarrow q)\wedge(q\rightarrow r)\rightarrow (p\rightarrow r)$
...(自己證)








































