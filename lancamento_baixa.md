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


