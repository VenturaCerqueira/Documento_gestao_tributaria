🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Idice Financeiro  
Utilizada para corrigir valores monetários ou ajustar tributos ao longo do tempo, levando em conta a inflação ou outras variações econômicas, **exemplo:** IPC, IGPM e outros. 
# Sistema:
Lista de Índices financeiro
![alt text](image.png)
**Data:** *08/11/2024*
 Novo Índice financeiro
![alt text](image-1.png)
Cadastro dos índice por mês/ano
![alt text](image-2.png)
# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | indice_financeiro            |
02       | indice_financeiro_correcao   |

#
#   ✅ - Tabelas relacionadas com 01 - indice_financeiro:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | indice_financeiro_correcao   |      1 - N    |
02       | receita_tipo                 |      1 - N    |

#   ✅ - Tabelas dependente 02 - indice_financeiro_correcao:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | indice_financeiro            |     1 -  N    |  

#
# 🔢 - Campos de 01 - indice_financeiro:
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome                         |                         | varchar(100)            |  nome do indice monetários.                                                          |  Código                                |

#
# 🔢 - Campos de 02 - indice_financeiro_correcao:
 **\#**  | **Nome**                     | **Tabela Raiz**          | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|--------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                          | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_indice                    |indice_financeiro_correcao| bigint UN               |                                                                                      |                                        |
03       | competencia                  |                          | date                    |                                                                                      |                                        |
04       | percentual                   |                          | decimal(15,2)           |                                                                                      |                                        |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |

 🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md)  