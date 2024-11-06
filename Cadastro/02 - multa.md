![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Multa  
### Cadastro das multas aplicado para calculo no DAM's, podendo cadastrar prazo inicial, prazo final e porcentual sobre-as.

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       |  multa                       |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | receita_tipo                 |      1 - n    |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | descricao                    |                         | varchar(30)             | Campo texto sobre a natureza da multa.                                               |  Descrição                             |
03       | competencia                  |                         | Date                    | Campo período fiscal ao qual a multa se refere.                                      |  Competência                           |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | view                         |               |
3        | excluir                      |               |

