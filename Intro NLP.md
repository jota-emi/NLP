# Introdução

## Definição
O Processamento de Linguagem Natural (PLN ou NLP) mescla ciência da computação, inteligência artificial e linguística se dedicando a geração e compreensão automática da linguagem natural.  Alguns desafios do PLN são compreensão de língua natural, fazer com que computadores extraiam sentido de linguagem humana ou natural e geração de língua natural.
## Bibliotecas Iniciais
  ### NLTK
  ### SpaCy
  
## Conceitos Básicos
  ### Tokenization
  Tokenization is breaking the raw text into small chunks. Tokenization breaks the raw text into words, sentences called tokens. These tokens help in understanding the context or developing the model for the NLP. The tokenization helps in interpreting the meaning of the text by analyzing the sequence of the words.
For example, the text “It is raining” can be tokenized into ‘It’, ‘is’, ‘raining’
  ### Stemming
  Stemming is basically removing the suffix from a word and reduce it to its root word.
For example: “Flying” is a word and its suffix is “ing”, if we remove “ing” from “Flying” then we will get base word or root word which is “Fly”.
  ### Lemmatization
  In simpler forms, a method that switches any kind of a word to its base root mode is called Lemmatization. 

 

In other words, Lemmatization is a method responsible for grouping different inflected forms of words into the root form, having the same meaning. It is similar to stemming, in turn, it gives the stripped word that has some dictionary meaning. The Morphological analysis would require the extraction of the correct lemma of each word. 

 

For example, Lemmatization clearly identifies the base form of ‘troubled’ to ‘trouble’’ denoting some meaning whereas, Stemming will cut out ‘ed’ part and convert it into ‘troubl’ which has the wrong meaning and spelling errors.

 

‘troubled’ -> Lemmatization -> ‘troubled’, and error

‘troubled’ -> Stemming -> ‘troubl’

COLOCAR IMAGEM DA COMPARAÇÃO
  ### Stop Words
  In computing, stop words are words that are filtered out before or after the natural language data (text) are processed. While “stop words” typically refers to the most common words in a language, all-natural language processing tools don’t use a single universal list of stop words.
 Stopwords are the words in any language which does not add much meaning to a sentence. They can safely be ignored without sacrificing the meaning of the sentence. For some search engines, these are some of the most common, short function words, such as the, is, at, which, and on. In this case, stop words can cause problems when searching for phrases that include them, particularly in names such as “The Who” or “Take That”.
When to remove stop words?
If we have a task of text classification or sentiment analysis then we should remove stop words as they do not provide any information to our model, i.e keeping out unwanted words out of our corpus, but if we have the task of language translation then stopwords are useful, as they have to be translated along with other words.
 ### Bag of Words
 The bag-of-words (BOW) model is a representation that turns arbitrary text into fixed-length vectors by counting how many times each word appears. This process is often referred to as vectorization.
Let’s understand this with an example. Suppose we wanted to vectorize the following:
the cat sat
the cat sat in the hat
the cat with the hat
We’ll refer to each of these as a text document.
Step 1: Determine the Vocabulary
We first define our vocabulary, which is the set of all words found in our document set. The only words that are found in the 3 documents above are: the, cat, sat, in, the, hat, and with.
Step 2: Count
To vectorize our documents, all we have to do is count how many times each word appears:
Image for post
Now we have length-6 vectors for each document!
the cat sat: [1, 1, 1, 0, 0, 0]
the cat sat in the hat: [2, 1, 1, 1, 1, 0]
the cat with the hat: [2, 1, 0, 0, 1, 1]
Notice that we lose contextual information, e.g. where in the document the word appeared, when we use BOW. It’s like a literal bag-of-words: it only tells you what words occur in the document, not where they occurred.
Implementing BOW in Python
Now that you know what BOW is, I’m guessing you’ll probably need to implement it. Here’s my preferred way of doing it, which uses Keras’s Tokenizer class:

Running that code gives us:
Vocabulary: ['the', 'cat', 'sat', 'hat', 'in', 'with']
[[0. 1. 1. 1. 0. 0. 0.]
 [0. 2. 1. 1. 1. 1. 0.]
 [0. 2. 1. 0. 1. 0. 1.]]
Notice that the vectors here have length 7 instead of 6 because of the extra 0 element at the beginning. This is an inconsequential detail - Keras reserves index 0 and never assigns it to any word.
How is BOW useful?
Despite being a relatively basic model, BOW is often used for Natural Language Processing (NLP) tasks like Text Classification. Its strengths lie in its simplicity: it’s inexpensive to compute, and sometimes simpler is better when positioning or contextual info aren’t relevant.
I’ve written a blog post that uses BOW for profanity detection — check it out if you’re curious to see BOW in action!
  
## Exercício: Perguntas e Respostas
  ### Métricas de Comparação
