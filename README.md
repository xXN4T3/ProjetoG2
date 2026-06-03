# Análise de Redes Sociais no Brasil

## 1. Descrição do Projeto

Este projeto apresenta uma análise de dados de redes sociais no Brasil utilizando técnicas de análise exploratória, visualização de dados, consultas SQL e desenvolvimento de dashboards interativos.

O objetivo é identificar padrões de desempenho entre diferentes plataformas digitais, avaliando métricas como alcance, visualizações, interações e taxa de engajamento, permitindo a geração de insights para estratégias de marketing digital.

O projeto foi desenvolvido como atividade acadêmica da disciplina de Análise e Visualização de Dados com Python.

---

## 2. Problema de Negócio

Empresas e criadores de conteúdo precisam compreender o desempenho de suas publicações em diferentes redes sociais para otimizar estratégias de comunicação e marketing.

As principais perguntas respondidas pelo projeto são:

* Qual plataforma apresenta maior alcance?
* Qual plataforma gera mais visualizações?
* Qual plataforma possui maior taxa média de engajamento?
* Quais tipos de conteúdo apresentam melhor desempenho?
* Como os indicadores evoluem ao longo do tempo?
* Como utilizar dados para apoiar decisões de marketing digital?

---

## 3. Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Streamlit
* SQLite
* SQLAlchemy
* Jupyter Notebook
* Google Colab
* GitHub

---

## 4. Estrutura do Projeto

```text
projeto_redes_sociais_brasil_G2/
│
├── index.html
├── app.py
├── requirements.txt
├── README.md
├── dados
│   └── simulacao_redes_sociais_brasil.csv
├── database
│   └── redes_sociais.sqlite
├── notebooks
│   └── analise_redes_sociais_brasil_NathanSilvaCardoso1.0.ipynb
```

---

## 5. Base de Dados

A base de dados contém informações simuladas sobre o desempenho de publicações em redes sociais brasileiras.

Principais atributos:

* Data da publicação
* Plataforma
* Tipo de conteúdo
* Alcance
* Visualizações
* Curtidas
* Comentários
* Compartilhamentos
* Taxa de engajamento

Durante o processamento dos dados foram criadas métricas derivadas, como:

* Ano
* Mês
* Ano/Mês
* Interações Totais

---

## 6. Processo Analítico

O projeto segue as seguintes etapas:

1. Importação da base CSV.
2. Tratamento e preparação dos dados.
3. Criação de métricas derivadas.
4. Análise exploratória dos dados.
5. Construção de visualizações.
6. Persistência dos dados em banco SQLite.
7. Realização de consultas SQL.
8. Desenvolvimento de dashboard interativo com Streamlit.
9. Disponibilização da documentação do projeto em página HTML.

---

## 7. KPIs Utilizados

| KPI                       | Descrição                                    |
| ------------------------- | -------------------------------------------- |
| Visualizações Totais      | Soma de todas as visualizações               |
| Alcance Total             | Soma do alcance das publicações              |
| Interações Totais         | Curtidas + Comentários + Compartilhamentos   |
| Taxa Média de Engajamento | Média da taxa de engajamento das publicações |

---

## 8. Funcionalidades do Dashboard

O dashboard desenvolvido em Streamlit possui:

### Filtros Interativos

* Plataforma
* Tipo de Conteúdo
* Ano

### Indicadores

* Visualizações Totais
* Alcance Total
* Interações Totais
* Engajamento Médio

### Visualizações

* Evolução temporal das visualizações
* Alcance por plataforma
* Engajamento médio por plataforma
* Engajamento por tipo de conteúdo

### Banco de Dados

* Integração com SQLite
* Consultas SQL demonstrativas
* Exibição dos resultados diretamente no dashboard

### Dados

* Visualização da base filtrada em formato tabular

---

## 9. Consulta SQL Utilizada

Exemplo de consulta implementada no projeto:

```sql
SELECT
    plataforma,
    SUM(alcance) AS alcance_total,
    SUM(visualizacoes) AS visualizacoes_total,
    AVG(taxa_engajamento) AS engajamento_medio
FROM redes_sociais
GROUP BY plataforma
ORDER BY alcance_total DESC;
```

Esta consulta permite comparar o desempenho geral entre as plataformas analisadas.

---

## 10. Como Executar o Projeto

### 1. Clonar o Repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd projeto_redes_sociais_brasil
```

### 2. Instalar Dependências

```bash
pip install -r requirements.txt
```

### 3. Executar o Dashboard

```bash
streamlit run app.py
```

---

## 11. Principais Análises Realizadas

* Comparação de desempenho entre plataformas.
* Avaliação do alcance total por rede social.
* Análise de engajamento por tipo de conteúdo.
* Evolução temporal das visualizações.
* Consultas SQL para apoio à análise.
* Construção de indicadores de desempenho (KPIs).

---

## 12. Objetivo Pedagógico

Este projeto tem como objetivo aplicar conceitos de:

* Análise exploratória de dados;
* Manipulação de dados com Pandas;
* Visualização de dados com Matplotlib e Seaborn;
* Integração com bancos de dados SQLite;
* Consultas SQL utilizando SQLAlchemy;
* Desenvolvimento de dashboards com Streamlit;
* Organização e documentação de projetos de ciência de dados.

O resultado final demonstra um fluxo completo de análise de dados, desde a coleta e preparação da informação até a geração de dashboards interativos para apoio à tomada de decisão.

---

## Autor

**Nathan Silva Cardoso**

Projeto desenvolvido para fins acadêmicos na disciplina Linguagens de Programação
