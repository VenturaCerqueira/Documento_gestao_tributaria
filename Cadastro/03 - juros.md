![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Juros
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | juros                        |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | receita_tipo                 |     1 - n     |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | descricao*                   |                         | varchar(30)             |                                                                                      |  Descrição                             |
03       | competencia*                 |                         | date                    |                                                                                      |  Competência                           |
04       | percentual*                  |                         | decimal(15,2)           |                                                                                      |  Percentual/mês                        |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |

# Ações / botões:
                                                                 
  [Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)   