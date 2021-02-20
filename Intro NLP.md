# Introdução

## Definição
O Processamento de Linguagem Natural (PLN ou NLP) mescla ciência da computação, inteligência artificial e linguística se dedicando a geração e compreensão automática da linguagem natural.  Alguns desafios do PLN são compreensão de língua natural, fazer com que computadores extraiam sentido de linguagem humana ou natural e geração de língua natural.
## Bibliotecas Iniciais
  ### NLTK
  ### SpaCy
  
## Conceitos Básicos
  ### Tokenization
  A tokenização é o processo de quebrar o texto bruto em pequenos pedaços. A tokenização divide o texto bruto em palavras, frases chamadas tokens. Esses tokens ajudam a compreender o contexto ou desenvolver o modelo para o processamento. A tokenização ajuda a interpretar o significado do texto, analisando a sequência das palavras.
Por exemplo, o texto “It is raining” pode ser transformado em ‘It’, ‘is’, ‘raining.

NA PRÁTICA (FALTA ADICIONAR)
  ### Stemming
  Stemming é basicamente a remoção do sufixo de uma palavra, reduzindo-a para o radical. Por exemplo: "Flying é uma palavra e seu sufixo é "ing", que indica ação presente, entretando, remove-se o "ing", deixando apenas o radical "Fly", que é a expressão que dá significado a palavra.
  
  NA PRÁTICA (FALTA ADICIONAR)
  
  ### Lemmatization
  Em resumo, Lemmatization é um método responsável por agrupar diferentes formas flexionadas de palavras, tendo o mesmo significado. É semelhante ao radical do Stemming, mas por sua vez, fornece a palavra que tem algum significado no dicionário. A análise morfológica exigiria a extração do lema correto de cada palavra.

Por exemplo, a Lemmatização identifica claramente a forma básica de ‘troubled’ para ‘trouble’ denotando algum significado, enquanto que o Stemming cortará a parte ‘ed’ e a converterá em ‘troubl’, que tem o significado errado e erros ortográficos.

‘Troubled’ -> Lematização -> ‘troubled’ e erro

‘Troubled’ -> Stemming -> ‘troubl’

COLOCAR IMAGEM DA COMPARAÇÃO

NA PRÁTICA (FALTA ADICIONAR)

### Stop Words
 Na computação, stop-words são palavras filtradas antes ou depois do processamento dos dados de linguagem natural (texto). Embora "stop words" normalmente se refiram às palavras mais comuns em um idioma, as ferramentas de processamento de linguagem totalmente natural não usam uma única lista universal de palavras irrelevantes.
 Stop words são palavras em qualquer idioma que não acrescentam muito significado a uma frase. Eles podem ser ignoradas com segurança sem sacrificar o significado da frase. Para alguns mecanismos de pesquisa, essas são algumas das palavras de função curtas mais comuns, como, "é", "em", "qual" e assim por diante. Nesse caso, as palavras irrelevantes podem causar problemas ao pesquisar frases que as incluam, especialmente em nomes como “The Who” ou “Take That”.
 
Quando remover palavras de parada?
Se temos uma tarefa de classificação de texto ou análise de sentimento, devemos remover as palavras irrelevantes, uma vez que não fornecem nenhuma informação ao nosso modelo, ou seja, manter as palavras indesejadas fora do nosso corpus, mas se temos a tarefa de tradução de idiomas, as palavras irrelevantes são úteis, pois devem ser traduzidos junto com outras palavras.

NA PRÁTICA (FALTA ADICIONAR)

 ### Bag of Words
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

NA PRÁTICA (FALTA ADICIONAR)

## Exercício: Perguntas e Respostas
  ### Métricas de Comparação
