↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/22-%20Org%C3%A3o%20Emissor.md) |🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
## 🗺️ Cadastro - Bairro


# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
1        | pais                         |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | logradouro                   |    1 - N      |
02       | contribuinte                 |    1 - N      |
03       | loteamento                   |    1 - N      |
04       | imovel                       |    1 - N      |


#   ✅ - Tabelas dependente:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | cidade                       |     1 -  N    |  


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                           | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|-----------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                         |                                        |
02       | fk_cidade                    | cidade                  | bigint UN               | Código *"id"* da tabela cidade.                                                         |                                        |
03       | nome                         |                         | varchar(100)            | Nome dos bairros.                                                                       |                                        |

↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/22-%20Org%C3%A3o%20Emissor.md) |🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 