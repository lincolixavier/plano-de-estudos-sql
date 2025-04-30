# Estude SQL por 90 dias

---

# 📅 **Plano de Estudo SQL + PostgreSQL — 90 Dias para se tornar MESTRE**

### ⚙️ Regras:
- Estudo médio: **1h a 2h/dia** (ajustável)
- Teoria + prática todos os dias
- Use um banco real local (PostgreSQL via Docker ou pgAdmin)
- Use sempre `EXPLAIN ANALYZE` a partir da metade do plano
- Progresso semanal deve incluir projeto prático real (ex: mini app, dashboard, blog, API)

---

## 🔵 **FASE 1 — FUNDAMENTOS ABSOLUTOS (Dias 1–30)**

### Semana 1 — Introdução ao SQL + SELECT básico

| Dia | Tópico | Prática recomendada |
|-----|--------|----------------------|
| 1 | Instalação PostgreSQL, psql ou DBeaver | Rodar primeiro SELECT no `pg_catalog.pg_tables` |
| 2 | `SELECT`, `FROM`, `WHERE` | Buscar usuários por nome e ID |
| 3 | `AND`, `OR`, `IN`, `BETWEEN` | Criar filtro de idade entre 20 e 30 |
| 4 | `ORDER BY`, `LIMIT`, `OFFSET` | Paginar uma lista de produtos |
| 5 | `INSERT INTO` com valores fixos | Inserir usuários, produtos, categorias |
| 6 | `UPDATE`, `DELETE` com cuidado | Atualizar um nome, deletar um usuário |
| 7 | Revisão prática + mini quiz (SQLBolt, Mode, Leetcode Easy) | |

### Semana 2 — Tipos de dados + Operadores

| Dia | Tópico | Prática |
|-----|--------|--------|
| 8 | Tipos SQL: `TEXT`, `UUID`, `INT`, `BOOLEAN`, `TIMESTAMP` | Criar tabela `events` |
| 9 | `IS NULL`, `COALESCE`, `CASE WHEN` | Exibir "Sem nome" onde nome for null |
| 10 | Funções: `UPPER()`, `LOWER()`, `NOW()`, `AGE()` | Formatar nomes e calcular idade |
| 11 | `DISTINCT`, `COUNT`, `SUM`, `AVG`, `MIN`, `MAX` | Contar usuários por cidade |
| 12 | `GROUP BY`, `HAVING` | Contar produtos por categoria com mais de 10 produtos |
| 13 | Subqueries simples (`SELECT` dentro de `WHERE`) | Buscar maiores preços |
| 14 | Mini desafio com subqueries + agregações | |

### Semana 3 — Relacionamentos e JOINs

| Dia | Tópico | Prática |
|-----|--------|--------|
| 15 | `INNER JOIN` básico | Tabela `users` + `orders` |
| 16 | `LEFT JOIN`, `RIGHT JOIN` | Ver usuários sem pedidos |
| 17 | `FULL JOIN`, `CROSS JOIN` | Combinações de promoções e produtos |
| 18 | Joins múltiplos encadeados | 3 tabelas: `users`, `orders`, `products` |
| 19 | Joins com subqueries | Buscar últimas compras de cada cliente |
| 20 | `ON` vs `USING` | Criar exemplo com `USING(user_id)` |
| 21 | Mini desafio só com JOINs (pgExercises) | |

### Semana 4 — Modelagem e consultas úteis

| Dia | Tópico | Prática |
|-----|--------|--------|
| 22 | Criar esquema de blog (users, posts, comments, tags) | Esquema no DBeaver ou draw.io |
| 23 | Normalização: 1NF, 2NF, 3NF (conceito) | Refatorar tabela mal modelada |
| 24 | `EXISTS`, `NOT EXISTS`, `IN`, `ANY`, `ALL` | Filtrar usuários com ou sem pedidos |
| 25 | `ARRAY`, `UNNEST`, `string_to_array`, `array_agg` | Guardar múltiplos valores em colunas |
| 26 | `JSONB`: operadores, indexação, leitura | Tabela `events` com payload JSON |
| 27 | Criar views e reusar queries | View de pedidos ativos com total acima de R$ 100 |
| 28 | Revisão geral + mini projeto CRUD simples (Ex: Users + Orders) | |

---

## 🟠 **FASE 2 — SQL AVANÇADO + RECURSOS POSTGRES (Dias 31–60)**

### Semana 5 — CTEs, funções e views

| Dia | Tópico | Prática |
|-----|--------|--------|
| 29 | CTE básica (`WITH`) | Calcular total de pedidos por cliente |
| 30 | CTEs aninhadas + recursivas | Criar árvore de categorias |
| 31 | Views vs Materialized Views | Cache de analytics |
| 32 | `CREATE FUNCTION`, `RETURNS`, `plpgsql` | Função para calcular desconto |
| 33 | `DO $$ BEGIN ... END $$` | Bloco anônimo para execuções rápidas |
| 34 | Funções com `INOUT`, `RAISE NOTICE`, `IF THEN` | Logs de auditoria simples |
| 35 | Mini desafio: usar CTE + função + view | |

### Semana 6 — Performance + índices

| Dia | Tópico | Prática |
|-----|--------|--------|
| 36 | `EXPLAIN`, `EXPLAIN ANALYZE` | Medir performance de query |
| 37 | `CREATE INDEX`, `UNIQUE`, `GIN`, `BTREE` | Índice em coluna `email`, `JSONB`, `tsvector` |
| 38 | Fatores que afetam performance (sequential vs index scan) | |
| 39 | Otimização com filtro seletivo e agregações | |
| 40 | Analisar planos ruins, reescrever query | |
| 41 | `VACUUM`, `ANALYZE`, `REINDEX`, autovacuum | |
| 42 | Desafio: encontrar gargalo real com dados mockados | |

### Semana 7 — Segurança, Transações, Controle

| Dia | Tópico | Prática |
|-----|--------|--------|
| 43 | `BEGIN`, `COMMIT`, `ROLLBACK` | Simular erro em transação |
| 44 | Isolation Levels: `READ COMMITTED`, `REPEATABLE READ`, `SERIALIZABLE` | Verificar efeitos com concorrência |
| 45 | Locks: `FOR UPDATE`, `NOWAIT`, `SKIP LOCKED` | Simular filas com bloqueios |
| 46 | Roles: `CREATE ROLE`, `GRANT`, `REVOKE` | Usuário só leitura |
| 47 | `SECURITY DEFINER`, `SET ROLE`, `pg_roles` | Funções seguras |
| 48 | Auditar acessos com triggers + log | |
| 49 | Revisão: segurança e integridade transacional | |

### Semana 8 — Projeto intermediário

| Dia | Tópico | Prática |
|-----|--------|--------|
| 50–56 | Criar sistema com dashboard de analytics, filtros, joins, views, CTEs, funções e index | Projeto: vendas, receitas, usuários, logs |

---

## 🔴 **FASE 3 — MESTRIA AVANÇADA (Dias 61–90)**

### Semana 9 — Window functions

| Dia | Tópico | Prática |
|-----|--------|--------|
| 57 | `ROW_NUMBER()`, `RANK()`, `DENSE_RANK()` | Top 3 usuários por mês |
| 58 | `PARTITION BY`, `ORDER BY`, `OVER()` | Agrupamento com posição |
| 59 | `LAG()`, `LEAD()`, `FIRST_VALUE()` | Comparar valores entre linhas |
| 60 | `NTILE()`, `CUME_DIST()` | Quartis e percentis |
| 61 | Casos reais com window + joins | Ranking de engajamento |
| 62 | Desafio completo de window functions | |
| 63 | Revisão com EXPLAIN de tudo | |

### Semana 10 — Extensões poderosas

| Dia | Tópico | Prática |
|-----|--------|--------|
| 64 | `pg_trgm` para busca fuzzy | LIKE com tolerância |
| 65 | `citext` para ignorar case | Email sem case sensitivity |
| 66 | `uuid-ossp`, `hstore`, `postgis` (visão geral) | Instalar e usar |
| 67 | Full-text search: `tsvector`, `tsquery` | Implementar busca com relevância |
| 68 | Indexação com GIN e FTS | Ver diferença de performance |
| 69 | JSONB + text search combinados | |
| 70 | Mini projeto de busca avançada | |

### Semana 11 — Particionamento, replicação e backup

| Dia | Tópico | Prática |
|-----|--------|--------|
| 71 | Tabelas particionadas (range, list) | Particionar por mês |
| 72 | `pg_partman`, `pg_cron` (visão) | Agendamentos |
| 73 | Backup e restore: `pg_dump`, `pg_restore` | Dump local do projeto |
| 74 | `pg_stat_statements` para análise | Ver queries mais pesadas |
| 75 | `pgbouncer` e pooling | |
| 76 | Monitoramento com `pgBadger`, `Prometheus` (visão) | |
| 77 | Revisão e preparação final | |

### Semana 12 — Projeto final de maestria

| Dia | Tópico | Prática |
|-----|--------|--------|
| 78–90 | Projeto final completo (com CRUD, analytics, segurança, views, triggers, funções, CTEs, índices e monitoramento). Escolha entre: |
- Sistema de gestão de vendas (ERP simplificado)  
- Analytics de rede social (likes, followers, engajamento)  
- Plataforma de conteúdo (blog com busca, tags, autores)

---

