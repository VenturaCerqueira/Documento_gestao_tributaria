# e-contrib - Modelo e-2025 
## 🗺️ Imobiliário - Logradouro
### Cadastro de Logradouro.

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | logradouro                   |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      


#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
1        | bairro                       |     1 - n     |
2        | tipo_logradouro              |     1 - n     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_tipo_logradouro           | tipo_logradouro         | bigint UN               |                                                                                      |                                        |
03       | fk_bairro                    | bairro                  | bigint UN               |                                                                                      |                                        |
04       | codigo                       |                         | int(11)                 |                                                                                      |                                        |
05       | nome                         |                         | varchar(100)            |                                                                                      |                                        |                     
06       | distrito                     |                         | varchar(2)              |                                                                                      |                                        |
07       | setor                        |                         | varchar(2)              |                                                                                      |                                        |
08       | quadra                       |                         | varchar(3)              |                                                                                      |                                        |
09       | pluviais                     |                         | tinyint(4)              |                                                                                      |                                        | 
10       | sarjetas                     |                         | tinyint(4)              |                                                                                      |                                        |
11       | coleta_lixo                  |                         | tinyint(4)              |                                                                                      |                                        |
12       | limpeza_publica              |                         | tinyint(4)              |                                                                                      |                                        |
13       | rede_esgoto                  |                         | tinyint(4)              |                                                                                      |                                        |
14       | pavimentacao                 |                         | tinyint(4)              |                                                                                      |                                        |
15       | valor_metro                  |                         | decimal(15,2)           |                                                                                      |                                        |
16       | cep                          |                         | varchar(8)              |                                                                                      |                                        |


# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | Excluir                      |               |


