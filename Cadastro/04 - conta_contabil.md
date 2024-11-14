↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/03%20-%20juros.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20receitas.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Conta contábil 
Conta contábil é responsável por registrar e controlar as receitas e despesas associadas a impostos, taxas e outras obrigações fiscais. Ela assegura a classificação precisa e a apuração correta dos valores devidos, facilitando parte contábil.
# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | conta_contabil               |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | [lancamento]()                   |     1 - N     |
02       | [receita_classificacao](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/06%20-%20classificacao_receita.md)        |     1 - N     |


#   ✅ - Tabelas dependente:
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | [receita_tipo](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/07%20-%20receita_tipo.md)                |     1 - N     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fK_receita_tipo*             | [receita_tipo](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/07%20-%20receita_tipo.md)            | bigint(20)              | Código *"id"* da tabela *tipo_receita*.                                              | Tipo de receita                        |
03       | codigo*                      |                         | varchar(50)             | Código da conta contábil.                                                            | Código                                 |
04       | descricao*                   |                         | varchar(200)            | Detalhamento da conta contábil, com descrição da natureza.                           | Descrição                              |
05       | sigla*                       |                         | varchar(10)             | Sigla do tributo, **exemplos:** IPTU, TFF e outras abreviações.                      | Sigla                                  |


# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |

↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/04%20-%20tipo_de_receita.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/06%20-%20classificacao_receita.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria)  