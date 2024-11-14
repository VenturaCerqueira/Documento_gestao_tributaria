↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md)| ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/20%20-%20UFM.md)||🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - CNAE item de serviço 
Tabela relacoional com codigo do CNAE. 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | cnae_item_servico            |

#
#   ✅ - Tabelas relacionadas: 
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | cnae                         |    1 - N      |
02       | item_servico                 |    1 - N      | 

#
# 🔢 - Campos:
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_cnae                      | cnae                    | bigint(20)              | Código *"id"* da tabela de **cnae**.                                                 |                                        |
03       | fk_item_servico              | item_servico            | bigint(20)              | Código *"id"* da tabela de **item_servico**.                                         |                                        |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |



↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md)| ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/20%20-%20UFM.md)||🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 