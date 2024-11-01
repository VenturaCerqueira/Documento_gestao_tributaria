# e-contrib - Modelo e-2025 
## 🗺️ Cadastro - Cidade
### Cadastro de bairros.

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | bairro                       |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
2        | imovel                       |               |
3        | logradouro                   |               |
4        | loteamento                   |               |
5        | contribuinte                 |               |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
1        | cidade                       |     1 - n     |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_cidade                    | cidade                  | bigint UN               |                                                                                      |                                        |
03       | nome                         |                         | varchar(100)            |                                                                                      |                                        |




