↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/01%20-%20indice_financeiro.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/03%20-%20juros.md) | 🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Multa  
Cadastro das multas aplicado para cálculo no DAM's, podendo cadastrar prazo inicial, prazo final e porcentual sobre-as.

#
# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       |  multa                       |
02       |  multa_prazo                 |

#
# Rotas/routes:
✅ Lista de Multa:
- http://www.e-contrib.com.br/gestaotributaria/**entidade**/cadastros/juros

✅ Novo Multa:
- http://www.e-contrib.com.br/gestaotributaria/**entidade**/cadastros/juros/criar

✅ Multa editar:
- http://www.e-contrib.com.br/gestaotributaria/**entidade**/cadastros/juros/editar/**multa_selecionado**

#
#   ✅ - Tabelas relacionadas: 01 - Multa:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | receita_tipo                 |      1 - n    |

#
# 🔢 - Campos tabela: 01 - multa  
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | descricao                    |                         | varchar(30)             | Campo texto sobre a natureza da multa.                                               |  Descrição                             |
03       | competencia                  |                         | Date                    | Campo período fiscal ao qual a multa se refere.                                      |  Competência                           |

#
# 🔢 - Campos tabela: 02- multa_prazo 
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_multa                     | multa                   | bigint(20)              | Código *"id"* da tabela de **multa**.                                                |                                        |
03       | prazo_inicial                |                         | int(11)                 | Início do período em dias para calcular a multa.                                     |  Prazo inicial                         |
04       | prazo_final                  |                         | int(11)                 | Término do período em dias para a aplicação da multa.                                |  Prazo final                           |
05       | percentual                   |                         | decimal(15,2)           | Percentual de multa que será aplicado dentro do período definido pelos prazos inicial e final.                                                                                      |  Percentual                            |

#
# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | view                         |               |
3        | excluir                      |               |

 ↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/01%20-%20indice_financeiro.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/03%20-%20juros.md) | 🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  