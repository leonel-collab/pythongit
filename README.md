# Pythongit - Consultas SQL 🗄️

Repositório com queries SQL para análise de dados de vendas.

## 📋 juncao_de_tabelas_sql

## **Objetivo da Query:**
Relacionar dados de clientes, cidades e vendas para gerar um relatório consolidado por cliente e localização.

# **Tabelas utilizadas:**
- **cliente** - Dados cadastrais dos clientes
- **cidades** - Tabela de cidades 
- **vendas** - Registro de vendas com valor total

# **Técnicas aplicadas:**
1. **INNER JOIN** - Conecta `cliente` → `cidades` via `CIDADES_ID` e `cliente` → `vendas` via `id_cliente`
2. **SELECT específico** - Retorna apenas: nome da cidade, nome do cliente, bairro, rua e valor_total
##3. **GROUP BY** - Agrupa os resultados por cidade, cliente, bairro, rua e valor_total.

