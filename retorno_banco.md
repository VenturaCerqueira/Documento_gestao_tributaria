# Registro do retorno bancario - retorno_banco 
 **\#**  | **Coluna**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|
01       | id                           |                         | bigint(20) UN AI PK     | |
02       | fk_usuario                   | users (id)              | bigint(20) NN UN        | |
03       | fk_banco                     | banco (id)              | bigint(20) NN UN        | |
04       | data_processamento           |                         | Datetime not null       | |
05       | data_geracao_arquivo         |                         | date                    | |
06       | nsa                          |                         | int                     | |
07       | nome_arquivo                 |                         | varchar(100)            | |
08       | created_at                   |                         | timestamp               | |
09       | update_at                    |                         | timestamp               | |