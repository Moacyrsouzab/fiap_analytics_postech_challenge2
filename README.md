# TECH CHALLENGE 2 - PÓS TECH FIAP 📊

> **Tech Challenge 2 - Data Analytics**
> Universidade FIAP - 2026

![Jupyter](https://img.shields.io/badge/Aplicação-Jupyter%20Notebook-orange)
![Python](https://img.shields.io/badge/Linguagem-Python-blue)
![Machine Learning](https://img.shields.io/badge/Tema-Classificação%20ML-purple)
![Status](https://img.shields.io/badge/Status-Concluído-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📌 Sobre o Projeto

**🍷 Case: Classificando a Qualidade de Vinhos com Machine Learning**

Este projeto tem como objetivo desenvolver um modelo de Machine Learning capaz de classificar a qualidade de vinhos a partir de variáveis físico-químicas, como acidez, teor alcoólico, densidade, dióxido de enxofre, pH, sulfatos e outros atributos laboratoriais.

Tradicionalmente, a avaliação da qualidade de vinhos é realizada por especialistas por meio de análise sensorial, considerando aspectos como aroma, sabor, acidez e equilíbrio. Embora esse processo seja relevante, ele pode ser subjetivo, custoso e pouco escalável.

Dessa forma, o projeto busca apoiar a tomada de decisão de produtores, enólogos e áreas de negócio por meio de uma abordagem analítica, transformando dados químicos em uma classificação objetiva de qualidade.

A variável original `quality` foi transformada em um problema de classificação binária:

* `1` — Alta Qualidade: vinhos com nota maior ou igual a 7;
* `0` — Baixa ou Média Qualidade: vinhos com nota menor que 7.

---

## Objetivo do Trabalho

Construir um pipeline completo de análise e modelagem preditiva para:

* compreender o comportamento das variáveis físico-químicas dos vinhos;
* realizar análise exploratória dos dados;
* transformar a variável de qualidade em uma variável binária;
* treinar e comparar modelos de classificação;
* avaliar o desempenho dos modelos com métricas adequadas;
* interpretar os principais fatores que influenciam a qualidade do vinho;
* apresentar conclusões e recomendações práticas com base nos resultados.

---

## 📈 Sobre o Dataset 

O projeto utiliza o **Wine Quality Dataset**, disponível no Kaggle, contendo informações físico-químicas de vinhos e suas respectivas notas de qualidade.

Dataset utilizado:

[Wine Quality Dataset — Kaggle](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)

O principal arquivo utilizado no notebook é:

```text
WineQT.csv
```

A base contém uma amostra de vinhos tintos portugueses do tipo **Vinho Verde**, com variáveis laboratoriais e a nota de qualidade atribuída por especialistas.

---

## 🔎 Estrutura dos Dados

| Coluna                 | Descrição                                                      |
| ---------------------- | -------------------------------------------------------------- |
| `fixed acidity`        | Acidez fixa do vinho                                           |
| `volatile acidity`     | Acidez volátil, associada a defeitos sensoriais quando elevada |
| `citric acid`          | Ácido cítrico, relacionado ao frescor e equilíbrio             |
| `residual sugar`       | Açúcar residual após fermentação                               |
| `chlorides`            | Concentração de cloretos                                       |
| `free sulfur dioxide`  | Dióxido de enxofre livre                                       |
| `total sulfur dioxide` | Dióxido de enxofre total                                       |
| `density`              | Densidade do vinho                                             |
| `pH`                   | Nível de acidez/basicidade                                     |
| `sulphates`            | Sulfatos, associados à conservação do vinho                    |
| `alcohol`              | Teor alcoólico                                                 |
| `quality`              | Nota de qualidade original                                     |
| `Id`                   | Identificador do registro                                      |

---

## Arquivos do Projeto

O projeto segue a seguinte estrutura:

```text
tech-challenge-2-wine-quality/
├── data/
│   └── WineQT.csv
│
├── notebooks/
│   └── Wine_Quality_Classif_TechChallenge2.ipynb
│
├── results/
│   ├── 01_distribuicao_target.png
│   ├── 02_distribuicoes_features.png
│   ├── 03_boxplots_por_classe.png
│   ├── 04_matriz_correlacao.png
│   ├── 05_comparacao_modelos_auc.png
│   ├── 06_matrizes_confusao.png
│   ├── 07_curvas_roc.png
│   ├── 08_features_importance.png
│   ├── 09_coeficientes_logistica.png
│   ├── 10_arvore_decisao.png
│   ├── 11_fronteiras_decisao.png
│   ├── 12_curva_precisao_recall.png
│   ├── 13_shap_summary.png
│   └── 14_shap_waterfall.png
|
├── src/
│
└── README.md
└── requirements.txt
└── Apresentacao_TechChallenge2.pdf
└── Relatorio_Executivo_TechChallenge_Fase 2.pdf
└── Video_Apresentacao_Executiva.txt

```

---

## 📥 Como Reproduzir a Análise

### 1. Baixar o dataset

Baixe o dataset no Kaggle:

🔗 [Wine Quality Dataset — Kaggle](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)

Após o download, extraia os arquivos CSV e salve-os na pasta `data/`.

O arquivo principal esperado para execução do notebook é:

```text
data/WineQT.csv
```

---

### 2. Instalar as bibliotecas necessárias

As principais bibliotecas utilizadas no projeto são:

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

Caso necessário, instale-as com:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

### 3. Executar o notebook

Abra o notebook no Google Colab, Jupyter Notebook ou JupyterLab:

```bash
jupyter notebook notebook/wine_quality_classification.ipynb
```

Execute as células sequencialmente para reproduzir:

* carregamento dos dados;
* auditoria de qualidade;
* análise exploratória;
* transformação da variável alvo;
* pré-processamento;
* treinamento dos modelos;
* avaliação dos resultados;
* interpretação das variáveis mais relevantes;
* conclusão do projeto.

---

## Metodologia

O desenvolvimento do projeto foi dividido nas seguintes etapas:

### 1. Compreensão do Problema

O problema foi tratado como uma classificação binária, em que o objetivo é identificar se um vinho pode ser considerado de alta qualidade com base em suas características físico-químicas.

### 2. Auditoria e Qualidade dos Dados

Foi realizada uma análise inicial para verificar:

* tipos das variáveis;
* quantidade de registros;
* presença de valores nulos;
* quantidade de valores únicos;
* existência de linhas duplicadas;
* distribuição da variável alvo.

O dataset não apresentou valores nulos. As linhas duplicadas foram mantidas, pois em dados físico-químicos é possível que vinhos diferentes apresentem medições idênticas ou muito semelhantes.

### 3. Análise Exploratória dos Dados

Foram analisadas as distribuições das variáveis numéricas, a relação entre cada variável e a qualidade do vinho, além da matriz de correlação.

As principais variáveis associadas à qualidade foram:

* `alcohol`;
* `volatile acidity`;
* `sulphates`;
* `citric acid`;
* `density`.

### 4. Transformação da Variável Alvo

A variável `quality`, originalmente representada por notas, foi convertida em uma variável binária chamada `high_quality`:

```python
quality >= 7 -> 1
quality < 7  -> 0
```

Essa transformação permitiu tratar o desafio como um problema de classificação supervisionada.

### 5. Pré-processamento

Foram aplicadas técnicas como:

* separação entre variáveis explicativas e variável alvo;
* divisão entre treino e teste;
* estratificação da amostra;
* padronização das variáveis numéricas;
* criação de variáveis derivadas;
* uso de pipelines do Scikit-learn.

### 6. Modelagem

Foram treinados e comparados quatro modelos de classificação:

1. Regressão Logística;
2. KNN;
3. SVM com kernel RBF;
4. Random Forest.

Também foi aplicada validação cruzada estratificada e ajuste de hiperparâmetros com `GridSearchCV`.

### 7. Avaliação dos Modelos

Como a base apresenta desbalanceamento entre as classes, a avaliação não se limitou à acurácia.

Foram utilizadas métricas como:

* Accuracy;
* Precision;
* Recall;
* F1-Score;
* ROC-AUC;
* matriz de confusão;
* curva ROC.

---

## 📊 Principais Resultados

O projeto identificou que o dataset possui desbalanceamento de classes, com uma proporção menor de vinhos classificados como alta qualidade.

Entre os modelos testados, o **Random Forest ajustado** apresentou o melhor desempenho geral no conjunto de teste, combinando boa acurácia, precisão, F1-Score e ROC-AUC.

O **SVM** apresentou maior capacidade de identificar vinhos de alta qualidade, com maior Recall, porém com maior quantidade de falsos positivos.

Dessa forma, a escolha do melhor modelo depende do objetivo de negócio:

* se o foco for evitar classificar vinhos comuns como premium, o Random Forest é mais indicado;
* se o foco for identificar o maior número possível de vinhos potencialmente bons, o SVM pode ser mais adequado.

---

## 📊 Principais Insights

* Vinhos com maior teor alcoólico tendem a apresentar maior probabilidade de alta qualidade.
* A acidez volátil elevada está negativamente relacionada à qualidade, pois pode indicar defeitos sensoriais.
* Sulfatos aparecem como variável relevante, associados à conservação e estabilidade do vinho.
* A combinação entre alto teor alcoólico e baixa acidez volátil é um forte indicativo de qualidade.
* A acurácia isolada não é suficiente para avaliar o modelo, devido ao desbalanceamento da variável alvo.
* Modelos de árvore, como Random Forest, são úteis por combinarem bom desempenho preditivo e interpretação das variáveis mais importantes.

---

## Conclusão

O trabalho desenvolveu um pipeline completo de Machine Learning para classificação da qualidade de vinhos a partir de variáveis físico-químicas.

A abordagem mostrou que é possível utilizar dados laboratoriais para apoiar a triagem e avaliação da qualidade dos vinhos, reduzindo subjetividade e auxiliando especialistas na tomada de decisão.

O modelo final apresentou bom desempenho geral, com destaque para o Random Forest, e indicou que variáveis como teor alcoólico, acidez volátil e sulfatos são determinantes para a classificação da qualidade.

Como próximos passos, recomenda-se:

* testar modelos de boosting, como XGBoost e LightGBM;
* avaliar técnicas de balanceamento, como SMOTE;
* validar o modelo com novas safras;
* expandir a análise para vinhos brancos e base combinada;
* desenvolver uma aplicação simples para classificação de novos vinhos.

---

## 📌 Entregáveis

* Notebook completo, comentado e organizado;
* Análise exploratória dos dados;
* Pipeline de pré-processamento;
* Treinamento e comparação de modelos;
* Avaliação com métricas de classificação;
* Interpretação dos resultados;
* Relatório executivo;
* Apresentação final do Tech Challenge. [Link no YouTube](https://youtu.be/EZjwfVLmtfw)
  
---

## 🧑‍💻 Tecnologias Utilizadas

* Python;
* Pandas;
* NumPy;
* Matplotlib;
* Seaborn;
* Scikit-learn;
* Jupyter Notebook.

---

## 📚 Referências

* Wine Quality Dataset — Kaggle.
* Cortez, P.; Cerdeira, A.; Almeida, F.; Matos, T.; Reis, J. Modeling wine preferences by data mining from physicochemical properties.
* Documentação oficial do Scikit-learn.
* Materiais da Pós Tech FIAP — Data Analytics.

---

## 👥 Integrantes do Grupo

| Nome                             | RM     |
| -------------------------------- | ------ |
| Emerson Henrique de Lima e Sousa | 373751 |
| Moacyr Souza Barros              | 373412 |
