# Diagnóstico de Diabetes com Machine Learning

Este projeto foi desenvolvido como parte do **Tech Challenge – Fase 1**, cujo objetivo é criar uma solução inicial baseada em Inteligência Artificial para **suporte ao diagnóstico médico**.  
Utilizamos o dataset público **Pima Indians Diabetes Dataset** para construir e avaliar modelos de classificação capazes de prever a presença de diabetes a partir de dados clínicos.

| O **relatório técnico** está no próprio notebook disponível em `notebooks/diabetes.ipynb`

## Descrição
O sistema realiza:
- **Exploração de dados**: estatísticas descritivas e visualizações para entender o dataset.
- **Pré-processamento**: tratamento de valores ausentes, normalização e codificação.
- **Modelagem**: aplicação de algoritmos como Regressão Logística, Árvore de Decisão, KNN e modelos de gradient boosting.
- **Avaliação**: métricas como *accuracy*, *precision*, *recall* e *F1-score*, priorizando a redução de falsos negativos.
- **Interpretabilidade**: uso de *feature importance* e SHAP para explicar as previsões.


##  Estrutura do Repositório
```plaintext
.
├── data/
│   └── pimas_indian_diabetes.csv   # Snapshot do dataset
├── notebooks/
│   └── diabetes.ipynb              # Notebook principal com todo o fluxo do projeto
├── reports/
│   └── relatorio.html              # Relatório em página web
│   └── relatorio.pdf               # Relatório em PDF
├── requirements.txt                # Dependências necessárias
└── README.md                  
```


## Dataset

**Pima Indians Diabetes Database**
📌 Disponível no [Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database/)

O dataset contém variáveis como número de gestações, glicose, pressão arterial, espessura da pele, insulina, índice de massa corporal, idade, entre outras.

Na pasta `data` há uma cópia do dataset, mas no código nós buscamos direto do Kaggle.

## 🛠 Tecnologias Utilizadas

* **Linguagem:** Python 3.10+
* **Manipulação de dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn, Plotly
* **Machine Learning:** Scikit-learn, XGBoost, LightGBM, CatBoost
* **Interpretabilidade:** SHAP, LIME
* **Ambiente:** Jupyter Notebook


## Como Rodar o Projeto

### Via Google Colab (recomendado)
- Faça download do arquivo `diabetes.ipynb` na área de releases;
- Faça upload no Google Drive;
- Abra com o Google Colab e rode;

### Localmente
#### Clonar o repositório
```bash
git clone https://github.com/usuario/diagnostico-diabetes.git
cd ia-tch001
```

#### Criar e ativar um ambiente virtual

```bash
python -m venv .venv

# Ativar no Windows
.\.venv\Scripts\activate

# Ativar no Linux/macOS
source .venv/bin/activate
```

#### Instalar as dependências

```bash
pip install -r requirements_full.txt
```

#### Executar o notebook

```bash
jupyter notebook diabetes.ipynb
```

## Resultados Obtidos

* **Melhor modelo:** `SGD-Log` e `Guassian NB` apresentaram equilíbrio entre *Recall* e *Precision*;
* **Principais variáveis:** Glicose, IMC e histórico de gestações foram os fatores mais relevantes para a previsão;
* **Desempenho médio:** *Accuracy* acima de **75%**, com *Recall* otimizado para reduzir falsos negativos;

## Limitações

* Dataset pequeno e restrito a uma única população;
* Ausência de variáveis clínicas complementares;
* Possível desbalanceamento entre classes;

## Trabalhos Futuros

* Expandir o dataset com dados de diferentes populações;
* Incluir variáveis laboratoriais adicionais;
* Aplicar *Ensemble Learning* e redes neurais;
* Integrar dados de imagem (ex.: exames de retina);
* Testar o sistema em ambiente real com supervisão médica;

## Pessoa autora
- Ricarth Lima
- Projeto desenvolvido para o **Tech Challenge - IA para Devs – Fase 1**.
