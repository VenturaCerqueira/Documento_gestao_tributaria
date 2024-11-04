![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 


# Sumário de Documentos de Gestão Tributária
## 1. Cadastro
- **01 - índice_financeiro.md**
- **02 - multa.md**
- **03 - juros.md**
- **04 - tipo_de_receita.md**
- **05 - conta_contabil.md**
- **06 - classificacao_receita.md**
- **07 - receitas.md**
- **08 - tipos_procedimento.md**
- **09 - CNAE.md**
- **10 - item_servico.md**
- **11 - veiculo_marca.md**
- **12 - veiculo.md**
- **13 - bairro.md**
- **14 - tipo_movimentacao.md**
- **15 - banco.md**
- **16 - cidade.md**
- **17 - estado.md**
- **18 - pais.md**

## 2. Contribuinte
- **Contribuinte.md**

## 3. Home
- **url.md**

## 4. Imobiliário
### Tabelas
- **01 - CIP.md**
 - **02 - Tipo_logradouro.md**
- **03 - logradouro.md**
- **04 - aliquota_iptu.md**
- **05 - info_imovel.md**
- **06 - caracteristica_imovel.md**
- **07 - item_caracteristica_imovel.md**
- **08 - loteamento.md**

- **imovel.md**
- **logradouro.md**
- **processa_iptu.md**

## 5. Nota Fiscal Avulsa

## 6. Processamento


#
##  Cadastro - Idice Financeiro  
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | iten_servico                 |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
1        | cnae_item_servico            |     1 - n     |
2        | Contribuinte_juridico        |     1 - n     |
3        | nota_contribuinte            |     1 - n     |
4        | nota                         |     1 - n     |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | nome                         |                         | varchar(100)            |                                                                                      |  Código                                |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |


#

##  Cadastro - Multa  
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       |  multa                       |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | receita_tipo                 |      1 - n    |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | descricao                    |                         | varchar(30)             |                                                                                      |  Descrição                             |
03       | competencia                  |                         | Date                    |                                                                                      |  Competência                           |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | view                         |               |
3        | excluir                      |               |



#


##  Cadastro - Juros
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | juros                        |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | receita_tipo                 |     1 - n     |

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | descricao*                   |                         | varchar(30)             |                                                                                      |  Descrição                             |
03       | competencia*                 |                         | date                    |                                                                                      |  Competência                           |
04       | percentual*                  |                         | decimal(15,2)           |                                                                                      |  Percentual/mês                        |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |



#


##  Cadastro - Tipo de receita 
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | receita_tipo                 |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | conta_contabil               |     1 - N     |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | indice_financeiro            |     1 - 1     |
02       | juros                        |     1 - 1     |
03       | multa                        |     1 - 1     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_indice                    | indice_financeiro       | bigint(20)              |                                                                                      | Índice                                 |
03       | fk_multa*                    | multa                   | bigint(20)              |                                                                                      | Multa                                  |
04       | fk_juros*                    | juros                   | bigint(20)              |                                                                                      | Juros                                  |
05       | descricao*                   |                         | varchar(100)            |                                                                                      | Descrição                              |   
06       | natureza*                    |                         | tinyint(3)              |                                                                                      | Natureza                               |

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Excluir                      |               |


# Observação:
    Apenas cadastros acima de 10 são permitidos excluir. 


#


##  Cadastro - Conta contábil 
### 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
01       | conta_contabil               |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | lancamento                   |     1 - N     |
02       | receita_classificacao        |     1 - N     |


#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
01       | receita_tipo                 |     1 - N     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fK_receita_tipo*             | receita_tipo            | bigint(20)              |                                                                                      | Tipo de receita                        |
03       | codigo*                      |                         | varchar(50)             |                                                                                      | Código                                 |
04       | descricao*                   |                         | varchar(200)            |                                                                                      | Descrição                              |
05       | sigla*                       |                         | varchar(10)             |                                                                                      | Sigla                                  |


# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | excluir                      |               |





