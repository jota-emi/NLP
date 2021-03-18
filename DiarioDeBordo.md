

# Resumo das atividades realizadas no estudo de NLP

## Dia 08/02/2021 - CONCEITOS BÁSICOS

### Definição
O Processamento de Linguagem Natural (PLN ou NLP) mescla ciência da computação, inteligência artificial e linguística se dedicando a geração e compreensão automática da linguagem natural.  Alguns desafios do PLN são compreensão de língua natural, fazer com que computadores extraiam sentido de linguagem humana ou natural e geração de língua natural.
### Bibliotecas Iniciais
  * NLTK
  * SpaCy
  
### Conceitos Básicos
  #### Tokenization
  A tokenização é o processo de quebrar o texto bruto em pequenos pedaços. A tokenização divide o texto bruto em palavras, frases chamadas tokens. Esses tokens ajudam a compreender o contexto ou desenvolver o modelo para o processamento. A tokenização ajuda a interpretar o significado do texto, analisando a sequência das palavras.
Por exemplo, o texto “It is raining” pode ser transformado em ‘It’, ‘is’, ‘raining.

  #### Stemming
  Stemming é basicamente a remoção do sufixo de uma palavra, reduzindo-a para o radical. Por exemplo: "Flying é uma palavra e seu sufixo é "ing", que indica ação presente, entretando, remove-se o "ing", deixando apenas o radical "Fly", que é a expressão que dá significado a palavra.
  

  
  #### Lemmatization
  Em resumo, Lemmatization é um método responsável por agrupar diferentes formas flexionadas de palavras, tendo o mesmo significado. É semelhante ao radical do Stemming, mas por sua vez, fornece a palavra que tem algum significado no dicionário. A análise morfológica exigiria a extração do lema correto de cada palavra.

Por exemplo, a Lemmatização identifica claramente a forma básica de ‘troubled’ para ‘trouble’ denotando algum significado, enquanto que o Stemming cortará a parte ‘ed’ e a converterá em ‘troubl’, que tem o significado errado e erros ortográficos.

‘Troubled’ -> Lematização -> ‘troubled’ e erro

‘Troubled’ -> Stemming -> ‘troubl’

COLOCAR IMAGEM DA COMPARAÇÃO



#### Stop Words
 Na computação, stop-words são palavras filtradas antes ou depois do processamento dos dados de linguagem natural (texto). Embora "stop words" normalmente se refiram às palavras mais comuns em um idioma, as ferramentas de processamento de linguagem totalmente natural não usam uma única lista universal de palavras irrelevantes.
 Stop words são palavras em qualquer idioma que não acrescentam muito significado a uma frase. Eles podem ser ignoradas com segurança sem sacrificar o significado da frase. Para alguns mecanismos de pesquisa, essas são algumas das palavras de função curtas mais comuns, como, "é", "em", "qual" e assim por diante. Nesse caso, as palavras irrelevantes podem causar problemas ao pesquisar frases que as incluam, especialmente em nomes como “The Who” ou “Take That”.
 
Quando remover palavras de parada?
Se temos uma tarefa de classificação de texto ou análise de sentimento, devemos remover as palavras irrelevantes, uma vez que não fornecem nenhuma informação ao nosso modelo, ou seja, manter as palavras indesejadas fora do nosso corpus, mas se temos a tarefa de tradução de idiomas, as palavras irrelevantes são úteis, pois devem ser traduzidos junto com outras palavras.


 #### Bag of Words
O modelo de saco de palavras (BOW) é uma representação que transforma texto arbitrário em vetores de comprimento fixo, contando quantas vezes cada palavra aparece. Esse processo geralmente é denominado vetorização.

Vamos entender isso com um exemplo. Suponha que desejamos vetorizar o seguinte:

o gato sentou

o gato sentou no chapéu

o gato com o chapéu

Vamos nos referir a cada um deles como um documento de texto.

Etapa 1: determinar o vocabulário

Primeiro definimos nosso vocabulário, que é o conjunto de todas as palavras encontradas em nosso conjunto de documentos. As únicas palavras encontradas nos 3 documentos acima são: the, cat, sat, in, the, hat e with.

Etapa 2: contar

Para vetorizar nossos documentos, tudo o que precisamos fazer é contar quantas vezes cada palavra aparece:

Imagem para postagem

Agora temos vetores de comprimento 6 para cada documento!
o gato sentou: [1, 1, 1, 0, 0, 0]
o gato sentou no chapéu: [2, 1, 1, 1, 1, 0]
o gato com o chapéu: [2, 1, 0, 0, 1, 1]

Observe que perdemos informações contextuais, por exemplo onde no documento a palavra apareceu, quando usamos BOW. É como um saco de palavras literal: apenas informa quais palavras ocorrem no documento, não onde ocorreram.

Como o BOW é útil?

Apesar de ser um modelo relativamente básico, o BOW é freqüentemente usado para tarefas de Processamento de Linguagem Natural (PNL), como Classificação de Texto. Seus pontos fortes estão na simplicidade: é barato de calcular e, às vezes, mais simples é melhor quando o posicionamento ou as informações contextuais não são relevantes.

## Dia 15/02/2021 - CNNs PARA NLP

### Teoria:

#### CNN Básica:
* ETAPA 1: CONVOLUÇÃO - Detectores de características
* ETAPA 2: MAX POOLING - Reduz dimensionalidade
* ETAPA 3: FLATENNING - Transformação para 1 vetor
* ETAPA 4: FULL CONECTION - Rede Neural Densa
#### Tratamento com Textos:

* ONE-HOT ENCODING
  * Não existe medidor de relação entre as palavras;
  * Representação fácil, mas não efetiva.
<img src="https://user-images.githubusercontent.com/45316134/111528056-6e690d80-873f-11eb-92c8-82bdc8a55339.png" width=75% height=75%>

* WORD EMBEDDING
  * Vetor menor;
  * Adiciona a relação entre as palavras;
  * ML somente para fazer os cálculos;
  * Sentido parecido -> Contexto parecido -> Embedding parecido.

<img src="https://user-images.githubusercontent.com/45316134/111528267-b5570300-873f-11eb-924e-ff1096a5666d.png" width=75% height=75%>

#### Arquitetura para NLP

<img src="https://user-images.githubusercontent.com/45316134/111528316-c3a51f00-873f-11eb-832b-d1beebb75139.png" width=75% height=75%>


* A convolução dos Kernels se dá de cima para baixo, nunca variando a quantidade de colunas;
* Pooling e Concatenação dos filtros;
* Não é necessário Flatenning, pois a saída da camada de pooling já será um vetor vertical;
* Finaliza na camada densa, que gerará uma resposta.


#### Artigos de Referência:
- [Understanding Convolutional Neural Networks for NLP](http://www.wildml.com/2015/11/understanding-convolutional-neural-networks-for-nlp/)
- [Word Embedding - Transformando palavras em números](https://iaexpert.academy/2019/04/12/word-embedding-transformando-palavras-em-numeros/)
- [Dot Product Explanation](https://www.mathsisfun.com/algebra/vectors-dot-product.html)


### Prática:
#### Tutorial Utilizado:
- [Udemy - Processamento de Linguagem Natural com Deep Learning (3h)](https://www.udemy.com/share/102C53B0QfdVhRTHk=/)

#### Primeiro Algoritmo com CNN para NLP:
- [Classificação de Sentimentos com CNN](https://colab.research.google.com/drive/1z9ml_AywmZ3rJllVvr43Ma-wws1qHkfR?usp=sharing)

#### Observações:

* Foi construída uma rede convolucional capaz de classificar sentimentos como positivos ou negativos, a partir de uma base de dados do Twitter.
* A maior parte do tempo exigido foi para o pré-processamento dos dados, incluindo limpeza, tokenização e padding. Vale muito a pena entender esses conceitos e a melhor maneira de preparar os dados para a rede.
* Devido a enorme quantidade de dados (1 milhão e 600 mil amostras), foi necessário reduzir a quantidade de dados para **480 mil amostras**, um valor ainda alto.
* Mesmo utilizando uma GPU no Colab, o treinamento de cada época da rede neural demorou cerca de 11 minutos, totalizando **quase 2 horas** para ser finalizado. A demora era até esperada devido a grande quantidade de dados, porém não tanto, pois a rede não era tão densa quanto poderia ser.
* A arquitetura da rede neural foi composta de:
   * **1 camada de Embedding**
   * **3 camadas de Convolução**
   * **3 camadas de Pooling**
   * **1 camada densa**
   * **1 camada de Dropout**
   * **1 camada densa de saída**
* O **resultado** foi regular, chegando a **76,7%** de acurácia nos dados de teste. Entretanto, foi observado um comportamento típico de **overfitting**, quando, a medida que as épocas se sucediam, menor a acurácia nos dados de validação e maior nos de treinamento.
* Para melhorar os resultados a melhor alternativa parece ser **aumentar a quantidade de dados utilizados e ajustar melhor os hiperparâmetros** da rede.

## Dia 16/02/2021 - RNNs PARA NLP

### Arquitetura:

<img src="https://user-images.githubusercontent.com/45316134/111684292-4ba12c80-8805-11eb-9ba7-2697b2426790.png" width=100% height=100%>

* Sistema de retroalimentação entre células;
* Pode ser:
  * One-to-Many
  * One´to-One
  * Many-to-One
  * Many-to-Many
 
### Vanish Gradient Problem
* Pesos da camada de retroalimentação tendem a ficar muito pequenos
#### Soluções
* Exploding:
  * Truncated Backpropagation;
  * Penalidades;
  * Gradient Clipping.
* Vanishing:
  * Inicialização dos pesos;
  * Echo State Networks;
  * LSTMs

### LSTMs

<img src="https://user-images.githubusercontent.com/45316134/111685196-62944e80-8806-11eb-824f-06b6bbc7aa51.png" width=70% height=70%>

* Forget Gates
* Seq-to-Seq
* Encoder e Decoder
* Cada novo estado é baseado no anterior
* Mecanismo de Atenção

#### Artigos de Referência:
- [Understanding RNNs](https://towardsdatascience.com/understanding-rnn-and-lstm-f7cdf6dfc14e)
- [On the difficulty of training recurrent neural networks](http://proceedings.mlr.press/v28/pascanu13.pdf)
- [Understanding LSTMs Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- [Understanding LSTMs and It's diagrams](https://medium.com/mlreview/understanding-lstm-and-its-diagrams-37e2f46f1714)

#### Tutorial Utilizado:
- [Udemy - Processamento de Linguagem Natural com Deep Learning (1h)](https://www.udemy.com/share/102C53B0QfdVhRTHk=/)


## Dia 22/02/2021 - INTRODUÇÃO AOS MODELOS MODERNOS

## Dia 23/02/2021 - ARQUITETURA TRANSFORMER

## Dia 01/03/2021 - INTRODUÇÃO AO BERT

#### Artigos de Referência:
- [A Visual Guide to Using BERT for the First Time](http://jalammar.github.io/a-visual-guide-to-using-bert-for-the-first-time)
- [BERT Explained: A Complete Guide with Theory and Tutorial](https://towardsml.com/2019/09/17/bert-explained-a-complete-guide-with-theory-and-tutorial/)
- [A Simple Guide On Using BERT for Binary Text Classification.](https://medium.com/swlh/a-simple-guide-on-using-bert-for-text-classification-bbf041ac8d04)
- [BERT Word Embeddings Tutorial](http://mccormickml.com/2019/05/14/BERT-word-embeddings-tutorial/)

#### Tutorial Utilizado:
- [Udemy - Natural Language Processing (NLP) with BERT (1h)](https://www.udemy.com/share/102RFuB0QfdVhRTHk=/)

#### Primeiro Algoritmo com BERT (KTrain)
- [Análise de Sentimento Binária em comentários do IMDB](https://colab.research.google.com/drive/1FxHkImkG7k4QaWtPjBEUH5wU3Nw6T2pM?usp=sharing)

#### Observações:

* Foi utilizada uma biblioteca chamada **Ktrain** que é simples e reduz muito a complexidade do programa, todavia o entendimento do uso dos parâmetros da rede treinada fica
prejudicado devido a simplicidade dos comandos.
* Mesmo utilizando uma GPU no Colab e apenas uma *epoch*, o treinamento da rede **demorou quase 2 horas** para ser finalizado.
* O **resultado** foi muito bom, chegando a **93,6%** de acurácia nos dados de teste.


## Dia 15/03/2021 - BERT

## Dia xx/xx/xxxx - CHATBOTS
