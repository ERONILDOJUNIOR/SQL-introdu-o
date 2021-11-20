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
