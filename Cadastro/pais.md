# e-contrib - Modelo e-2024 
## Informações Pais

# Tabela de resumo dos cadastros
 **\#**  | **Referencia**                    | **Tabela**              | **Versão Layout**       | **Descrição**                                                                                                                                                   |
---------|-----------------------------------|-------------------------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
01       | Cadastro de pais                  | pais                    |   e-1.0/2024            | | 


# Tabela de Pais
 **\#**  | **Coluna**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome                         |                         | varchar(100)            |                                                                                      |                                        |
03       | sigla2                       |                         | varchar(2)              | código de duas letras para identificar países é definido pela ISO 3166-1 alpha-2     |                                        |
04       | sigla3                       |                         | varchar(3)              | Sigla de três caracteres para identificar países é padronizada pela ISO 3166-1 alpha-3.|                                      |
05       | codigo                       |                         | varchar(10)             | Codificação ISO 3166-1 numeric.                                                      |                                        |
 