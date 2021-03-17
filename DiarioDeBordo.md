

# Resumo das atividades realizadas no estudo de NLP

## Dia xx/xx/xxxx - NLP BÁSICO

## Dia xx/xx/xxxx - CNNs PARA NLP

### Teoria:

#### CNN Básica:

#### Tratamento com Textos:

* ONE-HOT ENCODING
  * Não existe medidor de relação entre as palavras;
  * Representação fácil, mas não efetiva.

![image](https://user-images.githubusercontent.com/45316134/111528056-6e690d80-873f-11eb-92c8-82bdc8a55339.png)

* WORD EMBEDDING
  * Vetor menor;
  * Adiciona a relação entre as palavras;
  * ML somente para fazer os cálculos;
  * Sentido parecido -> Contexto parecido -> Embedding parecido.

![image][(https://user-images.githubusercontent.com/45316134/111528267-b5570300-873f-11eb-924e-ff1096a5666d.png) | width=100]

#### Arquitetura para NLP

![image](https://user-images.githubusercontent.com/45316134/111528316-c3a51f00-873f-11eb-832b-d1beebb75139.png)


* A convolução dos Kernels se dá de cima para baixo, nunca variando a quantidade de colunas;
* Pooling e Concatenação dos filtros;
* Não é necessário Flatenning, pois a saída da camada de pooling já será um vetor vertical;
* Finaliza na camada densa, que gerará uma resposta.


#### Artigos de Referência:
- [A Visual Guide to Using BERT for the First Time](http://jalammar.github.io/a-visual-guide-to-using-bert-for-the-first-time)
- [BERT Explained: A Complete Guide with Theory and Tutorial](https://towardsml.com/2019/09/17/bert-explained-a-complete-guide-with-theory-and-tutorial/)
- [A Simple Guide On Using BERT for Binary Text Classification.](https://medium.com/swlh/a-simple-guide-on-using-bert-for-text-classification-bbf041ac8d04)
- [BERT Word Embeddings Tutorial](http://mccormickml.com/2019/05/14/BERT-word-embeddings-tutorial/)


### Prática:
#### Tutorial Utilizado:
- [Udemy - Processamento de Linguagem Natural com Deep Learning (3h)](https://www.udemy.com/share/102C53B0QfdVhRTHk=/)

#### Primeiro Algoritmo com BERT (KTrain)
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

## Dia xx/xx/xxxx - RNNs PARA NLP

## Dia xx/xx/xxxx - INTRODUÇÃO AOS MODELOS MODERNOS

## Dia xx/xx/xxxx - ARQUITETURA TRANSFORMER

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


## Dia xx/xx/xxxx - BERT

## Dia xx/xx/xxxx - CHATBOTS
