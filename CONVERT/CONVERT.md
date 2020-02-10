
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
  
|  Formato  |  Query  |  Resultado  |
| ---: | :---: | ---: |
|  1 |  `SELECT CONVERT(varchar, GETDATE(), 1)` | 02/10/2020 |
|  2 |  `SELECT CONVERT(varchar, GETDATE(), 2)` | 20.02.10 |
|  3 |  `SELECT CONVERT(varchar, GETDATE(), 3)` | 10/02/2020 |
|  4 |  `SELECT CONVERT(varchar, GETDATE(), 4)` | 10.02.20 |
|  5 |  `SELECT CONVERT(varchar, GETDATE(), 5)` | 10/02/2020 |
|  6 |  `SELECT CONVERT(varchar, GETDATE(), 6)` | 10 Feb 20 |
|  7 |  `SELECT CONVERT(varchar, GETDATE(), 7)` | Feb 10, 20 |
| 10 |  `SELECT CONVERT(varchar, GETDATE(), 7)` | 02/10/2020 |
| 11 |  `SELECT CONVERT(varchar, GETDATE(), 7)` | 20/02/2010 |
| 12 |  `SELECT CONVERT(varchar, GETDATE(), 7)` | 200210 |

</p>

[mssqltips](https://www.mssqltips.com/sqlservertip/1145/date-and-time-conversions-using-sql-server/)
