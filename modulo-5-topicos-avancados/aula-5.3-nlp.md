# 🧠 Introdução ao Processamento de Linguagem Natural (PLN)

Olá, seja bem-vindo(a)! 👋

Este material é uma introdução prática e conceitual ao fascinante mundo do **Processamento de Linguagem Natural (PLN)**, também conhecido como **NLP (Natural Language Processing)**. O foco é mostrar como os computadores podem entender, interpretar e trabalhar com a linguagem humana, seja falada ou escrita.

## 📌 Por que isso importa?

Vivemos cercados por tecnologias que dependem do PLN:

* Chatbots em sites de atendimento
* Assistentes virtuais
* Aplicativos de tradução
* Sistemas de busca por voz
* Análise de sentimentos e muito mais!

Essas aplicações estão cada vez mais inteligentes, graças ao uso de **machine learning** e técnicas de linguagem natural.

---

## 🧩 Conceitos Fundamentais

Durante o aprendizado, você irá entender conceitos essenciais como:

### 🔹 Corpus

É um conjunto de textos anotados manualmente que servem de base para o treinamento e validação de algoritmos de PLN.

### 🔹 Tokenização

É o processo de dividir um texto em partes menores chamadas **tokens**, que geralmente são palavras ou pontuações.

### 🔹 Stop Words

São palavras que, por não adicionarem muito significado (como “o”, “de”, “a”), podem ser removidas para simplificar a análise de texto.

---

## 🛠️ Colocando em prática com Python + NLTK

Utilizamos a biblioteca **NLTK (Natural Language Toolkit)** para aplicar esses conceitos na prática. Veja algumas etapas:

```python
!pip install nltk
import nltk
nltk.download('stopwords')
from nltk.corpus import stopwords
stopwords = stopwords.words('portuguese')
```

### Exemplo de Tokenização e remoção de stop words:

```python
from nltk.tokenize import word_tokenize
nltk.download('punkt')

frase = 'Eu dirijo devagar porque nós queremos ver os animais.'
tokens = word_tokenize(frase)

for t in tokens:
    if t.lower() not in stopwords:
        print(t)
```

Resultado: apenas palavras relevantes da frase são exibidas.

---

## 📈 TF-IDF: O que é importante em um texto?

Outra técnica essencial é o cálculo **TF-IDF (Term Frequency - Inverse Document Frequency)**. Ele identifica quais palavras são mais importantes em um documento, levando em conta:

* A frequência com que aparecem em um único texto (**TF**)
* E em quantos textos elas aparecem (**IDF**)

### Exemplo prático com Scikit-learn:

```python
from sklearn.feature_extraction.text import TfidfVectorizer
import pandas as pd

texto1 = 'A matemática é muito importante para compreendermos como a natureza funciona'
texto2 = 'A matemática é incrível, quanto mais estudo matemática, mais eu consigo aprender matemática'

tfidf = TfidfVectorizer()
vetor = tfidf.fit_transform([texto1, texto2]).todense()
nomes = tfidf.get_feature_names_out()

df = pd.DataFrame(vetor, columns=nomes)
print(df)
```

Esse código cria um DataFrame com os pesos de cada palavra, mostrando quais termos se destacam em cada texto. Por exemplo, “matemática” recebe maior peso no segundo texto por se repetir várias vezes.

---