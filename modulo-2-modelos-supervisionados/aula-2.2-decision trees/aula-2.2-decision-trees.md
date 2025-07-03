# 🌳 Introdução às Árvores de Decisão
---

## 🧠 Por que aprender Árvores de Decisão?

As árvores de decisão são uma excelente porta de entrada para o mundo do machine learning por dois motivos principais:

* **Facilidade de interpretação:** é possível entender claramente o que está motivando uma decisão do modelo.
* **Processo lógico:** seguem um raciocínio próximo ao humano, facilitando a análise e validação por especialistas da área.

---

## 📊 O que você vai ver aqui?

Para facilitar o entendimento, utilizamos um exemplo bem prático: a classificação de **peixes** com base em características como **brilho** e **tamanho**. Nosso objetivo é prever se um peixe é **Salmão** ou **Sea Bass (Badejo)**.

Durante essa jornada, você vai acompanhar:

* Como é construída uma árvore de decisão a partir de um conjunto de dados.
* Como definimos as regras de decisão com base nos atributos.
* Como avaliamos a “qualidade” das divisões usando o **índice de Gini** — uma medida de impureza bastante comum em modelos de classificação.

---

## 🧪 Como funciona na prática?

Começamos com uma pequena base de dados contendo:

* `Brilho`: medida de frescor ou qualidade do peixe.
* `Tamanho`: comprimento do peixe.
* `Classificação`: rótulo com a espécie (Salmão ou Sea Bass).

A partir disso, construímos uma árvore com regras como:

```text
Se Tamanho > 25 ➡️ Salmão  
Se Tamanho <= 25 e Brilho > 0.9 ➡️ Salmão  
Se Tamanho <= 25 e Brilho <= 0.9 ➡️ Sea Bass  
```

Essas regras são criadas de forma automática, com base na melhor divisão dos dados segundo o índice de Gini. Quanto menor o valor do Gini, mais "pura" é a divisão, ou seja, melhor é a separação entre as classes.

---

## 🧮 Um pouco de matemática (sem exagero!)

O índice de Gini é calculado assim:

```
Gini = 1 - ∑ (p_i²)
```

Onde `p_i` é a proporção de elementos da classe `i` em um grupo. Testamos várias divisões nos dados e escolhemos aquela que gera o menor índice Gini — isto é, a divisão mais “limpa”.

---

## 🔁 E depois?

Esse processo é repetido em cada grupo de dados criado até que não haja mais impurezas — ou seja, até que cada ramo da árvore leve a uma única classe.

Assim, obtemos uma **árvore de decisão completa**, pronta para classificar novos dados com base nas regras extraídas do conjunto original.

---
