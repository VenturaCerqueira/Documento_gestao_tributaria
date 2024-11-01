# e-contrib - Modelo e-2025 
##  Cadastro - Idice Financeiro  
### Lista de item de serviço seguinte Lei 116/
https://www.planalto.gov.br/ccivil_03/leis/lcp/lcp116.htm

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | iten_servico                 |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
1        | cnae_item_servico            |     1 - n     |
2        | Contribuinte_juridico        |     1 - n     |
3        | nota_contribuinte            |     1 - n     |
4        | nota                         |     1 - n     |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome                         |                         | varchar(100)            |                                                                                      |  Código                                |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |

