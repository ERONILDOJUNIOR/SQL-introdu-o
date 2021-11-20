# Bancos Relacionais
## Estudo de casos : Criação de um banco.
Imagine que Você foi contratado para criar um banco de dados que armazene informações sobre uma escola que vende cursos.
Para esse projeto será preciso armazenar os dados dos alunos (Nome, data de nascimento, CPF e endereço).
Os alunos podem se matricular em cursos e ter suas respectivas notas baseadas em atividades.

## Definindo entidades: Uma entidade é uma representação de um conjunto de informações sobre determinado conceito do sistema.
### Entidade Aluno  - 
      *Nome
      *CPF
      *Endereço
      *Data de nascimento
### Entidade Curso  - 
      *Nome
### Entidade Nota   - 
      *Atividade
      *Nota
## Definindo relacionamentos: Como as entidades se relacionam entre si.
### Alunos  - 
      Podem fazer vários cursos e terão notas pra cada um deles.
### Cursos  - 
      Podem ser feitos por diversos alunos.
### Nota    - 
      Estão atreladas a um aluno e um curso.
## Chaves primarias: Termo usado pra identificar exclusivamente um campo das tabbelas geradas (identificador).
### Chave primária é usada pra fazer ligação entre duas entidades distintas e criar um relacionamento. 
## Tipos de dados
### Numéricos  -
      Inteiros: 
          TINYINT   - Inteiro muito peuqueno.
          SMALLINT  - Inteiro Pequeno.
          MEDIUMINT - Inteuiro mediano.
          INT       - Inteiro (Padrão).
          BIGINT    - Interiro grande.
      Decimais:
          DECIMAL   - Decimal de ponto fixo.
          FLOAT     - Número de ponto flutuante precisão simples(32bits).
          DOUBLE    - Número de pnoto flutuante prcisão dupla(64bits).
### Texto      -
          CHAR      - Cadeia de caracteres de tamanho determinado.
          VARCHAR   - Cadeia de caracteres de tamanha não determinado.
          TEXT      - Cadeia de caracteres não binária e pequena.
### Data       -
          DATE      - Valor referênte a uma data "YYYY-MM-DD".
          TIME      - Valor referente a uma hora "hh:mm:ss".
          DATETIME  - Valor referente a uma data e uma hora "YYYY-MM-DD hh:mm:ss" . 
## Agora vamos trabalhar com CARDINALIDADE: 
![Introdução Cardinalidade](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/blob/main/AULAS/Cardinalidade.md)
