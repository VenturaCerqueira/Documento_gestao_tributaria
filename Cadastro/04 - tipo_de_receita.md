↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/03%20-%20juros.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20conta_contabil.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Tipo de receita 
Cadastro de **receitas tributárias**, incluindo exemplos como **impostos, taxas** e **contribuições**. Essas receitas têm fundamento legal na Constituição e em leis específicas. O cadastro também inclui informações sobre o índice financeiro, a taxa de juros, a multa aplicável e a natureza jurídica de cada receita, indicando se é **tributária** ou **não tributária**.  

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | receita_tipo                 |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | conta_contabil               |     1 - N     |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | indice_financeiro            |     1 - 1     |
02       | juros                        |     1 - 1     |
03       | multa                        |     1 - 1     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_indice                    | indice_financeiro       | bigint(20)              | Campo referente ao tipo de índice financeiro cadastrado.                             | Índice                                 |
03       | fk_multa*                    | multa                   | bigint(20)              | Campo referente a multa para receita.                                                | Multa                                  |
04       | fk_juros*                    | juros                   | bigint(20)              | Campo referente ao tipo do juros da receita.                                         | Juros                                  |
05       | descricao*                   |                         | varchar(100)            | Nome das receitas tributárias.                                                        | Descrição                              |   
06       | natureza*                    |                         | tinyint(3)              | Referente ao tipo de naturaza juridca do tributos. <br> **Valores válidos:** <br> 1 - Tributária; <br> 2 - Não tributária;                                                                                  | Natureza                               |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Excluir                      |               |


# Observação:
    Apenas cadastros acima de 10 são permitidos excluir. 

↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/03%20-%20juros.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20conta_contabil.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  