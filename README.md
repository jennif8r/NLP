# Natural Language Processing (NLP)

## O que é?

NLP, ou Processamento de Linguagem Natural (do inglês, Natural Language Processing), é um campo da inteligência artificial focado na interação entre computadores e a linguagem humana. Esse campo envolve a capacidade das máquinas de ler, interpretar, compreender e responder à linguagem escrita ou falada de maneira significativa para os seres humanos.

## Exemplos

- **Análise de Sentimentos**: Identificação de sentimentos e emoções em texto, como analisar opiniões em redes sociais ou avaliações de produtos.
- **Reconhecimento de Fala**: Transformação de fala em texto, como em assistentes de voz (Siri, Google Assistant).
- **Tradução Automática**: Tradução de texto de um idioma para outro, como o Google Tradutor.
- **Chatbots e Assistentes Virtuais**: Sistemas que conversam com usuários, respondendo perguntas e executando tarefas.
- **Análise de Texto**: Extração de informações e resumos de grandes volumes de texto.
- **Classificação de Texto**: Organização de documentos em categorias, como filtragem de spam em emails.
- **Correção e Sugestão de Texto**: Ferramentas que corrigem erros gramaticais e sugerem melhorias, como o Grammarly.

## Conceitos Básicos

### Corpus
Conjunto de documentos (texto não estruturado) em linguagem natural.

![Exemplo](/Imagem/corpus.png)


### Anotações (Annotations)
Técnica de localizar e classificar elementos específicos de um texto.
- **Exemplo**: Anotar sentimentos para treinar um modelo de IA.
- **Ferramentas especializadas**: Doccano, Brat

![Exemplo](/Imagem/Anotação.png)

### Tokenization
Processo de separar a sentença em suas partes: palavras, pontos, símbolos.

![Exemplo](/Imagem/Tokenization.png)

### Parts-of-Speech Tagging (POS)
Adiciona tags a cada token, como por exemplo, se é verbo, substantivo, etc.


![Exemplo](/Imagem/Parts-of-Speech%20Taggong%20(POS).png)

### Lemmatizing (Lemma)
Traz a palavra na sua flexão, de modo que possam ser analisadas juntas.
- **Exemplo**: Amigo, amigos, amiga, amigas => amigo

![Exemplo](/Imagem/Lemmatizing.png)

### Stemming
Corta palavras, buscando ter uma representação raiz e única. É menos sofisticado que o Lemmatization.

![Exemplo](/Imagem/Stremming.png)

### Dependency Parsing
Encontra relação entre palavras "pais" e "filhos".

![Exemplo](/Imagem/Dependency%20Parsing.png)

### NGRAM
Trata palavras consecutivas (n palavras consecutivas).

- Bigrams e trigams: ou seja, vai tratar duas ou três palavras consecutivas. 

- 4 ou mais não usado para palavras devido a esparsidade. 

- Pode também ser aplicado a letras. 

Exemplo: Vamos considerar a frase: "Eu gosto de aprender NLP".

- **Unigram (n=1)**: "Eu", "gosto", "de", "aprender", "NLP"
- **Bigram (n=2)**: "Eu gosto", "gosto de", "de aprender", "aprender NLP"
- **Trigram (n=3)**: "Eu gosto de", "gosto de aprender", "de aprender NLP"

## Modelo

Um modelo é um banco de dados linguístico específico de cada idioma. A maioria das bibliotecas de NLP tem seus próprios modelos, mas você pode criar o seu.

## Representação Computacional de Texto
Os computadores são máquinas digitais que processam dados na forma de números binários (0s e 1s). Essa representação binária é a linguagem nativa dos computadores, permitindo a execução de instruções e o armazenamento de dados de maneira eficiente e confiável. No entanto, muitas das informações que queremos processar, como texto, imagens e áudio, não estão naturalmente em formato binário estruturado. Por isso, precisamos de técnicas para converter essas informações em representações que os computadores possam manipular. 

Quando falamos de texto, estamos lidando com informações não estruturadas. Para que um computador consiga processar e compreender texto de maneira eficiente, é necessário transformar essas palavras em uma forma numérica que preserve o significado e as relações semânticas entre elas. É aqui que entra o conceito de word embedding. 
## Word Embedding
É uma técnica ou técnicas capazes de representar texto de forma estrutura e forma numérica. Ou seja, representação computacionais de texto.  

#### One Hot Encoding
Forma mais simples de word embedding.

![Exemplo](/Imagem/One%20hot%20Encoding.png)

Limitação:  

- se tiver um texto muito grande (corpus muito grande) você pode ter milhares ou milhões de elementos, e isso torna a matriz muito grande e tensa.  

- Outro problema é que as palavras são representadas sem contexto.

#### TF-IDF
Representa as palavras de acordo com a frequência nos documentos, mostrando a importância de cada palavra.

Exemplo:  testar em PROCESSO, ele vai ver as palavras em comum no documento e 	as incomuns.  

- Palavras Comum: Processo, lei, partes.  

- Palavras Incomum: Ambiental.  

![Exemplo](/Imagem/TF-IDF.png)

#### Word2Vec
Treinamento que produz um vetor demonstrando matematicamente a relação entre palavras.
- **CBOW**: Prever uma palavra central no seu contexto.
- **Skip-gram**: Prever o contexto a partir de uma palavra central.
- **Outras formas**: FastText, Glove, Bert

## Pipeline
Maneira Geral:

![Exemplo](/Imagem/Pipeline.png)

### Bibliotecas

Existem diversas bibliotecas que facilitam o trabalho com NLP. Elas fornecem ferramentas e modelos prontos para diversas tarefas, como tokenização, POS tagging, lematização, e embeddings. Algumas das mais populares são: 

- **NLTK (Natural Language Toolkit)**: Uma das bibliotecas mais antigas e completas para tarefas de NLP.
- **spaCy**: Conhecida por sua eficiência e modelos pré-treinados de alta qualidade.
- **Transformers (Hugging Face)**: Focada em modelos de deep learning, especialmente para tarefas complexas como tradução e geração de texto.
- **Gensim**: Excelente para modelagem de tópicos e embeddings.
- **Stanford NLP**: Oferece uma ampla gama de ferramentas para várias tarefas de NLP.

Essas bibliotecas são essenciais para desenvolver aplicações que envolvem processamento de linguagem natural, permitindo a construção de sistemas mais inteligentes e capazes de entender e interagir com os seres humanos de maneira mais natural.
