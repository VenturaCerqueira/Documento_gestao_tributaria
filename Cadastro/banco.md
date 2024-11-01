# e-contrib - Modelo e-2025 
## 🏦 Cadastro - Banco  
### Armazenamento dos dados bancários para pagamentos dos DAM's.

# Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | banco                        |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
1        | lancamento_baixa             |     1 - n     |
2        | retorno_banco                |     1 - n     |

#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
1        | lancamento                   |     n - 1     |
2        | contribuinte_receita         |     n - 1     |



# Regras:
 **\#**  |**Nome**                      |   **Descrição**                                               |
---------|------------------------------|---------------------------------------------------------------|      
1        | Regra_unique_banco           |  *Codigo* e *nome* deve-se unico.                             |



#  Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      | 
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome *                       |                         | Varchar(100)            | Nome do banco.                                                                       | Nome                                   |
03       | codigo *                     |                         | varchar(5) UN           | Código do banco padrão Febraban                                                      | Código                                 |
04       | cod_contabil                 |                         | Varchar(30)             | Código da conta contabil.                                                            | Código contábil                        |
05       | cod_agencia                  |                         | Varchar(20)             | Código da Agência.                                                                   | Código agência                         |
06       | cod_conta                    |                         | Varchar(20)             | Código da Conta com digito, sem hífen.                                               | Código conta                           |
07       | numero_convenio              |                         | Int                     | Número do convenio do municipio no banco.                                            | Código banco Siafic                    | 
08       | chave_pix                    |                         | Varchar(100)            | Chave de segurança fornecida do banco chave pix.                                     ||
09       | client_id                    |                         | Varchar(255)            | Chave de segurança fornecida do banco chave pix.                                     || 
10       | client_secret                |                         | Varchar(255)            | Chave de segurança fornecida do banco chave pix.                                     ||
11       | app_key                      |                         | Varchar(255)            | Chave de segurança do Banco do Brasil com API.                                       ||
12       | cod_banco_siafic             |                         | Varchar(5)              | Código do banco para o SIAFIC. (nota-1)                                              ||

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | Excluir                      |               |

# ⚠️ Notas: 

        1- Quando cod_banco_siafic estiver preenchido, ele sera usado no envio ao SIAFIC, senão o campo codigo enviado.       

# 📄 Mensagem de erros/advertências: 

