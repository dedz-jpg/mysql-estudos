# Estudos em MySQL

Este repositório contém scripts e exemplos práticos do meu aprendizado em **SQL** e **bancos de dados relacionais**.  
O objetivo é documentar o processo de criação de tabelas, inserção de dados e consultas básicas no MySQL.

---

## Estrutura do repositório

mysql-estudos/
│
├── scripts/
│ ├── create_table.sql # Criação da tabela pessoas
│ ├── insert_pessoas.sql # Inserções de exemplo
│ └── select_pessoas.sql # Consultas de exemplo
│
├── imagens/
│ ├── mysql_bruna.png # Print inserindo Bruna
│ └── mysql_pablo.png # Print inserindo Pablo
│
└── README.md

sql
Copiar código

---

## Scripts SQL

### Criação da tabela
```sql
-- Cria a tabela pessoas com campos básicos
create table pessoas (
    id int not null auto_increment,
    nome varchar(30) not null,
    nascimento date,
    sexo enum('M','F'),
    peso decimal(5,2),
    altura decimal(3,2),
    nacionalidade varchar(20) default 'Brasil',
    primary key (id)
) default charset = utf8mb4;
Inserções de exemplo
sql
Copiar código
-- Inserindo uma pessoa com todos os dados preenchidos
insert into pessoas
(id, nome, nascimento, sexo, peso, altura, nacionalidade)
values
(DEFAULT, 'Bruna', '2002-10-25', 'F', 54, 1.69, 'Brasil');

-- Inserindo pessoa com valor DEFAULT para nacionalidade
insert into pessoas
values
(DEFAULT, 'Pablo', '2023-07-20', 'M', 90, 1.50, DEFAULT);
Consulta
sql
Copiar código
-- Consulta todos os registros da tabela
select * from pessoas;
Exemplos visuais
Inserção de Bruna

Registro da Bruna adicionado na tabela pessoas

Inserção de Pablo

Registro do Pablo utilizando valor DEFAULT para nacionalidade

Próximos passos
Criar novas tabelas relacionadas (ex: endereços, cursos, pedidos)

Estudar joins (INNER JOIN, LEFT JOIN, etc.)

Implementar chaves estrangeiras (FK)

Praticar normalização de banco de dados

Inserir mais consultas com filtros, ordenação e agrupamentos
