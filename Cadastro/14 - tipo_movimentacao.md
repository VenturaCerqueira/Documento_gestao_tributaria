↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/17%20-%20estado.md) |🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
## 🗺️ Cadastro - Tipo movimentação
Cadastro vinculado ao protocolo do contribuinte.  

# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
1        | tipo_movimentacao            |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | contribuinte_movimentacao    |    1 - N      |
#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                           | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|-----------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                         |                                        |
02       | descricao *                  |                         | varchar(191)            |                                                                                         | Descrição                              |

↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/17%20-%20estado.md) |🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 