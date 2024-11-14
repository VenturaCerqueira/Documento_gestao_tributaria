🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025
 
##  Lista de Índice financeiro 
Utilizada para corrigir valores monetários ou ajustar tributos ao longo do tempo, considerando a inflação ou outras variações econômicas.<br>**Exemplo:** IPC, IGPM e outros. 
# Rotas/routes:
✅ Lista de Índices financeiro:
- http://www.e-contrib.com.br/gestaotributaria/**entidade**/cadastros/indices-financeiro

✅ Novo Índice financeiro:
- http://www.e-contrib.com.br/gestaotributaria/**entidade**/cadastros/indices-financeiro/criar

✅ Índices financeiro editar por competência:
- http://www.e-contrib.com.br/gestaotributaria/**entidade**/cadastros/indices-financeiro/editar/**Índice_selecionado**

# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | indice_financeiro            |
02       | indice_financeiro_correcao   |

#
#   ✅ - Tabelas relacionadas com 01 - indice_financeiro:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | indice_financeiro_correcao   |      1 - N    |
02       | receita_tipo                 |      1 - N    |

#   ✅ - Tabelas dependente 02 - indice_financeiro_correcao:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | indice_financeiro            |     1 -  N    |  

#
# 🔢 - Campos de 01 - indice_financeiro:
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome  *                      |                         | varchar(100)            |  Nome do indice monetários.                                                          |  Nome                                  |

#
# 🔢 - Campos de 02 - indice_financeiro_correcao:
 **\#**  | **Nome**                     | **Tabela Raiz**          | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|--------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                          | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_indice                    |indice_financeiro_correcao| bigint UN               | Código *"id"* da tabela de indice_financeiro                                         |                                        |
03       | competencia                  |                          | date                    | Data de competência do ajuste da inflação.                                           | Ano                                    |
04       | percentual                   |                          | decimal(15,2)           | Cadastro do indicador da inflação.                                                    | IPCA ACUMULADO %                       |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |

 🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md)  