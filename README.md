# Estudos em MySQL

Este repositório contém scripts e exemplos práticos do meu aprendizado em **SQL** e bancos de dados relacionais.  
Aqui você verá criação de tabelas, inserção de dados, consultas básicas e visualização dos resultados.

---

## Estrutura do repositório

mysql-estudos/
│
├── scripts/
│ ├── create_table.sql # Cria a tabela pessoas
│ ├── insert_pessoas.sql # Inserções de exemplo
│ └── select_pessoas.sql # Consulta de exemplo
│
├── imagens/
│ ├── mysql_bruna.png # Print inserindo Bruna
│ └── mysql_pablo.png # Print inserindo Pablo
│
└── README.md

sql

---

## Scripts SQL

### Criação da tabela

```sql
-- Cria tabela `pessoas` com vários tipos de coluna para praticar
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

-- Inserindo uma pessoa com todos os campos preenchidos
insert into pessoas
(id, nome, nascimento, sexo, peso, altura, nacionalidade)
values
(DEFAULT, 'Bruna', '2002-10-25', 'F', 54, 1.69, 'Brasil');

-- Inserindo pessoa usando valor DEFAULT para nacionalidade
insert into pessoas
(nome, nascimento, sexo, peso, altura)
values
('Pablo', '2023-07-20', 'M', 90, 1.50);
Consulta
sql

-- Consulta todos os registros da tabela `pessoas`
select * from pessoas;
Exemplos visuais
<p align="center"> <img src="imagens/mysql_bruna.png" alt="Inserção de Bruna" width="400"/> </p> <p align="center"><em>Inserção de Bruna na tabela `pessoas`</em></p> <p align="center"> <img src="imagens/mysql_pablo.png" alt="Inserção de Pablo" width="400"/> </p> <p align="center"><em>Inserção de Pablo (com DEFAULT em nacionalidade)</em></p>


Normalização do banco: 1ª, 2ª, 3ª forma normal

Consultas mais complexas: filtros, ordenações, agrupamentos, funções agregadas
