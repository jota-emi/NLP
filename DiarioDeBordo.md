

# Resumo das atividades realizadas no estudo de NLP

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
