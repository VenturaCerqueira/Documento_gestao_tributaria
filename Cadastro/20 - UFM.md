↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md)| ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/19%20-cnae_item_servico.md) |🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - UFM (Unidade Fiscal do Município)
Utilizada para corrigir monetariamente os valores de multas, taxas, tributos e outras dívidas, compensando as distorções causadas pela inflação.

# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | ufm                          |

#
# 🔢 - Campos:cnae_item_servico
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | competencia                  |                         | date                    | Período fiscal ao qual a UFM se refere.                                              |                                        |
03       | valor                        |                         | decimal(12,2)           | Valor unidade fiscal do município.                                                   |                                        |
04       | status                       |                         | tinyint UN              |                                                                                      |                                        |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |




↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md) |🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 