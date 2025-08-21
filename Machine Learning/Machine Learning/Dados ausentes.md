Maioria dos algoritmos não funcionará com a ausência dos dados. Claro, existe exceções como as bibliotecas: XGBoost, CatGoost e LightGBM, que permite você passar datasets com ausências de dados.

Assim como ocorre em relação a várias questões no machine learning, não há respostas únicas sobre como tratar dados ausentes. Além do mais, a ausência de dados poderia representar diferentes situações. Suponha que tenhamos recebido dados de censo e que um atributo idade tenha sido informado como ausente. Isso é porque a amostra não quis revelar a sua idade? Não sabia a idade? Quem fez as perguntas se esqueceu de pedi-la? Há algum padrão para as idades ausentes? Ela está correlacionada com outro atributo? Ou é totalmente aleatória?

Há também diversas maneiras de lidar com dados ausentes:

• remover qualquer linha com dados ausentes;
• remover qualquer coluna com dados ausentes;
• imputar dados aos valores ausentes;
• criar uma coluna para informar que os dados estavam ausentes.

## Imputando dados

# Imputação de Dados (Imputation)

A **imputação de dados** é o processo de **preencher valores ausentes em um conjunto de dados** utilizando técnicas estatísticas ou de aprendizado de máquina. Em vez de simplesmente remover registros incompletos, a imputação permite **aproveitar toda a informação disponível**, mantendo a integridade e representatividade do conjunto de dados.

O objetivo é identificar **padrões nos dados existentes** e usar esses padrões para prever os valores ausentes, mesmo que haja alguma margem de erro. Existem diversas estratégias de imputação, incluindo:

- **Imputação simples:** preencher valores ausentes com a média, mediana ou moda da coluna.  
- **Imputação baseada em regressão:** utilizar modelos de regressão para prever os valores ausentes a partir de outras variáveis.  
- **Imputação por KNN (K-Nearest Neighbors):** estimar o valor ausente com base nos registros mais semelhantes.  
- **Imputação múltipla:** gerar várias previsões para cada valor ausente e combinar os resultados, aumentando a robustez da imputação.

A imputação de dados é essencial para **manter a qualidade das análises**, pois muitos algoritmos de aprendizado de máquina não lidam bem com valores ausentes e podem gerar resultados enviesados se esses dados forem ignorados.
