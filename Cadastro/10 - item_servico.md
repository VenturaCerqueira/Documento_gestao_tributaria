![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Cadastro - Item de serviço  
### Lista de item de serviço com base na Lei Complementar nº 116, de 31 de julho de 2003, é um marco regulatório que dispõe sobre o Imposto sobre Serviços de Qualquer Natureza (ISSQN) um tributo de competência dos municípios e do Distrito Federal no Brasil.
**Link:**   https://www.planalto.gov.br/ccivil_03/leis/lcp/lcp116.htm

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
02       | codigo *                     |                         | varchar(10)             | códigos específicos de serviços. <br> O primeiro número identifica o grupo principal de serviço.<br> O segundo número identifica um serviço específico dentro daquele grupo.|  Código                                |
03       | descricao *                  |                         | text                    | Descrição do serviço.                                                                         |  Descrição                             |
04       | aliquota *                   |                         | decimal(12,2)           | Aliquota da nota de serviço entre 2% e 5%.                                                                                     |  Alíquota                              |
         

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |

