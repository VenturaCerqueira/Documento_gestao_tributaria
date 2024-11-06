![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Juros
Juros para acréscimos financeiros aplicados sobre valores devidos, geralmente em casos de atraso no pagamento de impostos, taxas ou outras obrigações fiscais. São calculados mensalmente com base em um percentual definido para cada competência.

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
02       | descricao*                   |                         | varchar(30)             | Descrição sobre tipo de juros.                                                       |  Descrição                             |
03       | competencia*                 |                         | date                    | Campo período fiscal ao qual a multa se refere.                                      |  Competência                           |
04       | percentual*                  |                         | decimal(15,2)           | Campo referente ao percentual da multa.                                              |  Percentual/mês                        |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |

                                                                 
  ↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/04%20-%20tipo_de_receita.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)    