
<h1 align="center">:bar_chart: TelecomX - Analise de Evasão de Clientes</h1>

## 📌**Contexto do Projeto:**

Fui contratada como assistente de análise de dados na Telecom X e farei parte do projeto Churn de Clientes.

A empresa enfrenta um alto índice de cancelamentos e precisa compreender quais fatores influenciam a evasão de clientes.

Meu papel neste projeto é coletar, tratar e analisar os dados, utilizando Python e suas principais bibliotecas, com o objetivo de extrair insights estratégicos que apoiem a tomada de decisão.



## 🎯**Objetivo:**

O principal objetivo deste projeto é:

- Coletar e tratar os dados da TelecomX

- Analisar os dados de clientes da TelecomX

- Identificar padrões e variáveis associadas ao Churn

- Gerar insights que apoiem estratégias de redução da evasão



## 🗂️ Base de Dados

- Formato: JSON

- Origem: Repositório público no GitHub

- Total de registros: 7.267 clientes

- Durante a importação, foi identificado que parte das informações estava estruturada em dicionários (JSON aninhado), exigindo processos de normalização e tratamento para viabilizar a análise exploratória.



 ## 🧱 Estrutura do Dataset (Após Normalização)

Após o processo de normalização das colunas em formato de dicionários, a base de dados passou a ter uma estrutura tabular, com cada atributo representado em uma coluna independente.

| Coluna | Descrição |
|--------|-----------|
| customerID | Identificador único do cliente |
| Churn | Indica se o cliente cancelou o serviço |
| gender | Gênero do cliente |
| SeniorCitizen | Indica se o cliente é idoso (0 = Não, 1 = Sim) |
| Partner | Indica se o cliente possui parceiro(a) |
| Dependents | Indica se o cliente possui dependentes |
| tenure | Tempo de permanência do cliente (em meses) |
| PhoneService | Indica se o cliente possui serviço de telefonia |
| MultipleLines | Indica se o cliente possui múltiplas linhas |
| InternetService | Tipo de serviço de internet contratado |
| OnlineBackup | Indica se o cliente possui backup online |
| DeviceProtection | Indica se o cliente possui proteção de dispositivos |
| TechSupport | Indica se o cliente possui suporte técnico |
| StreamingTV | Indica se o cliente possui serviço de streaming de TV |
| StreamingMovies | Indica se o cliente possui serviço de streaming de filmes |
| Contract | Tipo de contrato do cliente |
| PaperlessBilling | Indica se o cliente utiliza fatura digital |
| PaymentMethod | Método de pagamento |
| Charges.Monthly | Valor mensal cobrado do cliente |
| Charges.Total | Valor total cobrado ao longo do contrato |



## 🔍 Etapas do Projeto:

### 1 - Importação dos Dados

- Carregamento da base de dados diretamente de uma URL pública no formato JSON.

---

### 2 - Limpeza e Tratamento dos Dados

- Normalização de colunas em formato de dicionário

- Ajuste de tipos de dados 

- Identificação e tratamento de valores ausentes, vazios incluindo a variável alvo Churn

- Criação de novas colunas Faixa etária e Contas Diárias

---

### 3 - Análise Exploratória de Dados (EDA)

- Análise da distribuição de clientes com e sem Churn
- Distribuição dos clientes status de Churn
- Análise das variaveis categoricas
- Contagem e comparação de clientes por variáveis

---

### 4 - Avaliação do impacto dos serviços contratados

- Análises de correlação entre variáveis

---

### 5 - Construção de gráficos para identificação de padrões

- Graficos de barras, setores, barras empilhadas, readmap

---

### 6 - Conclusões e Insights

Interpretação dos resultados com foco em comportamento do cliente e retenção.

- Cliente novo(1-5 meses) de contrato, sem parceiro, sem dependentes,usando fibra otica, sem serviços adicionais, paga por Eletronic Check e tem contrato mensal são os que mais cancelam.

- Quanto mais serviços contratados maior é a média mensal paga.

- Poucos clientes optam por pacotes completos

- Clientes que possuem streaming tendem a cancelar um pouco mais

---

### 7 - Recomendações

Sugestões estratégicas baseadas nos achados da análise.

- Incentivar clientes com poucos serviços a aderirem a pacotes mais completos.

- Incentivar upgrade para contratos anuais

- Promover serviços que demonstraram associação com maior retenção, como suporte técnico e segurança online.

- Criar campanhas específicas para estimular contratação de serviços adicionais.

- Monitoramento contínuo do Churn

- Criar pacotes de benefícios para os primeiros meses

- Contato proativo com clientes em risco (primeiros meses)



## 🛠️ Ferramentas e Tecnologias

- 🐍 **Python** – linguagem principal para análise de dados
- 🐼 **Pandas** – manipulação, limpeza e tratamento de dados
- 🔢 **NumPy** – operações matemáticas e computação numérica
- 📊 **Matplotlib** – visualização de dados
- 📈 **Seaborn** – visualização estatística e gráficos avançados
- ☁️ **Google Colab** – ambiente de desenvolvimento em nuvem
- ⚙️ **ETL** – extração, transformação e carga de dados
- 📂 **Git & GitHub** – versionamento de código e portfólio



## 🚀 Próximos Passos e Evoluções do Projeto

Como evolução natural deste estudo, são propostos os seguintes aprimoramentos com foco em automação, predição e apoio à tomada de decisão:

### 1 - Automação do Monitoramento de Churn
Implementação de um pipeline automatizado para monitorar novos cancelamentos à medida que novos dados forem incorporados à base. O objetivo é gerar **alertas automáticos** sempre que um cancelamento ocorrer, acompanhados de uma análise preliminar dos **possíveis fatores associados ao Churn**, com base em padrões históricos.

Essa automação permitirá uma atuação mais rápida e preventiva por parte das áreas de negócio.

---

### 2 - Modelagem Preditiva de Churn
Desenvolvimento de modelos de **Machine Learning** para prever a probabilidade de cancelamento de clientes ativos. A partir dessas previsões, será possível:
- Identificar clientes com maior risco de evasão
- Priorizar ações de retenção
- Otimizar campanhas e recursos

Modelos como Regressão Logística, Árvores de Decisão e Random Forest podem ser avaliados em etapas futuras.

---

### 3 - Identificação de Oportunidades de Upsell e Cross-sell
Criação de modelos analíticos para identificar clientes com maior propensão a **contratar novos serviços**, considerando histórico de uso, perfil e comportamento contratual. Essa abordagem pode apoiar estratégias de **aumento de ticket médio** e personalização de ofertas.

*Upsell é quando a empresa incentiva o cliente a migrar para um plano melhor ou mais caro do que o atual.*

*Cross-sell é quando a empresa oferece serviços adicionais que complementam o que o cliente já possui.*

---

### 4 - Visualização e Acompanhamento Gerencial
Construção de dashboards interativos para acompanhamento contínuo de indicadores de Churn, risco de cancelamento e oportunidades comerciais, facilitando a comunicação dos resultados para áreas não técnicas.

---

Essas evoluções ampliam o impacto do projeto, transformando a análise exploratória inicial em uma solução orientada por dados e voltada à tomada de decisão estratégica.



## 👩‍💻 Autor

Paulo Terra

Analista de TI | Gestor CPD | Infraestrutura e Projetos

Projeto desenvolvido para fins de estudo (Alura One) e portfólio profissional.











