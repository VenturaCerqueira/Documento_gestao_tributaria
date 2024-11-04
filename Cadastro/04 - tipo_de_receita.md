# e-contrib - Modelo e-2025 
##  Cadastro - Tipo de receita 
### 

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
02       | fk_indice                    | indice_financeiro       | bigint(20)              |                                                                                      | Índice                                 |
03       | fk_multa*                    | multa                   | bigint(20)              |                                                                                      | Multa                                  |
04       | fk_juros*                    | juros                   | bigint(20)              |                                                                                      | Juros                                  |
05       | descricao*                   |                         | varchar(100)            |                                                                                      | Descrição                              |   
06       | natureza*                    |                         | tinyint(3)              |                                                                                      | Natureza                               |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Excluir                      |               |


# Observação:
    Apenas cadastros acima de 10 são permitidos excluir. 