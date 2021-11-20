# CARDINALIDADES
## Veja o esquema abaixo:
![cardinalidade](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/blob/main/imagens/cardinalidade1.png)
## Porque?
     Um aluno pode ter N notas.
     Um aluno pode ter N cursos.
     Um curso tem N alunos Matriculados.
     Um curso tem N notas relacionadas a ele.
     Uma nota só pode estar ligada a um único aluno.
     Uma nota só pode estar ligada a um punico curso.
## Para as cardinalidades de N para N temos que criar mais uma entidade:
![cardinalidade](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/blob/main/imagens/cardinalidade2.png)
## Como a entidade "notas" se relaciona com "alunos e Cursos" tendo apenas relação de 1 para N, Podemos relacionar "notas" somente com a nova entidade "aluno_cursos":
![cardinalidade](https://github.com/ERONILDOJUNIOR/SQL-introdu-o/blob/main/imagens/cardinalidade3.png)
