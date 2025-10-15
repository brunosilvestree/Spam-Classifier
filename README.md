# Classificação de SMS: Spam vs Ham

Este projeto implementa um modelo de **aprendizado de máquina supervisionado (ML)** para classificar mensagens SMS como **spam** (indesejadas) ou **ham** (legítimas).  
O modelo foi treinado utilizando o clássico dataset [SMS Spam Collection (Kaggle)](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset?select=spam.csv).

---

## Objetivo

Demonstrar um pipeline completo de *Machine Learning aplicado a Processamento de Linguagem Natural (NLP)*:

1. Leitura e exploração dos dados  
2. Limpeza e pré-processamento textual  
3. Vetorização com TF-IDF  
4. Treinamento e avaliação de modelos de classificação  
5. Visualização e análise de resultados

---

## Estrutura do Projeto

```
Spam-Classifier/
│
├── data/
│   └── spam.csv
│
├── notebooks/
│   └── Spam.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Tecnologias Utilizadas

- **Python 3.10+**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn**
- **NLTK** (Natural Language Toolkit)

---

## Etapas do Projeto

### 1. Leitura e limpeza de dados
- Carrega o dataset `spam.csv`  
- Renomeia colunas para `label` e `message`  
- Substitui rótulos `ham → 0` e `spam → 1`

### 2. Pré-processamento de texto
- Conversão para minúsculas  
- Remoção de pontuações e stopwords  
- Tokenização e limpeza com regex (`re`)  

### 3. Vetorização
- Conversão de texto em vetores numéricos com **TF-IDF**  
- Separação em **dados de treino e teste (80/20)**

### 4. Treinamento
- Modelo base: **Multinomial Naive Bayes**  
- Avaliação com métricas de classificação

### 5. Avaliação e resultados
- Exibição da **matriz de confusão**  
- Cálculo de **acurácia, precisão, recall e F1-score**  
- Visualizações com Seaborn e Matplotlib  

---

## Resultados

O modelo apresentou **alta acurácia (~96%)**, com excelente equilíbrio entre *precision* e *recall*, demonstrando eficácia na detecção de mensagens de spam sem penalizar falsos positivos em excesso.

---

## Como Executar Localmente

1. Clone este repositório:
```bash
git clone https://github.com/seuusuario/spam-classifier.git
cd spam-classifier
```

2. Crie um ambiente virtual:
```bash
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scripts\activate     # Windows
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

4. Execute o notebook:
```bash
jupyter notebook notebooks/Spam.ipynb
```