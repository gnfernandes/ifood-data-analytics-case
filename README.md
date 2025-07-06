# Case Técnico de Data Analytics - iFood

Este repositório contém a solução desenvolvida para o Case Técnico de Data Analytics do iFood, focado na análise de uma estratégia de cupons para retenção de usuários e na criação de segmentações de usuários.

## Estrutura do Repositório

- `notebooks/`: Contém os notebooks Jupyter com o processamento de dados (ETL) e as análises exploratórias e de segmentação.
- `reports/`: Contém o relatório final em PDF com as conclusões e sugestões para as lideranças de negócio.
- `README.md`: Este arquivo, com a descrição do projeto e instruções.

## Como Executar o Projeto

Para replicar a análise e os resultados deste projeto, siga os passos abaixo:

### 1. Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas:

- Python 3.x
- Jupyter Notebook ou JupyterLab
- Bibliotecas Python: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn` (e outras que possam ser necessárias para a análise de dados).

Você pode instalar as bibliotecas necessárias usando `pip`:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 2. Configuração do Ambiente

1. Clone este repositório para o seu ambiente local:

   ```bash
   git clone <URL_DO_SEU_REPOSITORIO>
   cd ifood_case_study
   ```

2. Os dados utilizados neste case são fornecidos pelo iFood e podem ser acessados através dos links abaixo:

   - Pedidos (order.json): `https://data-architect-test-source.s3-sa-east-1.amazonaws.com/order.json.gz`
   - Usuários (consumers.csv): `https://data-architect-test-source.s3-sa-east-1.amazonaws.com/consumer.csv.gz`
   - Merchants (restaurant.csv): `https://data-architect-test-source.s3-sa-east-1.amazonaws.com/restaurant.csv.gz`
   - Marcação de usuários que participaram do teste A/B (ab_test_ref.csv): `https://data-architect-test-source.s3-sa-east-1.amazonaws.com/ab_test_ref.tar.gz`

   Recomenda-se baixar esses arquivos e colocá-los em um diretório `data/` na raiz do projeto, ou ajustar os caminhos nos notebooks para onde você os salvou.

### 3. Executando os Notebooks

Os notebooks devem ser executados na seguinte ordem para garantir a correta sequência de processamento e análise:

1. `notebooks/03_etl_process.ipynb`: Realiza o processo de ETL (Extração, Transformação e Carga) dos dados.
2. `notebooks/01_exploratory_data_analysis.ipynb`: Contém a análise exploratória dos dados e a definição de indicadores.
3. `notebooks/02_data_cleaning.ipynb`: Aborda a análise de segmentação e os resultados do teste A/B com base nos segmentos definidos.

Para abrir e executar os notebooks:

```bash
jupyter notebook
```

Navegue até o diretório `notebooks/` e abra cada arquivo `.ipynb` na ordem especificada.

## Análise e Conclusões

Para uma visão detalhada das análises, conclusões e recomendações, consulte o relatório final:

- `reports/ifood_data_analytics_report.pdf`

Este relatório é destinado a líderes de negócio e apresenta os insights de forma clara e concisa, sem a necessidade de conhecimento técnico aprofundado.
