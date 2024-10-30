# e-contrib - Modelo e-2024 
## Informações banco/ retorno bancario / lançamento baixa

# Tabela de resumo dos cadastros
 **\#**  | **Referencia**                    | **Tabela**              | **Versão Layout**       | **Descrição**                                                                                                                                                   |
---------|-----------------------------------|-------------------------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
01       | Registro bancario                 | banco                   |   e-1.0/2024            | Armazenamento dos dados bancários, campos de integração com SIAFIC , incluso cadastro das chave Pix e credenciais para API.<br> - **Cadastro de Bancos:** <br> 01 - nome; <br> 02 - Código;<br> 03 - Código contábil;<br> 04 - Código agência;<br> 05 - Código conta;<br> 06 - Código banco Siafic;   | 
02       | Retorno  bancario| retorno_banco| e-1.0/2024 | 



# Tabela de banco
 **\#**  | **Coluna**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome                         |                         | Varchar(100)            |                                                                                      | Nome - campo obrigatórios              |
03       | codigo                       |                         | varchar(5)              |                                                                                      | Código - campo obrigatórios            |
04       | Cod_contabil                 |                         | Varchar(30)             |                                                                                      | Código contábil                        |
05       | Cod_agencia                  |                         | Varchar(20)             |                                                                                      | Código agência                         |
06       | Cod_conta                    |                         | Varchar(20)             |                                                                                      | Código conta                           |
07       | numero_convenio              |                         | Int                     |                                                                                      | Código banco Siafic                    | 
08       | chave_pix                    |                         | Varchar(100)            |                                                                                      ||
09       | client_id                    |                         | Varchar(255)            |                                                                                      || 
10       | Client_secret                |                         | Varchar(255)            |                                                                                      ||
11       | app_key                      |                         | Varchar(255)            |                                                                                      ||
12       | cod_banco_siafic             |                         | Varchar(5)              |                                                                                      ||
13       | created_at                   |                         | timestamp               |                                                                                      ||
14       | update_at                    |                         | timestamp               |                                                                                      ||


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

# Registro do Lançamentos das baixas - lancamento_baixa 
 **\#**  | **Coluna**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|
01       | id                           |                         | bigint(20) UN AI PK     | |
02       | fk_lancamento_cota           | lancamento_cota         | bigint(20) FK NN UN     | |
03       | fk_banco                     | banco                   | bigint(20) FK NN UN     | |
04       | fk_modalidade                | modalidade              | bigint(20) FK NN UN     | |
05       | fk_usuario                   | users                   | bigint(20) FK NN UN     | |
06       | fk_usuario_situacao          | users                   | bigint(20) FK NN UN     | |
07       | valor_pagamento              |                         | Decimal(15,2) NN        | |
08       | data_lancamento              |                         | datetime                | |
09       | data_credito                 |                         | date                    | |
10       | data_extincao                |                         | date                    | |
11       | data_situacao                |                         | datetime                | |
12       | valor_tarifa                 |                         | decimal(15,2)           | |
13       | motivo                       |                         | Varchar(255)            | |
14       | agencia_arrecadadora         |                         | Varchar(8)              | |
15       | canal_recebuimento           |                         | Varchar(1)              | |
16       | numero_autenticacao          |                         | Varchar(30)             | |
17       | codigo_barras                |                         | Varchar(44)             | |
18       | historico                    |                         | Varchar(255)            | |
19       | situacao                     |                         | char(1)       NN        | |
20       | created_at                   |                         | timestamp               | |
21       | update_at                    |                         | timestamp               | |




