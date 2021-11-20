# Vamos começar nosso projeto?
## Primeiro precisamos criar nosso banco de dados chamado "curso", os comandos abaixo servem para este fim:
```sql
CREATE SCHEMA curso
```
## ou
```sql
CREATE DATABASE curso
```
## Vamos agora criar 3 tabelas: Alunos, Cursos e Notas. Elas teram apenas um único atributo que será nossa chave primária.
```sql
CREATE TABLE aluno(
id_aluno INT NOT NULL AUTO_INCREMENT ,
PRIMARY KEY (id_aluno)
);
```
```sql
CREATE TABLE cursos(
id_cursos INT NOT NULL AUTO_INCREMENT,
PRIMARY KEY (id_cursos)
);
```
```sql
CREATE TABLE notas(
id_notas INT NOT NULL AUTO_INCREMENT,
PRIMARY KEY (id_notas)
);
```
### Nossas chaves primarias não podem ser nulas e são autoincrementáveis. 
## Para fazer alterações nas tabelas e inserir novas colunas utilizaremos os comandos abaixo:
```sql
ALTER TABLE aluno
ADD COLUMN nome VARCHAR(100) NOT NULL AFTER id_aluno,
ADD COLUMN cpf VARCHAR(11) NOT NULL AFTER nome,
ADD COLUMN data_nascimento DATE NOT NULL AFTER cpf,
ADD COLUMN endereco VARCHAR(255)  NOT NULL AFTER data_nascimento,
ADD COLUMN cidade VARCHAR(100) NOT NULL AFTER endereco,
ADD COLUMN estado VARCHAR(2) NOT NULL AFTER cidade;
```
```sql
ALTER TABLE cursos
ADD COLUMN nome VARCHAR(50) NOT NULL AFTER id_cursos,
ADD COLUMN descrição VARCHAR(300) NOT NULL AFTER nome;
```
```sql
ALTER TABLE notas
ADD COLUMN nota FLOAT AFTER id_notas,
ADD COLUMN atividade VARCHAR(100) NOT NULL AFTER nota;
```
## Se for preciso excluir alguma tabela no meio do projeto use o seguinte código:
```sql
DROP TABLE notas
```
### Este código apaga a tabela "notas" completamente. 
## Da mesmo forma é possivel apagar todo o banco de dados com o comando DROP, a seguir um exemplo:
```sql
DROP DATABASE cursos
```
## Agora vamos povoar a tabela "aluno",usando os comandos abaixo:
```sql
INSERT INTO aluno VALUES 
(DEFAULT, 'Eronildo Junior', '10268457183','1998-02-26','General barreto de menezes, 80','Petrolina','PE'),
(DEFAULT, 'Ezequias Antunes', '54264527154','1998-06-17','Vital Brasil, 788','Remanso','BA'),
(DEFAULT, 'Evelyn Mariana', '55658882349','2002-12-21','Antonio de alencar sampaio, 321','Salgueiro','PE'),
(DEFAULT, 'Matheus dos Anjos','10336525698','1997-04-26','Veremundo soares, 10','Petrolina','PE'),
(DEFAULT, 'Matheus Passos', '54665885632','2003-01-14','Avenida Dantas Machado, 317B','Belo Horizonte','MG'),
(DEFAULT, 'Edwildson Rodrigues','6278193812', '1995-08-22','Avenida Barão do ouro preto, 820', 'Juazeiro', 'BA');
```

