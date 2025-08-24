## 📌 Descrição
Este repositório contém um **pipeline de dados financeiros** simples utilizado para alimentar o [dashboard-financeiro](./dashboard-financeiro) e [previsao-custos](./previsao-custos).  
O projeto realiza a **extração, transformação e carregamento (ETL)** dos dados, garantindo atualização incremental e automatizada em um banco open source online **Postgres (Supabase)**.

## 🚀 Objetivos do Projeto
- Automatizar a **captura de dados financeiros** via API.
- Realizar a **transformação e limpeza** dos dados com **Pandas**.
- Implementar **armazenamento incremental** em banco de dados relacional.
- Disponibilizar dados estruturados para uso em **dashboards (Power BI)** e outras análises.
- Permitir **execução automatizada** com script `.bat` e agendamento no **Windows Task Scheduler**.

## 🗂️ Fontes de Dados
- **APIs Financeiras** → Coleta de dados brutos.
- **Postgres (Supabase)** → Banco de dados para armazenamento incremental.

## 🔄 Fluxo de Processamento
1. **Extração** → `fetch_data.py` coleta dados via API.  
2. **Transformação** → `etl.py` aplica regras de limpeza, padronização e cálculos.  
3. **Carga** → `load.py` insere dados no **Postgres (Supabase)** de forma incremental.  
4. **Execução automatizada** → `run_all.bat` + agendamento no Windows Task Schedulerroda todas as etapas em sequência. 
