![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
## 🗺️ Cadastro - Países
### Cadastro de países usando os códigos ISO 3166.

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | pais                         |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
1        | nota_tomador                 |     1 - n     |
2        | contribuinte                 |     1 - n     |
3        | Tomador                      |     1 - n     | 
4        | nota_contribuinte            |     1 - n     |
#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                           | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|-----------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                         |                                        |
02       | nome                         |                         | varchar(100)            | Nome dos países.                                                                        |                                        |
03       | sigla2                       |                         | varchar(2)              | código de duas letras para identificar países é definido pela ISO 3166-1 alpha-2        |                                        |
04       | sigla3                       |                         | varchar(3)              | Sigla de três caracteres para identificar países é padronizada pela ISO 3166-1 alpha-3. |                                        |
05       | codigo                       |                         | varchar(10)             | Codificação ISO 3166-1 numeric.                                                         |                                        |
 