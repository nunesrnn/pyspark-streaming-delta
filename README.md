# 🚀 PySpark Streaming com Delta Lake

Pipeline de processamento de dados em tempo real utilizando **PySpark Structured Streaming** e **Delta Lake**, seguindo a arquitetura em camadas **Bronze → Silver → Gold**.

---

## 📖 Sobre o Projeto

Este projeto simula um ambiente moderno de Engenharia de Dados capaz de receber eventos continuamente, processá-los em tempo real e disponibilizar dados confiáveis para análise.

O objetivo é demonstrar conhecimentos em:

- PySpark
- Structured Streaming
- Delta Lake
- Data Lakehouse
- ETL em tempo real
- Arquitetura Medallion (Bronze, Silver e Gold)

---

## 🏗️ Arquitetura

```text
           Fonte de Dados
                  │
                  ▼
        ┌─────────────────┐
        │     Bronze      │
        │ Dados Brutos    │
        └─────────────────┘
                  │
                  ▼
        ┌─────────────────┐
        │     Silver      │
        │ Dados Tratados  │
        └─────────────────┘
                  │
                  ▼
        ┌─────────────────┐
        │      Gold       │
        │ Dados de Negócio│
        └─────────────────┘
                  │
                  ▼
           Dashboards
           e Analytics
```

---

## 🥉 Camada Bronze

Responsável pela ingestão dos dados sem transformações relevantes.

Exemplos:

- Captura de eventos em tempo real
- Armazenamento bruto
- Preservação do histórico original

---

## 🥈 Camada Silver

Responsável pela qualidade dos dados.

Transformações:

- Remoção de registros inválidos
- Tratamento de valores nulos
- Conversão de tipos
- Padronização de colunas
- Deduplicação

---

## 🥇 Camada Gold

Responsável pelas regras de negócio e consumo analítico.

Exemplos:

- Faturamento diário
- Indicadores operacionais
- Métricas consolidadas
- Visões para BI

---

## 🛠️ Tecnologias Utilizadas

- Python 3.x
- Apache Spark
- PySpark Structured Streaming
- Delta Lake
- Git
- GitHub

---

## 📂 Estrutura do Projeto

```text
pyspark-streaming-delta/
│
├── data/
│
├── src/
│   ├── bronze.py
│   ├── silver.py
│   └── gold.py
│
├── notebooks/
│   ├── bronze.ipynb
│   ├── silver.ipynb
│   └── gold.ipynb
│
├── requirements.txt
│
└── README.md
```

---

## ⚙️ Instalação

Clone o repositório:

```bash
git clone https://github.com/nunesrnn/pyspark-streaming-delta.git
```

Entre na pasta:

```bash
cd pyspark-streaming-delta
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

---

## 📦 Dependências

```txt
pyspark
delta-spark
```

---

## ▶️ Fluxo de Execução

1. Receber dados em streaming.
2. Armazenar os dados na camada Bronze.
3. Aplicar limpeza e padronização na camada Silver.
4. Gerar agregações de negócio na camada Gold.
5. Disponibilizar os dados para consumo analítico.

---

## 🎯 Objetivos de Aprendizado

- Trabalhar com processamento em tempo real.
- Implementar pipelines utilizando PySpark.
- Utilizar tabelas Delta Lake.
- Aplicar arquitetura Medallion.
- Simular cenários reais de Engenharia de Dados.

---

## 📈 Melhorias Futuras

- [ ] Dockerização
- [ ] Deploy em Databricks
- [ ] Integração com Kafka
- [ ] Criação de dashboard Power BI
- [ ] Testes automatizados
- [ ] Monitoramento do pipeline

---

## 👨‍💻 Autor

**Renan Luis Trindade Nunes**

Estudante e Estagiário de Engenharia de Dados, com foco em PySpark, Databricks e Delta Lake.
