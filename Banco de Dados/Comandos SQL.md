# Resumo de Comandos SQL

Este documento apresenta um resumo dos principais tipos de comandos SQL: **DDL**, **DML**, **DQL**, **DCL** e **DTL**, com exemplos práticos para cada categoria.

---

## 📘 DDL - Data Definition Language

Comandos responsáveis pela definição da estrutura do banco de dados (tabelas, colunas, tipos de dados, etc).

### Exemplos:

```sql
-- Criar uma tabela
CREATE TABLE funcionarios (
    id INT PRIMARY KEY,
    nome VARCHAR(100),
    salario DECIMAL(10,2),
    admissao DATE
);

-- Alterar uma tabela
ALTER TABLE funcionarios ADD COLUMN departamento VARCHAR(50);

-- Excluir uma tabela
DROP TABLE funcionarios;
```

---

## ✏️ DML - Data Manipulation Language

Comandos usados para manipular os dados dentro das tabelas.

### Exemplos:

```sql
-- Inserir dados
INSERT INTO funcionarios (id, nome, salario, admissao)
VALUES (1, 'Ana Souza', 3500.00, '2020-03-15');

-- Atualizar dados
UPDATE funcionarios SET salario = 4000.00 WHERE id = 1;

-- Deletar dados
DELETE FROM funcionarios WHERE id = 1;
```

---

## 🔍 DQL - Data Query Language

Comando usado para consultar dados no banco.

### Exemplos:

```sql
-- Selecionar todos os dados
SELECT * FROM funcionarios;

-- Selecionar com filtro
SELECT nome, salario FROM funcionarios WHERE salario > 3000;
```

---

## 🔐 DCL - Data Control Language

Comandos usados para controlar permissões e acessos ao banco de dados.

### Exemplos:

```sql
-- Conceder permissão
GRANT SELECT, INSERT ON funcionarios TO 'usuario';

-- Revogar permissão
REVOKE INSERT ON funcionarios FROM 'usuario';
```

---

## 🔄 DTL - Data Transaction Language

Comandos usados para gerenciar transações no banco de dados.

### Exemplos:

```sql
-- Iniciar uma transação
START TRANSACTION;

-- Executar comandos
UPDATE funcionarios SET salario = salario * 1.1;

-- Confirmar a transação
COMMIT;

-- Ou desfazer a transação
ROLLBACK;
```

---

> ✅ **Observação:** Nem todos os bancos de dados implementam DTL como uma categoria separada, mas os comandos de transação são amplamente suportados.
