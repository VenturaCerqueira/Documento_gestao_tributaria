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
1        | cidade                       |     1 - n     |
2        | nota_contribuinte            |               |
3        | tomador                      |               |
4        | nota_tomador                 |               |
5        | bairro                       |               |
6        | users                        |               |
7        | nota                         |               |
8        | contribuinte                 |               |



#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_estado                    | cidade                  | bigint UN               |                                                                                      |                                        |
03       | nome                         |                         | varchar(100)            | Nome das cidades                                                                     |                                        |
04       | ibge                         |                         | int                     | Codígo do IBGE dos municipio.                                                        |                                        |





