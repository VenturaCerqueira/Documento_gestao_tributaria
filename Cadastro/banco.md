# e-contrib - Modelo e-2024 
## 🏦 Cadastro - Banco 

# Tabela de resumo dos cadastros
 **\#**  | **Referencia**                    | **Tabela**              | **Resumo**                                                                                                                                                   |
---------|-----------------------------------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
01       | Registro bancario                 | banco                   | Armazenamento dos dados bancários, campos de integração com SIAFIC , incluso cadastro das chave Pix e credenciais para API.<br>  **- View:** <br> 01 - nome; <br> 02 - Código;<br> 03 - Código contábil;<br> 04 - Código agência;<br> 05 - Código conta;<br> 06 - Código banco Siafic;   | 
02       | Lancamento da baixa               | lancamento_baixa        | Tabela dependente, contém a chave estrangeira fk_banco vinculada a lancamento_baixa, utilizada no processo de baixa da cota.                           |
03       |  Retorno do banco                 | retorno_banco           | Tabela com dependência na chave estrangeira fk_banco, vinculada a retorno_banco, utilizada no processamento de retorno bancário.| 
# Tabela de banco
 **\#**  | **Coluna**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome                         |                         | Varchar(100)            |                                                                                      | Nome - Campo obrigatórios              |
03       | codigo                       |                         | varchar(5) UN           |                                                                                      | Código - Campo obrigatórios            |
04       | Cod_contabil                 |                         | Varchar(30)             | **Regra banco:** Codigo deve-se unico                                                | Código contábil                        |
05       | Cod_agencia                  |                         | Varchar(20)             | Código da Agência SIAFIC.                                                            | Código agência                         |
06       | Cod_conta                    |                         | Varchar(20)             | Código da Conta SIAFIC.                                                              | Código conta                           |
07       | numero_convenio              |                         | Int                     |                                                                                      | Código banco Siafic                    | 
08       | chave_pix                    |                         | Varchar(100)            | Chave de segurança fornecida do banco chave pix.                                     ||
09       | client_id                    |                         | Varchar(255)            | Chave de segurança fornecida do banco chave pix.                                     || 
10       | Client_secret                |                         | Varchar(255)            | Chave de segurança fornecida do banco chave pix.                                     ||
11       | app_key                      |                         | Varchar(255)            | Chave de segurança do Banco do Brasil com API.                                       ||
12       | cod_banco_siafic             |                         | Varchar(5)              | **Validação:** <br> Quando **cod_banco_siafic** estiver preenchido, ele deve ser usado no envio ao SIAFIC, ignorando o valor da coluna **codigo**.<br><br>Caso **cod_banco_siafic** estiver **"null"**, o campo codigo enviado normalmente.       ||



