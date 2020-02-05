


<p align="center">
  <img src="https://d1.awsstatic.com/logos/partners/microsoft/logo-SQLServer-vert.c0cb0df0cd1d6c8469d792abb5929239da36611a.png">
</p>

# UNPIVOT function

## A função

A função `UNPIVOT` serve basicamente para transformar colunas em linhas em alguma determinada tabela.

## A sintaxe

A sintaxe do comando `UNPIVOT` consiste em:


>```sql 
>     
>UNPIVOT  
>(
>
>   nova_coluna FOR x IN (col1, col2, col3, col4, col5)  
>
>) AS alias;  
>      
>```

## Exemplo

Se tivermos uma tabela com a seguinte estrutura:

<p align="center">
  <img src="https://codingsight.com/wp-content/uploads/2018/04/unpivot-operator.png">
</p>

E utilizarmos o `UNPIVOT` nas colunas "Math", "English", "History", "Science" com o código:

>```sql 
>     
>SELECT StudentName,
>        Course, 
>        Score
>
>FROM Students
>UNPIVOT
>(
>
>	Score FOR Course in (Math, English, History, Science)
>
>) AS SchoolUnpivot
>      
>```

Iremos obter a seguinte tabela:

<p align="center">
  <img src="https://codingsight.com/wp-content/uploads/2018/04/6.png">
</p>

><br>
>Nota: Note que as colunas "Math", "English", "History", "Science" viraram linhas da nova coluna criada "Score"<br>
><br>

[CodingSight](https://codingsight.com/understanding-pivot-unpivot-and-reverse-pivot-statements/)<br>
[Microsoft Dosc](https://docs.microsoft.com/pt-br/sql/t-sql/queries/from-using-pivot-and-unpivot?view=sql-server-ver15)
