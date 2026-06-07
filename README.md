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

<img width="960" height="540" alt="Captura de tela 2026-06-05 183349" src="https://github.com/user-attachments/assets/5848767a-74d0-4c92-b918-e9c1201b6c96" /> **Código:**
```sql
SELECT 
    cidades.nome,
    cliente.nome,
    cliente.bairro,
    cliente.rua,
    vendas.valor_total
FROM cliente
INNER JOIN cidades ON cliente.CIDADES_ID = cidades.id
INNER JOIN vendas ON vendas.id_cliente = cliente.id
GROUP BY cidades.nome, cliente.nome, cliente.bairro, cliente.rua, vendas.valor_total;
