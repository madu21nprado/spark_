
# 💡 Projeto: Análise de Dados com Azure Databricks & Spark

**Autor(a): Maria Eduarda Prado**

## 📘 Descrição

Este projeto foi desenvolvido como parte dos desafios práticos da DIO, com o objetivo de aplicar os conhecimentos adquiridos sobre o uso do **Azure Databricks** e o **Apache Spark** em análises de dados.

Utilizamos a plataforma de nuvem para criar um ambiente escalável, processar dados com PySpark e extrair insights relevantes a partir de um dataset simulado de vendas.

---

## 🔧 Tecnologias e Ferramentas

- Microsoft Azure
- Azure Databricks
- Apache Spark
- PySpark
- Python
- Git & GitHub

---

## 🚀 Etapas Desenvolvidas

### ✅ 1. Criação do Workspace e Cluster no Azure Databricks

O primeiro passo foi a criação de um workspace Databricks e de um cluster com configuração padrão para executar notebooks PySpark.

*Exemplo de configuração:*
- Runtime: 11.3 LTS (Apache Spark 3.3.0)
- Worker Nodes: Standard_DS3_v2
-

### ✅ 2. Leitura e Visualização do Dataset

O dataset (`vendas.csv`) foi carregado no Databricks FileStore e lido com o PySpark.

```python
df = spark.read.csv("/FileStore/tables/vendas.csv", header=True, inferSchema=True)
df.show(5)
```

---

### ✅ 3. Tratamento e Análise dos Dados

- Remoção de valores nulos
- Conversão de tipos de dados
- Agregações por região, categoria e data
- Ordenações e filtros por métricas

```python
df_clean = df.dropna()
df_clean.groupBy("regiao").agg({"valor": "sum"}).show()


## 📊 Insights Obtidos

- As regiões **Sudeste** e **Sul** apresentaram os maiores volumes de vendas.
- A maior parte das transações ocorreu nos meses de novembro e dezembro.
- A categoria **Eletrônicos** teve o maior ticket médio.

---

## 💭 Possibilidades Futuras

- Aplicar Machine Learning com **Spark MLlib** para prever vendas
- Criar um dashboard integrado com Power BI
- Automatizar pipeline com Azure Data Factory

---

## 🧠 O que eu aprendi

- Criar e configurar ambientes escaláveis no Azure
- Escrever consultas e transformações com **PySpark**
- Analisar grandes volumes de dados de forma distribuída
- Organizar um projeto completo com Git e GitHub



**Maria Eduarda Prado** ✨  
