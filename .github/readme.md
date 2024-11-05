# EducEco - Projeto de Análise e Implementação de Modelos de IA

Este repositório contém o desenvolvimento de um projeto de IA para o EducEco, um aplicativo de aprendizado em sustentabilidade. O projeto explora quatro modelos de inteligência artificial, com análises comparativas e a escolha do modelo mais adequado para serialização e futura implementação no aplicativo.

## Estrutura do Repositório

- **analise.ipynb**: Este notebook contém análises e avaliações de quatro modelos de IA:
  - **Naive Bayes** - Implementado com o GaussianNB
  - **Árvore de Decisão** - Critério Gini
  - **Árvore de Decisão** - Critério Entropia
  - **K-Nearest Neighbors (KNN)** - Algoritmo de vizinhos mais próximos

- **analiseOficial.ipynb**: Este notebook contém a análise final e a serialização do modelo de IA escolhido, pronto para ser implementado no EducEco.

- **EducEco.xlsx**: Base de dados utilizada para treinamento e avaliação dos modelos.

- **Arquivos .pkl**: Arquivos com o modelo serializado, resultado do processo de seleção de modelos para uso no aplicativo:
  - O primeiro arquivo `.pkl` contém o modelo treinado.
  - O segundo arquivo `.pkl` contém o pipeline de preprocessamento e o modelo completo para a previsão.

## Requisitos

Para executar os notebooks, instale os seguintes pacotes (você pode instalá-los com o comando `pip install -r requirements.txt`):

- `pandas`
- `scikit-learn`
- `numpy`
- `imblearn`
- `matplotlib`
- `seaborn`
- `pickle`

## Como Executar

1. **Abra o `analise.ipynb`** para entender as análises comparativas dos quatro modelos e suas métricas. As métricas principais incluem acurácia, precisão, recall e F1-score para determinar o desempenho de cada modelo.
  
2. **Abra o `analiseOficial.ipynb`** para ver a análise completa do modelo escolhido e o processo de serialização. Este notebook fornece a análise da IA final, além do processo de serialização para exportação e uso futuro no EducEco.

## Implementação

O modelo serializado, pronto para ser carregado no EducEco, é encontrado nos arquivos `.pkl`. Para carregar o modelo e utilizá-lo, siga o exemplo de código abaixo:

```python
import pickle

# Carregar o modelo serializado
with open("modelo_escolhido.pkl", "rb") as file:
    modelo = pickle.load(file)

# Fazer previsões
# Exemplo: previsao = modelo.predict(X_novo)
