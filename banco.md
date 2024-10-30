# e-contrib - Modelo e-2024 
## Informações banco/ retorno bancario / lançamento baixa

# Tabela de resumo dos cadastros
 **\#**  | **Referencia**                    | **Tabela**              | **Versão Layout**       | **Descrição**                                                                                                                                                   |
---------|-----------------------------------|-------------------------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
01       | Registro bancario                 | banco                   |   e-1.0/2024            | Armazenamento dos dados bancários, campos de integração com SIAFIC , incluso cadastro das chave Pix e credenciais para API.<br> - **Cadastro de Bancos:** <br> 01 - nome; <br> 02 - Código;<br> 03 - Código contábil;<br> 04 - Código agência;<br> 05 - Código conta;<br> 06 - Código banco Siafic;   | 


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
12       | cod_banco_siafic             |                         | Varchar(5)              | **Validação:** <br> Quando **cod_banco_siafic** estiver preenchido, ele deve ser usado no envio ao SIAFIC, ignorando o valor da coluna **codigo**.<br><br>Caso **cod_banco_siafic** estiver **"null"**, o campo codigo enviado normalmente.       ||
13       | created_at                   |                         | timestamp               |                                                                                      ||
14       | update_at                    |                         | timestamp               |                                                                                      ||


