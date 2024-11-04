# e-contrib - Modelo e-2025 
## 🗺️ Cadastro - Cidade
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | estado                       |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
1        | nota_contribuinte            |               |
2        | tomador                      |               |
3        | nota_tomador                 |               |
4        | bairro                       |               |
5        | users                        |               |
6        | nota                         |               |
7        | contribuinte                 |               |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
1        | cidade                       |     1 - n     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_estado                    | cidade                  | bigint UN               | Codígo *"id"* do estado.                                                             |                                        |
03       | nome                         |                         | varchar(100)            | Nome das cidades                                                                     |                                        |
04       | ibge                         |                         | int                     | Codígo do IBGE dos municipio.                                                        |                                        |





