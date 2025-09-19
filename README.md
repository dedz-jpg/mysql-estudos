# Estudos em MySQL

Este repositório contém scripts e exemplos práticos do meu aprendizado em **SQL** e bancos de dados relacionais.  
Aqui você verá criação de tabelas, inserção de dados, consultas básicas e visualização dos resultados.

---

## Estrutura do repositório

mysql-estudos/
│
├── scripts/
│ ├── create_table.sql # Criação da tabela pessoas
│ ├── insert_pessoas.sql # Inserções de exemplo
│ └── select_pessoas.sql # Consulta de exemplo
│
├── imagens/
│ ├── mysql_bruna.png # Print da inserção da Bruna
│ └── mysql_pablo.png # Print da inserção do Pablo
│
└── README.md

sql
Copiar código

---

## Scripts SQL

### Criação da tabela

```sql
-- Cria a tabela `pessoas` com campos básicos
CREATE TABLE pessoas (
    id INT NOT NULL AUTO_INCREMENT,
    nome VARCHAR(30) NOT NULL,
    nascimento DATE,
    sexo ENUM('M', 'F'),
    peso DECIMAL(5,2),
    altura DECIMAL(3,2),
    nacionalidade VARCHAR(20) DEFAULT 'Brasil',
    PRIMARY KEY (id)
) DEFAULT CHARSET = utf8mb4;
Inserções de exemplo
sql

-- Inserindo uma pessoa com todos os campos preenchidos
INSERT INTO pessoas
(id, nome, nascimento, sexo, peso, altura, nacionalidade)
VALUES
(DEFAULT, 'Bruna', '2002-10-25', 'F', 54, 1.69, 'Brasil');

-- Inserindo pessoa usando valor DEFAULT para nacionalidade
INSERT INTO pessoas
(nome, nascimento, sexo, peso, altura)
VALUES
('Pablo', '2023-07-20', 'M', 90, 1.50);
Consulta
sql

-- Consulta todos os registros da tabela `pessoas`
SELECT * FROM pessoas;
Exemplos visuais
<p align="center"> <img src="imagens/mysql_bruna.png" alt="Inserção de Bruna" width="400"/> </p> <p align="center"><em>Inserção de Bruna na tabela `pessoas`</em></p> <p align="center"> <img src="imagens/mysql_pablo.png" alt="Inserção de Pablo" width="400"/> </p> <p align="center"><em>Inserção de Pablo (com DEFAULT para nacionalidade)</em></p>

Próximos passos
Criar outras tabelas relacionadas (ex: enderecos, cursos, etc.)

Praticar joins: INNER JOIN, LEFT JOIN, RIGHT JOIN

Implementar chaves estrangeiras (foreign keys)

Normalização do banco: 1ª, 2ª, 3ª forma normal

Consultas mais complexas: filtros, ordenações, agrupamentos, funções agregadas

