↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/16%20-%20cidade.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 
 
![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
## 🗺️ Cadastro - Estado
Cadastro de estado base IBGE - BRASIL.

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | estado                       |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
1        | cidade                       |     1 - n     |

#
# 🔢 - Campos
 **\#**  | **Coluna**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | uf                           |                         | varchar(2)              | Sigla de duas letras para identificar estados.                                       |                                        | 
03       | nome                         |                         | varchar(191)            | Nome dos estados.                                                                    |                                        |  
04       | ibge                         |                         | int                     | **Campo sem utilização**                                                             |                                        |
05       | aliq_icms_interna            |                         | decimal(12,2)           | **Campo sem utilização**                                                             |                                        |

↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/16%20-%20cidade.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 
 