## Sumário  

- [1.1 Introdução a matrizes](#11-introdução-a-matrizes)  
- [1.2 Tipos especiais de matrizes](#12-tipos-especiais-de-matrizes)
- [1.3 Operações com matrizes](#1.3-Operações-com-matrizes)

  

---  

  

## 1.1 Introdução a matrizes  

  

Chamamos de matriz uma tabela de elementos estruturados em linhas com colunas. **Abstrair** significa considerar algo de forma isolada, separando-o de outros detalhes.  

  

Por exemplo, ao recolhermos os dados referentes a altura, peso e idade de um grupo de quatro pessoas, podemos dispô-los em uma tabela:  


| Pessoa       | Altura (m) | Peso (kg) | Idade (anos) |
|:------------:|:----------:|:---------:|:------------:|
| **Pessoa 1** |    1,70    |    70     |      23      |
| **Pessoa 2** |    1,75    |    60     |      45      |
| **Pessoa 3** |    1,60    |    52     |      25      |
| **Pessoa 4** |    1,81    |    72     |      30      |

  

Se abstrairmos os significados das linhas e colunas, temos uma matriz $A_{4 \times 3}$:  

  

$$  

A =  

\begin{bmatrix}  

1,70 & 70 & 23 \\  

1,75 & 60 & 45 \\  

1,60 & 52 & 25 \\  

1,81 & 72 & 30  

\end{bmatrix}  

$$  

  

Os elementos de uma matriz podem ser números (reais ou complexos), funções, ou ainda outras matrizes.  

  

Assim, podemos representar uma matriz genérica com **m** linhas e **n** colunas por:  

  

$$  

A_{m \times n} =  

\begin{bmatrix}  

a_{11} & a_{12} & \dots & a_{1n} \\  

a_{21} & a_{22} & \dots & a_{2n} \\  

\vdots & \vdots & \vdots & \vdots \\  

a_{m1} & a_{m2} & \dots & a_{mn}  

\end{bmatrix}  

= [a_{ij}]_{m \times n}  

$$  

  

Usaremos sempre letras maiúsculas para denotar matrizes, e quando queremos especificar a ordem de uma matriz A (o número de linhas e colunas), escreveremos $A_{m \times n}$.  

  

### Como localizar um elemento em uma matriz?  

  

Para localizarmos um elemento de uma matriz, dizemos a **linha** e a **coluna** (nesta ordem) em que ele está. Por exemplo, na matriz $B_{2 \times 3}$:  

  

$$  

B =  

\begin{bmatrix}  

1 & 0 & -4 \\  

-3 & 2 & 2  

\end{bmatrix}  

$$  

  

O elemento que está na primeira linha e terceira coluna (elemento $b_{13}$) é **-4**.  

  ---

## 1.2 Tipos especiais de matrizes  

Ao trabalharmos com matrizes, observamos que algumas possuem padrões específicos. Seja pela sua dimensão (quantidade de linhas e colunas) ou pela natureza de seus elementos, essas matrizes apresentam propriedades que as diferenciam das demais.  

Por serem utilizadas com frequência na prática, elas recebem nomes especiais, como:  

  

- **1.2.1 Matriz Quadrada** é aquela cujo número de linhas é igual ao número de colunas (m = n). Exemplo:  

$$  

\begin{bmatrix}  

1 & 0 & 4 \\  

3 & 2 & 2 \\  

4 &5 & 6  

\end{bmatrix}  

$$  

> No caso de matrizes quadradas $A_{m \times n}$ dizemos que **A** é uma matriz de ordem *m*  

  

* 1.2.2 **Matriz Nula** é aquela em que em que $a_ i j$ = 0, para todo *i* e *j.* 
	Exemplo: Pag 7

* 1.2.3 **Matriz Coluna** é aquela que possui uma única coluna (n = 1).
	Exemplo:
$$  
\begin{bmatrix}  

1 \\  

3 \\  

4 

\end{bmatrix}  
$$
* 1.2.4 **Matriz Linha** é aquela onde m = 1.
	Exemplo:
	$$  

\begin{bmatrix}  
1 & 0 & 4 
\end{bmatrix}  

$$
---
# 1.3 Operações com matrizes

Ao utilizar matrizes, surge naturalmente a necessidade de efetuarmos certas operações. Como:

* 1.3.1 **Adição**: A soma de duas matrizes de mesma ordem, $A_{m \times n}$ =  $\begin{bmatrix} a_ i j\end{bmatrix}$ e $B_{m \times n}$ = $\begin{bmatrix} a_ i j\end{bmatrix}$, é uma matriz $m\times n$, que denotaremos **A + B**, cujo elementos são somas dos elementos correspondentes de **A** e **B**, cujos elementos são somas dos elementos correspondentes de **A** e **B**. Isto é, 
		  $$A + B = \begin{bmatrix} a_ i j + b_ i j\end{bmatrix} {m\times n} $$
		Exemplo:
			$$
A + B =
\begin{bmatrix} 
1+6 & 2+5 & 3+4 \\ 
4+3 & 5+2 & 6+1 
\end{bmatrix}
=
\begin{bmatrix} 
7 & 7 & 7 \\ 
7 & 7 & 7 
\end{bmatrix}
 
			$$

> Propriedades:  Dadas as matrizes **A, B** e **C** de mesma ordem $m \times n$ temos:
> i) A+ B = B + A (comuntativa)
> ii) A+(B + C) = (A + B) + C (associatividade)
> iii) A + 0 = A, onde 0 denota a matriz nula ${m \times n}$ 

* ## 1.3.2 Multiplicação por Escalar  
Seja $(A = [a_{ij}]_{m \times n}) e (k)$ um número, então definimos uma nova matriz:  $k \cdot A = [k a_{ij}]_{m \times n}$
	Exemplo
$$
-2 \begin{bmatrix} 
2 & 10 \\ 
1 & -3 
\end{bmatrix}
=
\begin{bmatrix} 
-4 & -20 \\ 
-2 & 6 
\end{bmatrix}
$$

### Propriedades  

Dadas matrizes (A) e (B) de mesma ordem (m $\times$ n) e números \(k, k_1, k_2\), temos:  

1. \(k(A + B) = kA + kB\)  
2. \((k_1 + k_2)A = k_1 A + k_2 A\)  
3. \(0 $\cdot$ A = 0\), isto é, se multiplicarmos o número zero por qualquer matriz \(A\), teremos a matriz nula.  
4. \(k_1 (k_2 A) = (k_1 k_2) A\)  

---


## Produtos de matrizes
# Produtos com Matrizes e Vetores

---

### 1. Produto por Escalar  
Multiplicamos **toda a matriz** por um número real \(k\).  
Cada elemento $(a_{ij})$ vira $(k \cdot a_{ij})$.  

**Exemplo:**  

$$
2 \cdot 
\begin{bmatrix} 
1 & -3 \\ 
0 & 4 
\end{bmatrix} 
= 
\begin{bmatrix} 
2 & -6 \\ 
0 & 8 
\end{bmatrix}
$$

---

###  2. Produto de Matrizes  
É a multiplicação de duas matrizes.  
- Só existe se o número de **colunas da primeira** = número de **linhas da segunda**.  
- O elemento $(c_{ij})$ é obtido multiplicando a **linha $(i)$** da primeira pela **coluna $(j)$** da segunda e somando.  

**Exemplo:**  

$$
\begin{bmatrix} 
1 & 2 \\ 
3 & 4 
\end{bmatrix}
\cdot
\begin{bmatrix} 
2 & 0 \\ 
1 & 2 
\end{bmatrix}
=
\begin{bmatrix} 
4 & 4 \\ 
10 & 8 
\end{bmatrix}
$$

---

### 3. Produto Escalar (Interno)  
Aplicado em **vetores**.  
- Multiplicamos elementos correspondentes e somamos.  

**Exemplo:**  

$$
(2,3,4) \cdot (1,0,5) = 2\cdot1 + 3\cdot0 + 4\cdot5 = 22
$$

---

## # 4. Produto Vetorial  
Aplicado em **vetores 3D** $((\mathbb{R}^3)).$  
- O resultado é **outro vetor perpendicular** aos dois originais.  

**Exemplo:**  

$$
(1,0,0) \times (0,1,0) = (0,0,1)
$$

