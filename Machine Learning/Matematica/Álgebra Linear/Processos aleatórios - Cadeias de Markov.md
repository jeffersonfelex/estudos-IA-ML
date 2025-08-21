# 1.5.0

Muitos processos da natureza e da sociedade podem ser estudados como **processos estocásticos**, ou seja, fenômenos em que a transição de um estado para outro ocorre segundo uma certa probabilidade.

## Definição
- Um **processo de Markov** é uma sequência de estados em que a probabilidade de transição depende **apenas do estado atual**, e não do histórico completo.
- Essa sequência de estados, regida por probabilidades, é chamada de ==**cadeia de Markov==

- ## Características
- A transição entre estados é representada por uma **matriz das probabilidades de transição**.
- O elemento `t_ij` dessa matriz indica a probabilidade de transição do estado `i` para o estado `j`.
- Também se utiliza o conceito de **vetor de probabilidades**, que descreve a distribuição de probabilidades entre os estados em um dado instante.

## Exemplo
- Estados possíveis: **chuva (C)** e **seca (S)**.
- Supondo que:
  - Se chover bastante em um ano, a chance de seca no próximo é `3/4`.
  - Se houver seca em um ano, a chance de seca no próximo é `1/2`.
- Isso gera uma **árvore de probabilidades**, onde é possível calcular a chance de cada cenário após alguns anos.
## Importância
- Cadeias de Markov permitem previsões de comportamento a longo prazo.
- Apesar de simplificar fenômenos reais, são ferramentas úteis para modelagem de processos estocásticos.
---
# 1.5.1 Definição:

O processo de formação de um processo aleatório de Markov deve assumir estados $a_1,a_2,...,a_r$, de tal modo que a probabilidade de transição de um estado $a_j$ para um estado $a_i$ seja $p_ij$ (um número que depende apenas daquele índice, ou seja, $a_j$ e $a_i$).

A matriz das probabilidades de transição (matriz estocástica) é dada por:
$$  

T =  

\begin{bmatrix}  

a_{11} & a_{12} & \dots & a_{1n} \\  

a_{21} & a_{22} & \dots & a_{2n} \\  

\vdots & \vdots & & \vdots \\  

a_{m1} & a_{m2} & \dots & a_{mn}  

\end{bmatrix}
$$
# Definição: Matriz de Transição de Markov

Seja **P** uma matriz quadrada cujas entradas $P_ij$ são definidas para todos os estados $i$ e $j$.  

Dizemos que **P** é uma **matriz Markoviana** (ou **matriz de probabilidade de transição**) se:

1. Para todo $i ∈ S$, temos $P_ij ≥ 0$, onde $S$ é o conjunto de estados.  
2. A soma das probabilidades de transição a partir de um estado é igual a 1:  

   $\sum_{j \in S} P_{ij} = 1, \quad \forall i \in S$
## Observação
Um **processo Markoviano** é totalmente definido por:
- Sua **matriz de probabilidades de transição** $P$.
- A **distribuição de probabilidade inicial** do estado $X0$.

[Cadeia de Markov - Conceitos Fundamentais](https://www.youtube.com/watch?v=k6FAZJGTZJo)

---
# 1.5.2 Previsões a Longo Prazo:

Para podermos fazer previsões a longo prazo, com padrões da matriz $T$ deve cumprir algumas condições