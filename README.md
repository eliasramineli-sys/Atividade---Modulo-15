Atividade referente ao módulo 15 do curso de cientista de dados da EBAC

````md
 📊 Atividade MOD15 – Tratamento e Análise de Dados com Python

Projeto desenvolvido utilizando Python e Jupyter Notebook para realizar etapas fundamentais do processo de análise e preparação de dados, aplicando técnicas de limpeza, tratamento e exploração dos dados.

---

🚀 Objetivo

O objetivo desta atividade foi aplicar conceitos de pré-processamento e análise de dados para transformar informações brutas em dados mais organizados, consistentes e preparados para análises futuras e modelos de Machine Learning.

---
 🛠 Tecnologias utilizadas

- Python 3
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Plotly
- Scikit-Learn

---

📂 Etapas desenvolvidas

1️⃣ Importação dos dados
Leitura do arquivo CSV utilizando a biblioteca Pandas.

Exemplo:

```python
import pandas as pd

df = pd.read_csv(
    r"C:\Users\ELIAS\Downloads\arquivo.csv",
    delimiter=';'
)
```

---

2️⃣ Exploração inicial

Foram realizadas verificações iniciais:

- Visualização das primeiras linhas
- Tipos de dados
- Valores nulos
- Estatísticas gerais
- Estrutura do DataFrame

Exemplos:

```python
df.head()

df.info()

df.describe()

df.isnull().sum()
```

---

3️⃣ Tratamento dos dados

Aplicações realizadas:

✔ Remoção de registros duplicados

```python
df = df.drop_duplicates()
```

✔ Correção de valores ausentes

```python
df['coluna'] = df['coluna'].fillna(
    df['coluna'].median()
)
```

✔ Padronização de textos

```python
for coluna in df.select_dtypes(include='object'):
    
    df[coluna] = (
        df[coluna]
        .str.strip()
        .str.lower()
    )
```

✔ Conversão de tipos

```python
df['coluna'] = pd.to_numeric(
    df['coluna'],
    errors='coerce'
)
```

---

 4️⃣ Estatísticas descritivas

Análises realizadas:

- Média
- Mediana
- Moda
- Desvio padrão
- Quartis
- Distribuição dos dados

Exemplo:

```python
df.describe()
```

---

5️⃣ Análise de Outliers

Identificação de possíveis valores discrepantes utilizando gráficos.

Exemplo:

```python
import matplotlib.pyplot as plt

plt.boxplot(df['coluna'])
plt.show()
```

---

6️⃣ Análise Univariada e Bivariada

Foram exploradas relações entre variáveis através de:

- Histogramas
- Boxplots
- Correlação
- Gráficos de dispersão

---

📈 Resultados

Após o tratamento:

✔ Dados limpos  
✔ Valores inconsistentes corrigidos  
✔ Estrutura preparada para análise  
✔ Base pronta para futuras aplicações de Machine Learning

---

🎯 Aprendizados

Durante a atividade foram praticados conceitos importantes:

- Manipulação de DataFrames
- Limpeza de dados
- Tratamento de valores nulos
- Padronização
- Estatísticas descritivas
- Visualização de dados
- Pré-processamento

---

 Como executar

Clone este repositório:

```bash
git clone LINK_DO_REPOSITORIO
```

Instale as dependências:

```bash
pip install pandas numpy matplotlib plotly scikit-learn
```

Abra o Jupyter Notebook:

```bash
jupyter notebook
```








