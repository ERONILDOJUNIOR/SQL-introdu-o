# Banco de Dados - INTRODUÇÃO
### Introdução Banco de Dados
![banco](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/blob/main/imagens/5a54fd9f-bbc2-4e6c-a6b0-86d1e70390c6.jpg)
## O que são banco de dados?
São um conjunto de arquivos relacionados entre si com registros. 
São coleções organizadas de dados que fazem em conjunto um sentido trazendo informações.
Armazenam os dados de forma robusta, mantendo segurança e integridade dos dados.
## Tipos de Banco de Dados:
  ### Relacionais - 
    Definição simples: Dados relacionados entre si.
    Contexto: Usados geralmente em aplicações e por meio de tabelas relacionadas.
    Exemplos: PostgreeSQL, OracleSQL e MySQL.
  ### NoSQL       - 
    Definição Simples: Dados não relacionados entre si.
    Contexto: Usado geralmente em análise de dados como Data Science e Big Data. 
    Exemplos: MongoDB, Cassandra e CouchDB.
## Características de um banco de dados
  Bancos de dados devem executar procedimentos chamados de transações. A integridade de uma transação deve ser regida por quatro propriedades:
  ### Atomicidade   - 
    Todas as ações devem ser concluídas com sucesso, ou o processo falha como um todo e toda a ação é desfeita (rollback). 
    Se há sucesso em todas as ações a informação é mantida no banco (commit);
  ### Consistência  -
    Deve-se obedecer regras e restrições definidas em um banco, como por exemplo uso de chaves estrangeiras ou uso de campos únicos;
  ### Isolamento    - 
    Cada transação deve ser independente de outras transações;
  ### Durabilidade  -
    Os resultados de uma transação devem ser permanentes, exceto se outra transação a desfizer.
# SQL - INTRODUÇÃO
### Introdução a linguagem SQL
  ## Definição -
    Structured Query Language - é a linguagem usada para executar comandos em bancos de dados relacionais, baseado em tabelas. 
  ## Operações - 
    CRUD: Criate, Read, Update e Delete. São as operações base para se lidar com bancos de dados.
  ## Tipos de Comandos:
  ### DML - Linguagem de Manipulação de Dados: Permite manipulação de dados, como exclusão, inclusão e alterações. Exemplos de comandos:
    INSERT (permite adicionar dados)
    UPDATE (permite atualizar dados)
    DELETE (permite apagar dados)
  ### DDL - Linguagem de Definição de Dados: Permite a criação e alteração de dados. Exemplos de comandos:
    CREATE TABLE (cria tabelas)
    ALTER TABLE (altera tabelas)
    DROP TABLE (apaga tabelas).
  ### DQL - Linguagem de Consulta de Dados: Permite a realização de buscas nas tabelas dos bancos de dados. Exemplo de comando:
     SELECT (comando mais importante usado para realizar buscas)
## Vamos falar um pouco sobre bancos relacionais?
[Introdução Bancos Relacionais](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/edit/main/AULAS/IntroduçãoBancosRelacionais.md)
