
# 📊 Case Técnico de Data Analytics – iFood

Este repositório apresenta a solução desenvolvida para o **Case Técnico de Data Analytics do iFood**, com foco na **análise de uma campanha de cupons promocionais** e na **segmentação de clientes via metodologia RFM**. O projeto visa responder às questões de negócio propostas, com embasamento estatístico, modelagem analítica e recomendações estratégicas.

## 🗂️ Estrutura do Repositório

```
.
├── notebooks/
│   ├── etl_process.ipynb                  # ETL dos dados originais para o BigQuery
│   ├── exploratory_data_analysis.ipynb    # Análise exploratória, segmentações e métricas
│   └── ifood_abtest_segmentation_results.ipynb  # Resultados do Teste A/B e análise segmentada
├── reports/
│   └── relatorio_executivo.pdf           # Relatório final com conclusões de negócio
├── data/                                  # (opcional) Arquivos de dados baixados localmente
└── README.md                              # Este arquivo
```

## 🚀 Objetivos do Projeto

- Avaliar o impacto de uma campanha de cupons utilizando Teste A/B.
- Medir retorno financeiro (ROI), retenção e ticket médio.
- Propor estratégias segmentadas de cupons com base em perfis de clientes.
- Recomendar melhorias baseadas em análises preditivas e RFM.

## 🛠️ Tecnologias Utilizadas

- **Python 3.10+**
- **Google BigQuery** (armazenamento e consultas SQL)
- **Jupyter Notebook** (ambiente analítico)
- **Pandas, Numpy, Seaborn, Scikit-learn, Scipy** (bibliotecas de análise)
- **Google Colab** (execução remota e gratuita)

## ⚠️ Requisitos para Execução

Antes de executar os notebooks, você precisará:

1. Ter uma conta no **Google Cloud Platform (GCP)** com o BigQuery ativado.
2. Criar um **dataset** no BigQuery com permissões de leitura/escrita.
3. Substituir o ID do projeto pelo seu próprio nos notebooks:

```python
project_id = "seu-id-do-projeto"  # Substitua aqui
```

## 📥 Download dos Dados

Os dados utilizados neste case estão disponíveis publicamente pelo iFood:

| Arquivo              | Link                                                                 |
|----------------------|----------------------------------------------------------------------|
| `order.json.gz`      | https://data-architect-test-source.s3-sa-east-1.amazonaws.com/order.json.gz     |
| `consumer.csv.gz`    | https://data-architect-test-source.s3-sa-east-1.amazonaws.com/consumer.csv.gz   |
| `restaurant.csv.gz`  | https://data-architect-test-source.s3-sa-east-1.amazonaws.com/restaurant.csv.gz |
| `ab_test_ref.tar.gz` | https://data-architect-test-source.s3-sa-east-1.amazonaws.com/ab_test_ref.tar.gz |

Recomenda-se salvar os arquivos em um diretório `data/` ou carregar diretamente no BigQuery.

## ▶️ Ordem de Execução

1. `etl_process.ipynb`  
   - Carrega os dados do iFood, trata inconsistências e envia as tabelas limpas para o BigQuery.

2. `exploratory_data_analysis.ipynb`  
   - Realiza análises descritivas, estatísticas e segmentação de clientes via RFM.

3. `ifood_abtest_segmentation_results.ipynb`  
   - Avalia os resultados do Teste A/B (grupo controle x grupo com cupom), calcula métricas como ROI, lift, ticket médio e retention por segmento.

## 📊 Relatório Executivo

O relatório completo com análises, gráficos e recomendações está disponível em:

📄 `reports/relatorio_executivo.pdf`

Ele foi escrito com foco em stakeholders não técnicos, explicando de forma clara:

- Resultados estatísticos
- Análise financeira da campanha
- Segmentações estratégicas
- Propostas de novas campanhas mais eficazes

## 🧠 Principais Conclusões

- A campanha analisada gerou **incremento de pedidos e receita**, mas **não foi financeiramente viável** nas premissas adotadas (ROI negativo).
- **Segmentos como “New Customers” e “Potential Loyalists”** apresentaram maior potencial de retorno com cupons direcionados.
- Estratégias futuras devem priorizar **personalização e testes A/B iterativos por segmento**.

## 📌 Observações Finais

Este projeto utiliza **Google BigQuery** como motor principal de dados. Para executar os notebooks corretamente:

- Altere a variável `project_id` no início dos notebooks para o ID do seu projeto.
- Garanta que você tenha permissões suficientes para criar e consultar tabelas no BigQuery.
- Utilize o ambiente gratuito do **Google Colab** para execução sem dependências locais.

## 🙋‍♂️ Autor

Guilherme Fernandes  
[LinkedIn](https://www.linkedin.com/in/gnfernandes/)
