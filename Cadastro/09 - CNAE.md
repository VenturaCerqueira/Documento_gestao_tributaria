![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - CNAE
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | cnae                         |


#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | cnae_item_servico            |    1 - N      |
02       | contribuinte_cnae            |    1 - N      |
03       | lancamento                   |    1 - N      |
04       | nota                         |    1 - N      |
05       | contribuinte_juridico        |    1 - N      |
06       | atividade_secundaria         |    1 - N

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | codigo                       |                         | varchar(14)             |                                                                                      |  Código                                |
03       | descricao                    |                         | text                    |                                                                                      |  Descrição                             |
04       | percentual                   |                         | decimal(15,2)           |                                                                                      |  Percentual                            |


# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |

