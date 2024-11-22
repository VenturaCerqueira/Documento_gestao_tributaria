🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025
 
##  Lista de Índice financeiro 
Utilizada para corrigir valores monetários ou ajustar tributos ao longo do tempo, considerando a inflação ou outras variações econômicas.<br>**Exemplo:** IPC, IGPM e outros. 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | contribuinte_fisico          |

#
#   ✅ - Tabelas relacionadas
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       |contribuinte_juridico         |    N - 1      |


#   ✅ - Tabelas dependente 
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | contribuinte                 |     1 -  N    |  

#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_contribuinte              | contribuinte            | bigint(20)              |||
03       | estrangeiro                  |                         | tinyint(4)              |||
04       | sexo                         |                         | tinyint(4)              |||
05       | rg                           |                         | varchar(10)             |||
06       | rg_orgao_emissor             |                         | varchar(10)             |||
07       | rg_data_exp                  |                         | date                    |||
08       | cnh                          |                         | varchar(15)             |||
09       | cnh_categoria                |                         | tinyint(4)              |||
10       | cnh_vencimento               |                         | date                    |||
11       | registro_profissional        |                         | varchar(20)             |||
12       | profissao                    |                         | varchar(50)             |||
13       | estado_civil                 |                         | int(11)                 |||
14       | data_nascimento              |                         | date                    |||
15       | nome_mae                     |                         | varchar(70)             |||
16       | obito_data                   |                         | date                    |||
17       | obito_nome_responsavel       |                         | varchar(70)             |||
18       | autonomo_informal            |                         | tinyint(4)              |||
