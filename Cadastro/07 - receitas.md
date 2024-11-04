![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Receitas  
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       |  receita                     |
#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | receita_classificacao        |     1 - 1     |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | receita_valor                |     1 - N     |
02       | contribuinte_receita         |     1 - N     |
03       | lancamento                   |     1 - N     |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_receita_classificacao     | receita_classificacao   | bigint(20)              |                                                                                      | Classificação de receita               |
03       | codigo                       |                         | int(11)                 |                                                                                      | Código                                 |
04       | descricao                    |                         | varchar(255)            |                                                                                      | Descrição                              |
05       | valor                        |                         | decimal(15,2)           |                                                                                      | Valor                                  |
06       | mutiplicador                 |                         | tinyint(4)              |                                                                                      | Multiplicador                          |
07       | complemento                  |                         | varchar(30)             |                                                                                      | Descrição multiplicador                |
08       | cod_conta_principal          |                         | varchar(40)             |                                                                                      | Código principaL                       |
09       | cod_conta_encargos           |                         | varchar(40)             |                                                                                      | Juros/Multa                            |
10       | cod_conta_da                 |                         | varchar(40)             |                                                                                      | Dívida ativa                           |
11       | cod_conta_da_encargos        |                         | varchar(40)             |                                                                                      | Juros/Multa (D.A.)                     |
12       | num_fonte_recurso            |                         | varchar(20)             |                                                                                      | Nº fonte                               |
13       | cod_orgao                    |                         | varchar(20)             |                                                                                      | Código Órgão                           |  
14       | cod_conta_reconhecimento     |                         | varchar(40)             |                                                                                      | Código evento receita                  |
15       | cod_conta_pagamento          |                         | varchar(40)             |                                                                                      |                                        |        

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |

