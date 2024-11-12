↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/03%20-%20juros.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20conta_contabil.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Receita condutor 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | receita_condutor             |

#
#   ✅ - Tabelas dependente:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | contribuinte_receita         |    1 - 1      |
02       | contribuinte                 |    1 - 1      |
03       | users                        |    1 - N      |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_usuario_cadastro          | users                   | bigint UN               |                                                                                      |                                        |
03       | fk_condutor                  | contribuinte            | bigint UN               |                                                                                      |                                        |
04       | fk_contribuinte_receita      | contribuinte_receita    | bigint UN               |                                                                                      |                                        |
05       | baixa                        |                         | dateime                 |                                                                                      |                                        |
06       | status                       |                         | tinyint                 |                                                                                      |                                        |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|



# Observação:
    

↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/03%20-%20juros.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20conta_contabil.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  