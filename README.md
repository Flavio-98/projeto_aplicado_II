# Análise de Assinaturas e Cancelamentos NETFLIX - Projeto Aplicado II

## Equipe  
* *KAIQUE NASCIMENTO DE PAULA* - RA: 24024831  
* *MOACYR SOUZA BARROS* - RA: 10441179  
* *MIGUEL SHIRAISHI* - RA: 10431805  
* *FLÁVIO ESTEVAM NOGUEIRA* - RA: 10441572  

---

## 1. Definição da Organização  

### *Organização: Netflix*  
A Netflix é uma empresa global de entretenimento que oferece serviços de streaming de filmes, séries e documentários via internet. Sua plataforma está disponível em mais de 190 países e conta com uma ampla base de assinantes que podem escolher entre diferentes tipos de assinatura (Basic, Standard, Premium).  

### *Missão*  
Proporcionar uma experiência de entretenimento personalizada e de alta qualidade para seus assinantes ao redor do mundo, através de uma vasta biblioteca de conteúdos e de um serviço inovador.  

### *Modelo de Receita*  
A receita da Netflix é baseada em assinaturas mensais, com diferentes planos que oferecem variações na qualidade do streaming e no número de telas simultâneas. A empresa utiliza análises de dados extensivas para personalizar recomendações de conteúdo e otimizar a retenção de usuários.  

---

## 2. Apresentação dos Dados Utilizados (Metadados)  

A base de dados fornecida contém informações sobre os assinantes da plataforma, suas assinaturas e características demográficas.  

| Coluna              | Descrição                                                   | Tipo de Dado  |
|---------------------|------------------------------------------------------------|---------------|
| User ID            | Identificador único de cada usuário                        | Numérico     |
| Subscription Type  | Tipo de assinatura (Basic, Standard, Premium)              | Categórico   |
| Monthly Revenue    | Receita mensal gerada por cada usuário (em dólares)       | Numérico     |
| Join Date          | Data de adesão do usuário à plataforma (dd-mm-aa)         | Data         |
| Last Payment Date  | Data do último pagamento realizado pelo usuário (dd-mm-aa) | Data         |
| Country           | País de origem/residência do usuário                       | Categórico   |
| Age                | Idade do usuário                                           | Numérico     |
| Gender            | Gênero do usuário (Masculino, Feminino)                   | Categórico   |
| Device            | Dispositivo usado para acessar a plataforma                 | Categórico   |
| Plan Duration     | Duração do plano atual do usuário (1 mês, 6 meses, etc.)  | Categórico   |

---

## 3. Objetivos e Metas  

### *Objetivo Geral*  
Explorar dados demográficos e comportamentais dos assinantes da Netflix para gerar insights sobre comportamento do usuário, prever cancelamentos (*churn*) e identificar oportunidades de campanhas para aumentar a retenção e o engajamento.  

### *Objetivos Específicos*  
- Analisar o comportamento dos usuários com base no país, idade, gênero e dispositivo utilizado;  
- Identificar possíveis cancelamentos e desenvolver estudos/propostas para minimizar o churn;  
- Propor estratégias de retenção e campanhas de marketing com base nos dados analisados.  

---

## 4. Cronograma de Atividades (Estimativa)  

| Fase                        | Tarefa                                              | Status    | Data de Entrega |
|-----------------------------|----------------------------------------------------|----------|----------------|
| *Etapa 1*                 | Definição da organização, área de atuação e dados | Feito | 03/03/2025     |
| *Etapa 2*                 | Desenvolvimento de visualizações e narrativas     | Feito | 31/03/2025     |
| *Etapa 3*                 | Análise dos resultados e previsão de churn       | Feito | 28/04/2025     |
| *Etapa 4*                 | Apresentação final do projeto                     | Feito | 26/05/2025     |

---

## 5 Análise de Dados de Assinaturas de Plataforma

### Apresentação dos Dados Utilizados

Este projeto analisa uma base de dados que contém informações sobre assinantes de uma plataforma, suas assinaturas e características demográficas.

### Metadados

| Coluna             | Descrição                                         | Tipo de Dado |
|--------------------|---------------------------------------------------|--------------|
| User ID            | Identificador único de cada usuário.              | Numérico     |
| Subscription Type  | Tipo de assinatura (Basic, Standard, Premium).    | Categórico   |
| Monthly Revenue    | Receita mensal gerada por cada usuário (em dólares). | Numérico     |
| Join Date          | Data de adesão do usuário à plataforma (dd-mm-aa). | Data         |
| Last Payment Date  | Data do último pagamento realizado (dd-mm-aa).     | Data         |
| Country            | País de origem/residência do usuário.             | Categórico   |
| Age                | Idade do usuário.                                | Numérico     |
| Gender             | Gênero do usuário (Masculino, Feminino).          | Categórico   |
| Device             | Dispositivo usado para acessar a plataforma.        | Categórico   |
| Plan Duration      | Duração do plano atual (1 mês, 6 meses, etc.).    | Categórico   |

**Total:** 10 colunas e 2500 linhas.

### Fluxo de Análise

A análise seguiu um fluxo lógico de exploração e interpretação dos dados:

* **Importação e limpeza dos dados:**
    * Carregamento do dataset com pandas.
    * Tratamento de valores ausentes e inconsistências.
    * Conversão de tipos de dados.
* **Análise Exploratória de Dados (EDA):**
    * Estatísticas descritivas (describe(), info()).
    * Gráficos para distribuições e tendências (histograma, boxplot, scatterplot).
* **Visualização e Identificação de Tendências:**
    * Uso do seaborn para gráficos (dispersão, barras, heatmaps).
    * Comparação de métricas entre planos de assinatura.
    * Identificação de padrões no comportamento dos assinantes.
* **Geração de insights:**
    * Interpretação de dados visuais e estatísticos.
    * Identificação de fatores de cancelamento.
    * Sugestões de estratégias de retenção.

### Ferramentas e Tecnologias Utilizadas

* **Python:** Linguagem principal.
* **Jupyter Notebook:** Ambiente interativo de desenvolvimento.

### Bibliotecas Utilizadas

* **pandas:** Carregamento, manipulação e tratamento de dados.
* **seaborn:** Criação de gráficos estatísticos e visualizações.
* **matplotlib:** Construção e personalização de visualizações.
* **datetime:** Manipulação de datas e horários.
* **sklearn.model_selection.train_test_split:** Para dividir o dataset em conjuntos de treino e teste.
* **sklearn.tree.DecisionTreeClassifier:** Para implementar o modelo de Árvore de Decisão para classificação.
* **sklearn.metrics:** Para avaliar o desempenho do modelo através de métricas como acurácia, precision, recall, F1-Score, relatório de classificação, matriz de confusão e curva ROC/AUC.
* **imblearn.over_sampling.SMOTE:** Para aplicar a técnica de Synthetic Minority Over-sampling Technique (SMOTE) no tratamento de dados desbalanceados.

### Análise Exploratória

A análise exploratória buscou identificar correlações entre características dos usuários e o cancelamento da assinatura.

### Dados Analisados

* Distribuição de assinantes por idade, gênero e país.
* Frequência de cancelamentos ao longo do tempo.
* Tipos de planos mais populares e propensos ao cancelamento.

**Principais Descobertas:**

* Maior parte dos cancelamentos nos primeiros três meses.
* Plano básico com maior taxa de cancelamento.
* Retenção mais eficaz em assinantes mais jovens.

  Os gráficos gerados estão disponíveis no repositório do GitHub.

 ## 6. Método Analítico Aplicado

**Inferência de Churn:**

* Usuários com "Last Payment Date" superior a 30 dias em relação a 01/08/2023 foram considerados como churn.

**Modelo Preditivo:**

* Utilizou-se uma Árvore de Decisão (`DecisionTreeClassifier`) para modelar a probabilidade de cancelamento.

**Pré-processamento:**

* Variáveis categóricas foram transformadas utilizando a técnica de one-hot encoding.
* A base de dados foi dividida em conjuntos de treino (70%) e teste (30%).
* Para lidar com o desbalanceamento severo da base de dados, foram aplicadas técnicas de balanceamento de classes (SMOTE) e ajuste de pesos (`class_weight='balanced'`).

**Análise Exploratória Adicional:**

Além do modelo preditivo, também foram consideradas as seguintes distribuições e tendências:

* Distribuição de assinantes por idade, gênero e país.
* Frequência de cancelamentos ao longo do tempo.
* Tipos de planos mais populares e aqueles com maior propensão ao cancelamento.

## 7. Avaliação do Modelo e Métricas

Os resultados do modelo preditivo no conjunto de teste foram os seguintes:

* **Acurácia:** 52,27%
* **Precision:** 43,68%
* **Recall:** 62,71%
* **F1-Score:** 51,49%

Esses resultados demonstram que, apesar do desbalanceamento inicial dos dados, o modelo alcançou um bom equilíbrio entre a identificação de canceladores reais (bom recall) e a minimização de falsos positivos (precision razoável), especialmente considerando as técnicas de balanceamento aplicadas. O F1-Score, que combina precision e recall, indica um desempenho geral satisfatório do modelo.

## 8. Resultados Preliminares e Insights

A análise dos dados e os resultados do modelo preditivo forneceram insights valiosos sobre o perfil dos usuários mais propensos ao churn e potenciais oportunidades de negócio:

**Perfil do usuário mais propenso ao churn:**

* **Plano:** Basic
* **Idade:** 18-25 anos
* **Dispositivo:** Predominância de laptop
* **Países:** Mercados emergentes

**Oportunidades de negócio:**

* Desenvolver promoções e melhorias focadas no plano Basic para aumentar sua retenção.
* Implementar campanhas de marketing específicas para o público jovem adulto (18-25 anos).
* Incentivar o uso multiplataforma, destacando os benefícios da utilização em diferentes dispositivos (ex.: smart TV + mobile).

**Ponto de atenção:**

* A maior parte dos cancelamentos ocorre nos primeiros três meses de assinatura, indicando a importância de estratégias de engajamento e valorização do serviço logo após a adesão.

## 9. Visualização de Dados

Os gráficos gerados durante a análise (inclusos no repositório do GitHub) oferecem uma visualização clara dos dados e auxiliam na compreensão dos comportamentos mais críticos para o negócio, como a distribuição de churn por diferentes características dos usuários e a frequência de cancelamentos ao longo do tempo.

## 10. Esboço do Storytelling

**Contexto:**

Mercado de streaming altamente competitivo. Retenção de clientes é vital.

**Problema:**

Churn elevado em determinados perfis de usuário. Durante o projeto, foi identificado um forte desbalanceamento nos dados, com predominância de clientes cancelados. Técnicas de balanceamento de classes foram aplicadas para melhorar a capacidade preditiva do modelo.

**Solução:**

Modelo de Machine Learning para identificar usuários de risco e antecipar ações de retenção.

**Impacto:**

Aumento potencial da taxa de retenção em até 10%, com melhora da receita e diminuição dos custos de aquisição. 

---

## 11. Estrutura do Repositório  

O projeto está organizado da seguinte forma no repositório:  

📂 projeto_aplicado_II
│
│-- 📁 data/ # Arquivos de dados utilizados na análise
│ │-- 📄 Netflix_Userbase.csv # Dataset com os dados da Netflix
│
│-- 📄 README.md # Documentação do projeto
