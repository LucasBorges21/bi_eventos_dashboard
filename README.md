<h1 align="center">📊 Power BI – Análise Comercial de Eventos</h1>

<p align="center">
  Projeto de Business Intelligence desenvolvido no Power BI para análise de desempenho comercial, receita e vendas no contexto de eventos corporativos.
</p>

---

## 🎯 Objetivos do Projeto

- Consolidar métricas de receita, conversão e ticket médio  
- Aplicar funções DAX e inteligência de tempo com tabela calendário  
- Demonstrar domínio de modelagem estrela (fato e dimensões)  
- Desenvolver um painel visual, interativo e orientado à decisão  

---

## 🗂 Estrutura do Projeto

```text
BI_EVENTOS_DASHBOARD/
├─ .venv/
│
├─ data/
│  ├─ dim_clientes.csv
│  ├─ dim_eventos.csv
│  ├─ dim_faturas.csv
│  ├─ dim_pedidos.csv
│  ├─ dim_vendedores.csv
│  └─ fato_vendas.csv
│
├─ dax/
│  ├─ dim_calendario_dax.txt
│  └─ medidas_dax.txt
│
├─ imagens/
│  ├─ dash1.png
│  └─ dash2.png
│
├─ relatorios/
│  └─ painel_eventos.pbix
│
├─ .gitignore
└─ README.md

Cada diretório contém:  
- **/data** – tabelas fato e dimensões usadas no Power BI  
- **/dax** – código da tabela calendário e medidas DAX personalizadas  
- **/imagens** – capturas de tela do painel final  
- **/relatorios** – arquivo `.pbix` do relatório principal  

---

## 🧠 Modelagem e Medidas DAX

O modelo segue uma arquitetura estrela, com tabelas de dimensão (`DIM_Eventos`, `DIM_Clientes`, `DIM_Pedidos`, `DIM_Vendedores`, `DIM_Calendário`) e uma tabela fato (`Fato_Vendas`).  
A tabela calendário foi criada diretamente no Power BI para habilitar funções de tempo como `TOTALYTD`, `DATEADD` e comparações mensais e anuais.

---

## 📏 Exemplos de Medidas DAX

Total Vendas = 
SUM(fato_vendas[valor_total])

Ticket Médio = 
DIVIDE([Total Vendas], COUNTROWS(fato_vendas), 0)

Variação % M/M = 
DIVIDE(([Total Vendas] - [Total Vendas Mês Anterior]), [Total Vendas Mês Anterior])

## 📊 Visual do Painel

<p align="center">
  <img src="https://github.com/LucasBorges21/bi_eventos_dashboard/blob/af8c6eec37df036c53ed592198b041aabe1b2069/imagens/dash1.png" width="850px" alt="Dashboard Power BI - Análise Comercial de Eventos">
</p>

O painel apresenta **indicadores de desempenho**, **gráficos de evolução temporal**, **distribuição de vendas por evento e vendedor**, além de um **overview financeiro consolidado**.  
Foram aplicados **segmentadores interativos**, **gráficos dinâmicos por período** e **análises de tendência de receita e variação mensal**.

---

## 💬 Conclusão

Este projeto demonstra minha capacidade de **modelar dados, aplicar DAX e desenvolver dashboards analíticos completos**.  
A estrutura segue boas práticas de BI, priorizando clareza, performance e aplicabilidade prática em cenários reais de negócio.

✦ *Autor:* **Lucas Borges**  
✦ *Propósito:* Portfólio de estudos em Análise de Dados e Business Intelligence
