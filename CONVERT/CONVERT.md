
<p align="center">
  <img src="https://d1.awsstatic.com/logos/partners/microsoft/logo-SQLServer-vert.c0cb0df0cd1d6c8469d792abb5929239da36611a.png">
</p>

# CONVERT Function

## A função

 A função `CONVERT` serve basicamente para alternar entre tipos em um valor informado.

## A sintaxe

A sintaxe do comando `CONVERT` consiste em:

>```sql
> 
>  CONVERT(tipo_dado, expressao, estilo)
>
>```

## Exemplos

>
>```sql
> 
>  SELECT CONVERT(int, 25.65);
>
>```

`>> 25`

>
>```sql
> 
>  SELECT CONVERT(varchar, 25.65);
>
>```

`>> "25.65"`

## CONVERT com tipos de Data

É comum utilizar o comando `CONVERT` para alterar o retorno de um valor tipo `data`.

Os exemplos a seguir utilizaram a data "10/02/2020 14:22:41:907" como base.

<p align="center">
  
### Formatos Somente Data
  
|  Formato  |                    Query                   |   Resultado  |
| --------: | :----------------------------------------: | -----------: |
|         1 |  `SELECT CONVERT(varchar, GETDATE(), 1)`   |   02/10/2020 |
|         2 |  `SELECT CONVERT(varchar, GETDATE(), 2)`   |     20.02.10 |
|         3 |  `SELECT CONVERT(varchar, GETDATE(), 3)`   |   10/02/2020 |
|         4 |  `SELECT CONVERT(varchar, GETDATE(), 4)`   |     10.02.20 |
|         5 |  `SELECT CONVERT(varchar, GETDATE(), 5)`   |   10/02/2020 |
|         6 |  `SELECT CONVERT(varchar, GETDATE(), 6)`   |    10 Feb 20 |
|         7 |  `SELECT CONVERT(varchar, GETDATE(), 7)`   |   Feb 10, 20 |
|        10 |  `SELECT CONVERT(varchar, GETDATE(), 10)`  |   02/10/2020 |
|        11 |  `SELECT CONVERT(varchar, GETDATE(), 11)`  |   20/02/2010 |
|        12 |  `SELECT CONVERT(varchar, GETDATE(), 12)`  |       200210 |
|        23 |  `SELECT CONVERT(varchar, GETDATE(), 23)`  |   10/02/2020 |
|       101 |  `SELECT CONVERT(varchar, GETDATE(), 101)` |   02/10/2020 |
|       102 |  `SELECT CONVERT(varchar, GETDATE(), 102)` |   2020.02.10 |
|       103 |  `SELECT CONVERT(varchar, GETDATE(), 103)` |   10/02/2020 |
|       104 |  `SELECT CONVERT(varchar, GETDATE(), 104)` |   10.02.2020 |
|       105 |  `SELECT CONVERT(varchar, GETDATE(), 105)` |   10/02/2020 |
|       106 |  `SELECT CONVERT(varchar, GETDATE(), 106)` |  10 Feb 2020 |
|       107 |  `SELECT CONVERT(varchar, GETDATE(), 107)` | Feb 10, 2020 |
|       110 |  `SELECT CONVERT(varchar, GETDATE(), 107)` |   02/10/2020 |
|       111 |  `SELECT CONVERT(varchar, GETDATE(), 107)` |   10/02/2020 |
|       112 |  `SELECT CONVERT(varchar, GETDATE(), 107)` |     20200210 |

### Formatos Somente Horário
  
|  Formato  |                    Query                   |   Resultado  |
| --------: | :----------------------------------------: | -----------: |
|         8 |  `SELECT CONVERT(varchar, GETDATE(), 8)`   |     14:22:41 |
|        14 |  `SELECT CONVERT(varchar, GETDATE(), 14)`  | 14:22:41:907 |
|        24 |  `SELECT CONVERT(varchar, GETDATE(), 24)`  |     14:22:41 |
|       108 |  `SELECT CONVERT(varchar, GETDATE(), 108)` |     14:22:41 |
|       114 |  `SELECT CONVERT(varchar, GETDATE(), 114)` | 14:22:41:907 |

### Formatos Data e Horário
  
|  Formato  |                    Query                   |            Resultado         |
| --------: | :----------------------------------------: | ---------------------------: |
|         0 |  `SELECT CONVERT(varchar, GETDATE(), 0)`   |          Feb 10 2020  2:22PM |
|         9 |  `SELECT CONVERT(varchar, GETDATE(), 9)`   |   Feb 10 2020  2:22:41:907PM |
|        13 |  `SELECT CONVERT(varchar, GETDATE(), 13)`  |     10 Feb 2020 14:22:41:907 |
|        20 |  `SELECT CONVERT(varchar, GETDATE(), 20)`  |             10/02/2020 14:22 |
|        21 |  `SELECT CONVERT(varchar, GETDATE(), 21)`  |      2020-02-10 14:22:41.907 |
|        22 |  `SELECT CONVERT(varchar, GETDATE(), 22)`  |             02/10/2020 14:22 |
|        25 |  `SELECT CONVERT(varchar, GETDATE(), 25)`  |      2020-02-10 14:22:41.907 |
|       100 |  `SELECT CONVERT(varchar, GETDATE(), 100)` |          Feb 10 2020  2:22PM |
|       109 |  `SELECT CONVERT(varchar, GETDATE(), 109)` |   Feb 10 2020  2:22:41:907PM |
|       113 |  `SELECT CONVERT(varchar, GETDATE(), 113)` |     10 Feb 2020 14:22:41:907 |
|       120 |  `SELECT CONVERT(varchar, GETDATE(), 120)` |             10/02/2020 14:22 |
|       121 |  `SELECT CONVERT(varchar, GETDATE(), 121)` |      2020-02-10 14:22:41.907 |
|       126 |  `SELECT CONVERT(varchar, GETDATE(), 126)` |      2020-02-10T14:22:41.907 |
|       127 |  `SELECT CONVERT(varchar, GETDATE(), 127)` |      2020-02-10T14:22:41.907 |


### Formatos de Calendário Islâmico
  
|  Formato  |                    Query                   |              Resultado            |
| --------: | :----------------------------------------: | --------------------------------: |
|       130 |  `SELECT CONVERT(varchar, GETDATE(), 130)` |   16 جمادى الثانية 1441  2:22:41 |
|       131 |  `SELECT CONVERT(varchar, GETDATE(), 131)` |         16/06/1441  2:22:41:907PM |


</p>

[mssqltips](https://www.mssqltips.com/sqlservertip/1145/date-and-time-conversions-using-sql-server/)
