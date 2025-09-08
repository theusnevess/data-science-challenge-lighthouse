# Desafio de Ciência de Dados - Lighthouse

Este repositório contém o projeto desenvolvido para o desafio de Ciência de Dados da Lighthouse, focado na análise e predição de notas de filmes do IMDb.

## Estrutura do Projeto

O projeto está organizado nas seguintes pastas:

- `Data/`: Contém o dataset original utilizado no projeto (`desafio_indicium_imdb.csv`).
- `Models/`: Armazena o modelo de machine learning treinado e salvo no formato `.pkl` (`modelo_imdb.pkl`).
- `Notebooks/`: Inclui o Jupyter Notebook (`desafio-indicium.ipynb`) com toda a análise exploratória de dados (EDA), pré-processamento, modelagem e avaliação do modelo.

## Requisitos

Para executar este projeto, você precisará das seguintes bibliotecas Python. Elas estão listadas no arquivo `requirements.txt`:

```
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

## Instalação

Siga os passos abaixo para configurar o ambiente e instalar as dependências:

1.  **Clone o repositório:**

    ```bash
    git clone https://github.com/theusnevess/data-science-challenge-lighthouse.git
    cd data-science-challenge-lighthouse
    ```

2.  **Crie e ative um ambiente virtual (recomendado):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows, use `venv\Scripts\activate`
    ```

3.  **Instale as dependências:**

    ```bash
    pip install -r requirements.txt
    ```

## Como Executar o Projeto

Após a instalação das dependências, você pode executar o Jupyter Notebook para reproduzir a análise e a modelagem:

1.  **Inicie o Jupyter Notebook:**

    ```bash
    jupyter notebook
    ```

2.  No navegador, navegue até a pasta `Notebooks/` e abra o arquivo `desafio-indicium.ipynb`.

3.  Execute todas as células do notebook para ver a análise de dados, o treinamento do modelo e as predições.

## Relatórios e Análises

Os relatórios das análises estatísticas e EDA (Análise Exploratória de Dados) estão disponíveis nos seguintes formatos:

-   **Jupyter Notebook:** `Notebooks/desafio-indicium.ipynb` (contém todo o código e as visualizações).
-   **PDF:** `Notebooks/desafio-indicium.pdf` (uma versão em PDF do notebook para fácil visualização).

## Modelagem

O código de modelagem utilizado no passo 3 do desafio está contido no Jupyter Notebook `Notebooks/desafio-indicium.ipynb`. Ele inclui:

-   Pré-processamento e limpeza dos dados.
-   Divisão dos dados em conjuntos de treino e teste.
-   Treinamento de um modelo de Regressão Linear para prever a nota do IMDb.
-   Avaliação do modelo com métricas como MAE, MSE, RMSE e R2.

## Modelo Salvo

O modelo de previsão treinado está salvo no arquivo `Models/modelo_imdb.pkl`. Este arquivo pode ser carregado para fazer novas predições sem a necessidade de retreinar o modelo.

```python
import joblib

# Carregar o modelo
modelo_carregado = joblib.load('Models/modelo_imdb.pkl')

# Exemplo de uso (assumindo que 'X_novo_filme' é o dataframe com as features do novo filme)
# previsao = modelo_carregado.predict(X_novo_filme)
# print(f'Nota IMDb prevista: {previsao[0]:.2f}')
```

---