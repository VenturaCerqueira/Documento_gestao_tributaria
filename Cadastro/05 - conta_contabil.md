# e-contrib - Modelo e-2025 
##  Cadastro - Conta contábil 
### 

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
02       | fK_receita_tipo*             | receita_tipo            | bigint(20)              |                                                                                      | Tipo de receita                        |
03       | codigo*                      |                         | varchar(50)             |                                                                                      | Código                                 |
04       | descricao*                   |                         | varchar(200)            |                                                                                      | Descrição                              |
05       | sigla*                       |                         | varchar(10)             |                                                                                      | Sigla                                  |


# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |

