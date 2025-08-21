Engenharia de prompt é a prática de projetar prompts mais eficazes e limpos a LLMs, a fim de alcançar resultados melhores e desejados.


## Tokens
## Definição Básica

Em essência, um **token** é a unidade fundamental de informação que um Grande Modelo de Linguagem (LLM) processa. Pense neles como os "blocos de construção" que o modelo usa para entender e gerar texto.

Ao contrário do que se poderia imaginar, um LLM não lê uma frase inteira como nós. Em vez disso, ele a divide em pedaços menores e mais gerenciáveis, que são os tokens. A forma como o texto é dividido em tokens é determinada por um algoritmo chamado **tokenizer**.

## Por que Tokens são Usados?

Os LLMs não conseguem processar texto diretamente.O processo de **tokenização** é a ponte que converte o texto legível por humanos em uma sequência de números que o modelo pode processar.

## O Processo: Da Frase ao Token

Vamos ver um exemplo prático com a frase: **"O gato pulou."**

O tokenizer poderia dividir essa frase nos seguintes tokens:

* "O"
* " gato"
* " pulou"
* "."

Note que, muitas vezes, o espaço antes da palavra é incluído no token. Isso é uma característica comum de muitos tokenizers e ajuda o modelo a entender a estrutura da frase.

A sequência de tokens é então convertida em uma sequência de números que o LLM pode processar para prever o próximo token na sequência.

## Impacto e Importância dos Tokens

Compreender os tokens é crucial por algumas razões:

* **Custo:** As APIs de modelos de linguagem cobram com base na quantidade de tokens processados (tanto na entrada quanto na saída). Quanto mais tokens você usa, mais caro fica.
* **Janela de Contexto (Context Window):** Os LLMs têm um limite de quantos tokens podem processar de uma só vez. Esse limite é chamado de "janela de contexto". Se a sua solicitação (prompt e contexto) exceder esse limite, o modelo não conseguirá processar tudo.
* **Eficiência:** Tokenizers eficientes podem compactar informações de maneira mais eficaz, permitindo que mais texto caiba na janela de contexto. Por exemplo, em vez de dividir "internacionalização" em 18 caracteres, ele pode dividi-la em 4 ou 5 subtokens.
## LLMs

Grandes Modelos de Linguagem (LLMs) são sistemas de IA já treinados com vastos dados que utiliza NLP(Processamento de linguagem natural) a área que a semelha à linguagem humana. Eles utilizam mecanismos de previsão, analisa as entradas e preveem o próximo token mais provável. Assim as LLMs conseguem realizar tarefas como: **geração de texto, tradução, sumarização**. ==Compreender o prcessamento de tokens é um passo fundamental para insignht melhores e efizares gerados por essas LLMs.== 

Exemplo de LLMs: chatgpt, deepsheek, gemini.
