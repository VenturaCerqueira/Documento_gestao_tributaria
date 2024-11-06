![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Conta contábil 
Cadastro de conta contábil com classificação detalhada, incluindo código contábil, abreviação do tributo, descrição completa e tipo de receita. Cada tributo é categorizado por tipo de receita, como impostos, taxas e outras receitas.
# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | conta_contabil               |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | lancamento                   |     1 - N     |
02       | receita_classificacao        |     1 - N     |


#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | receita_tipo                 |     1 - N     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fK_receita_tipo*             | receita_tipo            | bigint(20)              | Código *"id"* da tabela *tipo_receita*.                                              | Tipo de receita                        |
03       | codigo*                      |                         | varchar(50)             | Código da conta contabil.                                                            | Código                                 |
04       | descricao*                   |                         | varchar(200)            | Detalhamento da conta contabil, descrevendo natureza.                                | Descrição                              |
05       | sigla*                       |                         | varchar(10)             | Sgila do tributo, exemplos: IPTU, TFF e outras abreviações.                          | Sigla                                  |


# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |

↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/04%20-%20tipo_de_receita.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/06%20-%20classificacao_receita.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  