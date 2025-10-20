# Análise Exploratória de Dados - Netflix Daily Top 10

## 📊 Sobre o Projeto

Este projeto realiza uma análise exploratória de dados (EDA) sobre o ranking diário do Top 10 da Netflix. O objetivo é compreender padrões de visualização, identificar outliers e explorar características dos conteúdos mais populares da plataforma.

## 📁 Estrutura do Projeto

```
analise-netflix/
│
├── dataset/
│   └── netflix_daily_top_10.csv    # Dataset com dados diários do Top 10
│
├── eda_netflix.ipynb                # Notebook principal com análises
├── Pipfile                          # Gerenciamento de dependências
├── Pipfile.lock                     # Lock de versões das dependências
└── README.md                        # Este arquivo
```

## 📋 Dataset

O dataset `netflix_daily_top_10.csv` contém informações sobre os conteúdos que figuraram no Top 10 diário da Netflix, incluindo:

- **As of**: Data do registro
- **Rank**: Posição no ranking diário
- **Year to Date Rank**: Posição acumulada no ano
- **Last Week Rank**: Posição na semana anterior
- **Title**: Título do conteúdo
- **Type**: Tipo (TV Show, Movie, Stand-Up Comedy)
- **Netflix Exclusive**: Se é exclusivo da Netflix
- **Netflix Release Date**: Data de lançamento na plataforma
- **Days In Top 10**: Dias consecutivos no Top 10
- **Viewership Score**: Score de visualização

## 🔍 Análises Realizadas

### 1. Exploração Inicial dos Dados
- Visualização dos primeiros e últimos registros
- Análise da estrutura e tipos de dados
- Verificação do período coberto pelos dados

### 2. Qualidade dos Dados
- Detecção de valores ausentes
- Análise de valores únicos em colunas categóricas
- Tratamento de dados faltantes

### 3. Transformação de Dados
- Conversão da coluna de data para o tipo datetime
- Preparação dos dados para análises temporais

### 4. Análise de Outliers
- **Visualização com Box Plot**: Identificação visual de outliers no Viewership Score
- **Análise de Distribuição**: Histograma para verificar normalidade dos dados
- **Método de Tukey (IQR)**: Detecção estatística de outliers usando o Range Interquartil
  - Cálculo do IQR (Q3 - Q1)
  - Definição de limites inferior e superior (Q1 - 1.5×IQR e Q3 + 1.5×IQR)
  - Identificação de valores fora dos limites estabelecidos

## 🛠️ Tecnologias Utilizadas

- **Python 3.9+**
- **Pandas**: Manipulação e análise de dados
- **Jupyter Notebook**: Ambiente de desenvolvimento interativo
- **Matplotlib**: Visualização de dados (através do pandas.plot)

## 🚀 Como Executar

### Pré-requisitos

- Python 3.9 ou superior
- Pipenv (recomendado) ou pip

### Instalação com Pipenv

```bash
# Instalar pipenv (se ainda não tiver)
pip install pipenv

# Instalar dependências
pipenv install

# Ativar ambiente virtual
pipenv shell

# Executar Jupyter Notebook
jupyter notebook eda_netflix.ipynb
```

### Instalação com pip

```bash
# Instalar pandas
pip install pandas

# Executar Jupyter Notebook
jupyter notebook eda_netflix.ipynb
```

## 📈 Principais Insights

O notebook revela informações importantes sobre:

- Padrões de permanência de conteúdos no Top 10
- Distribuição de scores de visualização
- Identificação de conteúdos com desempenho excepcional (outliers positivos)
- Características dos conteúdos exclusivos vs. não-exclusivos da Netflix

## 📝 Notas

- O dataset começa em abril de 2020
- A análise utiliza o método de Tukey para detecção de outliers, apropriado para distribuições não-normais
- Os dados refletem o comportamento de visualização durante o período coberto pelo dataset

## 👨‍💻 Autor

Daniela Medeiros

## 📄 Licença

Este projeto é de código aberto e está disponível para fins educacionais.

---

**Observação**: Este é um projeto de estudos para prática de análise exploratória de dados com Python e Pandas.

