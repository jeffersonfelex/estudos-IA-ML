## Sumário  

- [1.1 Introdução a matrizes](#11-introdução-a-matrizes)  

- [1.2 Tipos especiais de matrizes](#12-tipos-especiais-de-matrizes)  

  

---  

  

## 1.1 Introdução a matrizes  

  

Chamamos de matriz uma tabela de elementos estruturados em linhas com colunas. **Abstrair** significa considerar algo de forma isolada, separando-o de outros detalhes.  

  

Por exemplo, ao recolhermos os dados referentes a altura, peso e idade de um grupo de quatro pessoas, podemos dispô-los em uma tabela:  

  

| | Altura (m) | Peso (Kg) | Idade (Anos) |  

| :------------ | :--------: | :-------: | :----------: |  

| **Pessoa 1** | 1,70 | 70 | 23 |  

| **Pessoa 2** | 1,75 | 60 | 45 |  

| **Pessoa 3** | 1,60 | 52 | 25 |  

| **Pessoa 4** | 1,81 | 72 | 30 |  

  

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

  

* 1.2.2 Matriz Nula é aquela em que