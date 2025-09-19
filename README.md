# Estudos em MySQL

Este repositório contém scripts e exemplos práticos do meu aprendizado em **SQL** e **bancos de dados relacionais**.

## Estrutura
- `scripts/` → Scripts SQL de criação, inserção e consulta
- `imagens/` → Prints do MySQL Workbench com os resultados das queries
- `README.md` → Documentação do projeto

## Exemplos
Criação da tabela `pessoas`:
```sql
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
Inserindo registros:

insert into pessoas
(id, nome, nascimento, sexo, peso, altura, nacionalidade)
values
(DEFAULT, 'Bruna', '2002-10-25', 'F', 54, 1.69, 'Brasil');
![Exemplo de consulta](imagens/mysql_bruna.png)

Objetivo

Este repositório faz parte do meu portfólio, documentando meu aprendizado em MySQL e servindo como base para projetos futuros.

---
