# 🤖 Introdução à Inteligência Artificial: K-means, Neurônios Artificiais e Redes Neurais

Bem-vindo(a)! Nesta aula, você deu um grande passo na jornada do aprendizado de **Machine Learning** e **Redes Neurais**, explorando desde métodos de agrupamento até a estrutura básica de como uma rede neural funciona por dentro. Vamos recapitular de forma leve e didática o que foi abordado:

---

## 🎯 Parte 1: Clusterização com K-means

Você aprendeu sobre o **K-means**, um dos algoritmos de **aprendizado não supervisionado** mais populares. Ele é usado para **agrupar dados** com características semelhantes, sem a necessidade de rótulos.

### 🧠 Como funciona?

* Escolhe-se um número de grupos (k).
* O algoritmo posiciona k centróides.
* Cada ponto é atribuído ao centróide mais próximo.
* Os centróides são atualizados com base na média dos pontos atribuídos.
* O processo se repete até os grupos estabilizarem.

### 🛠️ Aplicação prática:

Você utilizou o K-means para agrupar **clientes de um shopping** com base em **renda anual** e **score de consumo**. Descobriu como o algoritmo pode ajudar empresas a entenderem melhor seu público-alvo.

---

## 🧩 Parte 2: O Neurônio Artificial (McCulloch-Pitts)

Em seguida, você mergulhou na base da **rede neural artificial**, conhecendo o **modelo de McCulloch-Pitts**.

### 🔍 O que é?

* Um modelo matemático simples inspirado nos neurônios biológicos.
* Possui **entradas binárias** (0 ou 1).
* Realiza um **somatório** dessas entradas.
* Compara o resultado a um **limiar**. Se ultrapassar, o neurônio “dispara” (saída = 1), caso contrário, não (saída = 0).

Este modelo é **a base para redes mais complexas**, por ser simples e eficiente.

---

## ⚙️ Parte 3: O Perceptron e Funções de Ativação

Você conheceu o **Perceptron**, uma evolução do neurônio de McCulloch-Pitts, que adiciona **pesos** às entradas, permitindo que cada entrada tenha importância diferente.

### 💡 Importância dos Pesos

* Cada entrada é multiplicada por um peso.
* Isso permite controlar a **sensibilidade do neurônio** a cada tipo de informação.

### ⚡ Funções de Ativação

Após o somatório ponderado, uma **função de ativação** transforma esse valor. Algumas que você viu:

* **Degrau (Step)**: retorna 0 ou 1 (ativa ou não ativa).
* **Linear**: retorna o valor original do somatório.
* **ReLU**: retorna 0 para valores negativos e o próprio valor se positivo. Muito usada em visão computacional.

---

## 🧠 Parte 4: Redes Neurais Multicamadas (MLP)

Você foi além do perceptron e entendeu o funcionamento das **redes neurais multicamadas** (Multilayer Perceptron – MLP).

### 🧱 Como funciona?

* Várias **camadas de neurônios** (entrada, ocultas e saída).
* Cada camada recebe os dados da anterior e **processa de forma mais especializada**.
* Essa estrutura permite que a rede **aprenda padrões mais complexos**, como imagens, sons, ou relações não-lineares entre dados.

---

## ❗ Parte 5: O Exemplo do “OU-Exclusivo” (XOR)

Um ótimo exemplo para demonstrar o poder das redes neurais foi o do **OU-Exclusivo (XOR)**, uma operação lógica que **não é linearmente separável**.

### 🧩 Por que isso é importante?

* Algoritmos simples, como **regressão logística**, não conseguem separar os dados de um problema XOR com uma única reta.
* Porém, com **duas camadas de neurônios**, é possível representar a saída correta combinando múltiplas "retas" (decisões).

### 🎯 Estrutura para resolver XOR:

1. Dois neurônios na primeira camada simulando as operações “E” e “OU”.
2. Um terceiro neurônio (segunda camada) combinando os resultados dos anteriores.
3. O resultado final identifica corretamente os casos em que **apenas uma entrada é verdadeira**, ou seja, resolve o problema do XOR.

Este exemplo mostra como redes neurais conseguem **representar relações não lineares**, algo que muitos algoritmos clássicos não conseguem.

---

## 🧪 O que vem a seguir?

No próximo passo, você irá começar a **implementar redes neurais** usando bibliotecas como o **Scikit-learn**, explorando como colocar tudo isso em prática com código.

---
