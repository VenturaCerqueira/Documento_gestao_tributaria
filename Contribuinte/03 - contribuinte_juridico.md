🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md)  

![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025
 
##  Lista de Índice financeiro 
Utilizada para corrigir valores monetários ou ajustar tributos ao longo do tempo, considerando a inflação ou outras variações econômicas.<br>**Exemplo:** IPC, IGPM e outros. 

# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | contribuinte_juridico        |

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
