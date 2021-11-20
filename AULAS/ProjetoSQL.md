# Vamos começar nosso projeto?
## Primeiro precisamos criar nosso banco de dados chamado "curso", os comandos abaixo servem para este fim:
```sql
CREATE SCHEMA curso
```
## ou
```sql
CREATE DATABASE curso
```
### Comando acima cria um banco de dados chamado "curso".
## Vamos agora criar 3 tabelas: Alunos, Cursos e Notas. Elas terão apenas um único atributo que será nossa chave primária.
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
### O comando "CREATE TABLE" é usado para criar as tabelas. O comando "INT" determina que o atributo "id" é um inteiro, o comando "NOT NULL" determina que não pode ser nula e o comando "AUTO_INCREMENT" determina que esses valores serão auto incrementados.
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
### O comando "ALTER TABLE" possibilita a alteração de uma tabela, Já o comando "ADD COLUMN" torna possivel adicionar uma coluna á tabela. Ao adicionar colunas é preciso determinar seu tipo, e em alguns casos colocar restrições como a impossibilidade de ser nula, também é possivel determinar onde a coluna será adicionada através do comando "AFTER", no caso a coluna será adicionada "depois" da coluna referenciada.  
## Se for preciso excluir alguma tabela no meio do projeto use o seguinte código:
```sql
DROP TABLE notas
```
### Este código apaga a tabela "notas" completamente. Muito cuidado com esse tipo de instrução.
## Da mesmo forma é possivel apagar todo o banco de dados com o comando DROP, a seguir um exemplo:
```sql
DROP DATABASE cursos
```
### Esse tipo de instrução pode trazer danos irreversíveis para todo o banco.
## Agora vamos povoar a tabela "aluno",usando o comando abaixo:
```sql
INSERT INTO aluno VALUES 
(DEFAULT, 'Eronildo Junior', '10268457183','1998-02-26','General barreto de menezes, 80','Petrolina','PE'),
(DEFAULT, 'Ezequias Antunes', '54264527154','1998-06-17','Vital Brasil, 788','Remanso','BA'),
(DEFAULT, 'Evelyn Mariana', '55658882349','2002-12-21','Antonio de alencar sampaio, 321','Salgueiro','PE'),
(DEFAULT, 'Matheus dos Anjos','10336525698','1997-04-26','Veremundo soares, 10','Petrolina','PE'),
(DEFAULT, 'Matheus Passos', '54665885632','2003-01-14','Avenida Dantas Machado, 317B','Belo Horizonte','MG'),
(DEFAULT, 'Edwildson Rodrigues','6278193812', '1995-08-22','Avenida Barão do ouro preto, 820', 'Juazeiro', 'BA');
```
### Com os comando "INSERT INTO" inserimos novas linhas a tabela, o comando "VALUES" é seguido por um par de parenteses "()", dentro deles teremos as informações para serem armazenadas nas tabelas, essas informações devem estar na ordem das colunas e separadas por virgula ",". Perceba que o primeiro parâmetro é passado como "DEFAULT", isso porque o "id" é uma chave primária que tem auto incremento, logo o próprio SGBD faz a distribuição desses IDs, Mas ainda sim é possivel setar um id específico.  
## Para verificar se a tabela está povoada execute o comando abaixo:
```sql
SELECT * FROM curso.aluno
```
### O comando "SELECT" é usado para selecionar, após ele vem uma descrição do que selecionar, como o parâmetro foi " * " tudo será selecionado (todas as colunas), O comando "FROM" diz onde será a seleção, no nosso caso no banco "curso" na tabela "aluno". Deverá aparecer para você algo semelhante a isto:
![tabela1](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/blob/main/imagens/tabela1.png)
## Ao olhar a tabela é possivel identificar que o campo "cpf" de EDWILDSON está faltando um digito, o valor correto seria "62781938125", para fazer atualização desse tipo teremos os seguintes comandos:
```sql
UPDATE aluno
SET cpf='62781938125'
where id_aluno = 6;
```
### Aqui o comando "UPDATE" faz atualização e "seta" o cpf correto onde o "id_aluno" é igual a 6. A nova tabela terá essa cara, perceba a mudança no cpf de EDWILDSON:
![tabela1](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/blob/main/imagens/tabela2.png)
