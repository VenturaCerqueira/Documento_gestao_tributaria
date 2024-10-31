# e-contrib - Modelo e-2024 
## Informações veiculo

# Tabela de resumo dos cadastros
 **\#**  | **Referencia**                    | **Tabela**              | **Versão Layout**       | **Descrição**                                                                                                                                                   |
---------|-----------------------------------|-------------------------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
01       | Cadastro de Veiculo               | Veiculo                 |   e-1.0/2024            |                                                                                                                 | 


# Tabela de Veiculo
 **\#**  | **Coluna**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_proprietario              | contribuinte            | BIGINT(20) UN           | Contribuinte dono veiculo.                                                           |                                        | 
03       | fk_condutor                  | contribuinte            | BIGINT(20) UN           | Contribuinte condutor do veiculo, podendo ser diferente do proprietario.             |                                        | 
04       | fk_marca                     | veiculo_marca           | BIGINT(20)UN            |                                                                                      |                                        |                      
05       | placa                        |                         | varchar(12)             |                                                                                      |                                        |   
06       | renavam                      |                         | varchar(30)             |                                                                                      |                                        |
07       | chassi                       |                         | varchar(30)             |                                                                                      |                                        |
08       | modelo                       |                         | varchar(100)            |                                                                                      |                                        |
09       | ano_modelo                   |                         | varchar(4)              |                                                                                      |                                        |
10       | cor                          |                         | varchar(20)             |                                                                                      |                                        |
11       | responsavel                  |                         | varchar(100)            | **Remover coluna**                                                                   |                                        |
12       | status                       |                         | tinyint                 |                                                                                      |                                        |   

