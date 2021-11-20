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
### Este código apaga a tabela "notas" completamente. Da mesmo forma é possivel apagar todo o banco de dados com o comando DROP, a seguir um exemplo:
```sql
DROP DATABASE cursos
```


