
# Aula 1.4 – K-Nearest Neighbors (KNN) 👥📏
---
## 📌 O que é o KNN?

O KNN é um algoritmo supervisionado que **não precisa ser treinado** da forma tradicional. Ele guarda os dados de treinamento e, quando precisa fazer uma previsão, **compara o novo dado com os mais próximos** em termos de distância.

A ideia é: **“diga-me com quem tu andas, que eu te direi quem és”**. Se a maioria dos vizinhos próximos pertence à classe “A”, o novo ponto provavelmente também será da classe “A”.

---

## 🧮 Entendendo a Distância Euclidiana

Antes de usar o KNN, é essencial saber como calcular a **distância entre dois pontos**. O tipo mais comum é a **distância euclidiana**, que você provavelmente já viu no ensino médio com o Teorema de Pitágoras.

### 🔢 Exemplo simples:
A distância entre os pontos `2` e `5` é:

```python
dist = ((2 - 5)**2)**0.5  # Resultado: 3.0
````

### 🧑‍🍳 Agora com dois atributos:

Imagine frutas com duas características: **massa** e **cor**.

```python
a = [5, 0.75]  # fruta A
b = [2, 0.50]  # fruta B

# Distância euclidiana entre elas:
dist = ((5 - 2)**2 + (0.75 - 0.50)**2)**0.5  # Resultado: ≈ 3.01
```

Essa fórmula pode ser estendida para **quantas dimensões forem necessárias** — ou seja, para quantas colunas tiverem no seu conjunto de dados.

---

## ⚙️ O que aprendemos nesta aula

* O que é o algoritmo **k-Nearest Neighbors (KNN)**.
* Como ele utiliza a **distância** entre dados para prever rótulos.
* Como calcular a **distância euclidiana** para dados com uma ou mais variáveis.
* Como isso se aplica a **classificação e regressão**.
* A importância de escolher **um valor adequado para "k"** (quantidade de vizinhos).
* Como usá-lo com a biblioteca **Scikit-learn**.

---

## 🛠️ Aplicações do KNN

* Reconhecimento de padrões
* Classificação de imagens
* Análise de crédito
* Diagnósticos médicos
* Recomendação de produtos

---

## 📚 Próximos passos

No próximo conteúdo, veremos:

* A **intuição visual do KNN**
* Como **implementar o modelo no Python**
* E como **avaliar seu desempenho** com métricas como a **acurácia**

---

*O KNN é um ótimo ponto de partida para aprender sobre modelos baseados em distância. Compreendendo bem a ideia de proximidade, você vai estar preparado para avançar em muitos outros algoritmos de Machine Learning!*

```
