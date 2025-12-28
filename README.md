# Probabilidade de Sobrevivência no Titanic

Este projeto utiliza algoritmos de Machine Learning para prever a probabilidade de sobrevivência de passageiros do Titanic, baseando-se no famoso dataset do Kaggle.

## 📋 Sobre o Projeto

O objetivo é criar um modelo capaz de classificar se um passageiro sobreviveria ou não ao naufrágio, com base em características como classe, sexo, idade, tarifa, local de embarque, entre outros.

O projeto foi desenvolvido em um Jupyter Notebook e aborda as seguintes etapas principais:

1.  **Limpeza de Dados**: 
    - Remoção de colunas com baixa relevância ou muitos dados faltantes (`Name`, `Cabin`, `PassengerId`, `Ticket` bruto).
    - Tratamento de valores nulos em `Age`, `Embarked` e `Fare` (substituição pela mediana ou moda).
2.  **Engenharia de Atributos (Feature Engineering)**:
    - *Frequency Encoding* para a coluna `Ticket`.
    - *One-Hot Encoding* para variáveis categóricas como `Sex` e `Embarked`.
3.  **Modelagem**: Treinamento e avaliação de diversos algoritmos de classificação:
    - Regressão Logística (Logistic Regression)
    - Árvore de Decisão (Decision Tree Classifier)
    - K-Nearest Neighbors (KNN)
    - Random Forest Classifier
4.  **Avaliação**: Comparação da acurácia dos modelos utilizando um conjunto de dados de teste validado com o gabarito (`gender_submission.csv`).

## 🚀 Como Executar

### Pré-requisitos
Certifique-se de ter o Python instalado (versão 3.x recomendada). As principais bibliotecas utilizadas são:

- `pandas`
- `scikit-learn` (sklearn)
- `jupyter` (para rodar o notebook)

Você pode instalar as dependências via pip:

```bash
pip install pandas scikit-learn notebook
```

### Base de Dados
O projeto espera que os arquivos de dados estejam no mesmo diretório do notebook. Os arquivos originais podem ser obtidos na competição do Kaggle: [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic/data).

Arquivos utilizados no código:
- `train (1).csv` (Base de treino)
- `test.csv` (Base de teste)
- `gender_submission.csv` (Gabarito para validação)

### Executando
1. Clone este repositório ou baixe os arquivos.
2. Abra o terminal na pasta do projeto.
3. Inicie o Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Abra o arquivo `titanic.ipynb` e execute as células sequencialmente.

## 📊 Resultados

Após o treinamento e teste dos modelos, os seguintes resultados de acurácia foram obtidos:

| Modelo | Acurácia Aproximada |
| :--- | :--- |
| **Regressão Logística** | **93.54%** |
| Random Forest | 86.12% |
| KNN | 85.40% |
| Árvore de Decisão | 77.51% |

O modelo de **Regressão Logística** apresentou o melhor desempenho para este conjunto de dados e pré-processamento realizado.