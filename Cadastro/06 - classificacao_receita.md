↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20receitas.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/07%20-%20receita_tipo.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Classificação receita


# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | receita_classificacao        |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | conta_contabil               |     1 - N     |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | indice_financeiro            |     1 - 1     |
02       | juros                        |     1 - 1     |
03       | multa                        |     1 - 1     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_conta_contabil *          | conta_contabil          | bigint(20)              |                                                                                      | Conta contábil                         |
03       | descricao *                  |                         | varchar(100)            |                                                                                      | Descrição                              |
04       | unidade *                    |                         | tinyint(3)              |                                                                                      | Unidade                                |
05       | periodo *                    |                         | tinyint(4)              |                                                                                      | Periodicidade                          |
06       | avulso *                     |                         | tinyint(3)              |                                                                                      | Avulso                                 |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | excluir                      |               |


↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20conta_contabil.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/07%20-%20receitas.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 
