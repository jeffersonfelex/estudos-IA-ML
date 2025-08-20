Um dos processos mais famosos de mineração de dados (Processo padrão do mercado para mineração de dados), contém vários passos que podem ser seguidos para uma melhoria:

1. Entendimento do negócio ( Bussiness understanding)
2. Entendimento dos dados (Data understanding)
3. Preparação dos dados (Data preparation)
4. Modelagem (Modeling)
5. Avaliação (Evaluation)
6. Implantação (Deployment)

![[Pasted image 20250819165200.png]]

---
## Faça uma pergunta a si

Com base nos dados e nos problemas apresentados, reflita sobre qual modelo de mineração de dados seria mais adequado. Pergunte a si mesmo, por exemplo:  

- Quais modelos podem ser aplicados a esses dados?  
- Qual modelo é mais eficiente para o tipo de problema que quero resolver?  
- Existem variáveis que precisam de transformação antes de aplicar o modelo?  
- Como posso avaliar a performance do modelo escolhido?  

Este exercício ajuda a tomar decisões mais embasadas e a planejar melhor o processo de análise de dados.

> Termos para os dados:
> Para uma aprendizagem supervisionada, nossa intenção é ter uma função que transforme atributos em um rótulo. Se fôssemos escrever isso como uma fórmula de álgebra, teríamos algo como : 
> $y = f(x)$
> X sendo uma matriz ($A_{m \times n}$). Cada linha ($m$) representa _amostra_ dos dados ou das informações acerca de um indivíduo. Cada coluna ($n$) é um _atributo_(feature). A saída de nossa função, y, é um vetor que contém rótulos(em classificações) ou valores(em regressão)

## Colete os dados

Na maioria dos casos, utilize o **Pandas** para coletar os dados, que geralmente já estão tabelados (uma recomendação minha), o que facilita bastante. Além disso, com o Pandas você consegue trabalhar com qualquer tipo de arquivo que armazene dados.

## Limpe os dados

Devemos garantir que os dados em nossa posse estejam em um formato que podemos utilizar ele em modelos. Grande parte dos modelos fazem parte da biblioteca **scikit-learn** e exige que os atributos sejam numéricos. E muitos desses modelos falham se ter valores ausentes ($NaN$).

Alguns modelos terão melhor desempenho se os dados estiverem padronizados (têm um valor de média igual a 0 e um desvio-padrão igual a 1).

Uma limpeza nos dados pode ser um pouco demorada. Ter acesso a um SME (Subject Matter Expert, ou Especialista no Assunto), que dê orientações sobre como lidar com dados discrepantes **(outliers)** ou ausentes poderá ajudar.

## Crie os atributos

Devemos criar atributos úteis e descartar colunas que não contribuem para o modelo. Isso inclui:  

- **Colunas sem variação:** se todos os valores forem iguais, a coluna não fornece informação relevante.  
- **Colunas irrelevantes ou únicas:** colunas com valores muito distintos, como nomes ou identificadores, não ajudam o modelo, a menos que se extraia informação útil (por exemplo, categorias ou títulos).  
- **Colunas que causam vazamento de dados:** qualquer coluna que revele indiretamente a resposta que queremos prever deve ser removida, pois pode enviesar o modelo.  
## Separe as amostras
Sempre que iremos fazer o treinamento e testes devemos utilizar dados distintos. Você não saberá realmente quão bem seu modelo poderá ser generalizado para dados que ainda não tenham sido vistos antes.

>==Geralmente o recomendado é 30% pra teste e 70% para treino==

## Normalize os dados

Normalizar ou pré-processar os dados ajudará muitos modelos a terem um melhor desempenho depois, particularmente, para aqueles que dependam de uma métrica de distância para determinar a semelhança. (Observe que modelos em árvore, que tratam cada atributo por si só, não têm esse requisito.) 

Vamos padronizar os dados para o pré-processamento. Padronizar significa traduzir os dados de modo que tenham um valor de média igual a zero e um desvio-padrão igual a um. Desse modo, os modelos não tratarão as variáveis com escalas maiores como mais importantes que as variáveis com menor escala.


## Modelo de base

Criar um modelo simples fornece uma **linha de base** para comparação com modelos mais complexos.  

- Cuidado ao usar a **precisão (`.score`) padrão**, pois ela pode ser enganosa.  
  - Exemplo: se um caso positivo ocorre 1 em 10 mil, um modelo que sempre prevê negativo terá mais de 99% de precisão, mas não é útil.  
  
> **Dica:** Sempre teste sua base de dados com um **modelo base** antes de usar modelos mais complexos.  
> Se o modelo base apresentar bom desempenho, mas o modelo complexo falhar, **algo está errado** no processo ou nos dados.

## Crie o modelo

- **Escolha o modelo** mais adequado para a sua demanda.  
- **Treine o modelo** com os dados previamente separados (treino, validação/teste) para evitar **vazamento de informações** e garantir avaliações confiáveis.

# Avaliação do Modelo

- Depois de treinar o modelo, use os **dados de teste** para verificar sua **capacidade de generalização**.  
- O método `.score` de um classificador retorna a **média da precisão das predições**.  
- Sempre aplique `.score` nos **dados de teste**, pois o desempenho nos dados de treinamento tende a ser melhor e não representa a generalização do modelo.
