
## 🧠 KNN para Classificação

Nesta etapa, conhecemos o algoritmo **KNN (k-Nearest Neighbors)** em sua aplicação para **classificação**. O modelo se baseia em uma ideia simples: ao receber um novo dado, ele verifica quais são seus **k vizinhos mais próximos** (com base na distância euclidiana, por exemplo) e o classifica de acordo com a **classe mais frequente** entre esses vizinhos.

### 📦 Como funciona?

* O modelo **não faz cálculos complexos internamente** nem cria fórmulas — ele apenas **armazena os dados de treino**.
* Quando um novo dado é apresentado, o algoritmo:

  1. Calcula a distância entre esse novo dado e todos os dados já conhecidos.
  2. Seleciona os `k` mais próximos.
  3. Verifica a classe predominante entre eles.
  4. Atribui essa classe ao novo dado.

### ⚙️ Implementação com `sklearn`

```python
from sklearn.neighbors import KNeighborsClassifier
knn = KNeighborsClassifier(n_neighbors=3)
```

### 📊 Usando um conjunto de dados (ex: frutas)

```python
import pandas as pd
from sklearn.model_selection import train_test_split

# Carregando dados
data = pd.read_table('fruit_data_with_colors.txt')
X = data[['mass', 'height', 'width', 'color_score']]
y = data['fruit_label']

# Dividindo em treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y)

# Treinando o modelo
knn.fit(X_train, y_train)

# Avaliando o modelo
print(knn.score(X_test, y_test))
```

### 📉 Avaliação

O desempenho inicial pode não ser muito alto (ex: 60%) e isso pode ser causado por **diferenças de escala entre os atributos**, como massa e cor. Como o KNN depende fortemente da **distância**, atributos com valores em escalas maiores podem dominar os cálculos. Solução? **Normalizar ou padronizar os dados**, o que será abordado nos próximos passos.

