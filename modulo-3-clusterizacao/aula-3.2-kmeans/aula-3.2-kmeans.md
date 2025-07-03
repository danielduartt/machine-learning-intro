# 🤖 Clusterização com K-means: Agrupando dados de forma inteligente
---

## 🧠 O que é Clusterização?

Clusterização é o processo de **agrupar elementos com características semelhantes**, com base em alguma métrica de distância. É muito usada para **descobrir padrões em grandes volumes de dados** que ainda não foram classificados. Essa técnica é muito aplicada em áreas como:

* 📊 Segmentação de clientes no marketing
* 🧬 Agrupamento de genes na biologia
* 🏥 Perfis de pacientes na saúde
* 🎧 Recomendação de músicas ou filmes

---

## 🔎 Como o algoritmo K-means funciona?

O **K-means** agrupa os dados com base na proximidade de seus valores em relação a pontos chamados de **centróides**, que representam o “centro” de cada grupo. O funcionamento básico segue estas etapas:

1. **Escolher o número de clusters (k)** desejado.
2. **Inicializar aleatoriamente os k centróides.**
3. **Atribuir cada ponto de dado ao centróide mais próximo**, com base em uma métrica de distância (geralmente a distância euclidiana).
4. **Atualizar os centróides**, calculando a média dos pontos atribuídos a cada grupo.
5. **Repetir os passos 3 e 4** até que os centróides não mudem mais significativamente (isso é chamado de *convergência*).

---

## 🧪 O que foi feito na prática?

Durante a aula, aplicamos o K-means usando Python, especificamente com a biblioteca `scikit-learn`. O dataset utilizado continha informações sobre **clientes de um shopping**, com atributos como:

* 💵 Renda anual
* 📈 Score de consumo

Esses dados foram visualizados em um gráfico de dispersão, e o algoritmo foi utilizado para formar grupos (clusters) de clientes com características parecidas.

Para determinar o número ideal de clusters, aplicamos o famoso **método do cotovelo (Elbow Method)**, que consiste em:

1. Rodar o K-means para diferentes valores de k (ex: de 1 a 10);
2. Calcular a soma das distâncias quadradas internas aos clusters (*inertia*);
3. Identificar o “cotovelo” do gráfico, ou seja, o ponto onde o ganho de performance começa a diminuir.

---

## 📈 Resultados obtidos

Após definir o número ideal de clusters, aplicamos o modelo ao dataset e visualizamos os agrupamentos por meio de gráficos com cores distintas, representando cada grupo de clientes. Com isso, foi possível identificar, por exemplo:

* Grupos de clientes com alta renda e baixo consumo (possível oportunidade de marketing)
* Clientes com consumo alto, mas renda média
* Clientes com baixa renda e baixo consumo (talvez menos prioritários para campanhas)

Essa segmentação permite **tomar decisões mais inteligentes e direcionadas**, seja para melhorar a comunicação, desenvolver produtos ou entender o comportamento dos usuários.

---

## ✅ Conclusão

O algoritmo K-means se mostrou **simples, eficiente e interpretável**, tornando-se uma ferramenta poderosa para quem trabalha com análise de dados. Mesmo sem conhecer previamente os grupos, conseguimos organizar e interpretar os dados de forma significativa.

Você aprendeu não só a teoria por trás do algoritmo, mas também **como aplicá-lo de forma prática e visual**, usando Python e bibliotecas amplamente adotadas no mercado.

---

## 🚀 Próximos passos sugeridos

* Aplicar o K-means em outros conjuntos de dados (clientes, produtos, vendas, etc.);
* Testar outras métricas de distância (como Manhattan);
* Comparar com outros métodos de clusterização, como DBSCAN ou métodos hierárquicos;
* Usar a clusterização como base para sistemas de recomendação ou segmentação de mercado real.

---
