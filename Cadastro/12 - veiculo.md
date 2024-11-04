# e-contrib - Modelo e-2025 
## 🚗 Cadastro - Veiculo  
### Cadastro de ve

# 🎲 - Modelo de dados:
 **\#**  |**Nome Fisico**               |
---------|------------------------------|
1        | veiculo                      |

#
#   ✅ - Tabelas relacionadas:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------|      
1        | veiculo_marca                |     1 - n     |
2        | contribuinte                 |     1 - n     |

#   ✅ - Tabelas dependente:
 **\#**  |**Nome Fisico**               |   **Relação** |
---------|------------------------------|---------------| 
1        | lancamento                   |     n - 1     |
2        | contribuinte_receita         |     n - 1     |


#
# 🔢 - Campos
 **\#**  | **Nome**                     | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|------------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                           |                         | bigint UN AI PK         |                                                                                      |                                        |
02       | fk_proprietario *            | contribuinte            | BIGINT(20) UN           | Contribuinte Proprietário veiculo.                                                   | Proprietário                           | 
03       | fk_condutor *                | contribuinte            | BIGINT(20) UN           | Contribuinte condutor do veiculo, podendo ser diferente do proprietario.             | Condutor                               | 
04       | fk_marca *                   | veiculo_marca           | BIGINT(20)UN            | Marcas de veículo cadastrado no banco.                                               | Marca                                  |                      
05       | placa *                      |                         | varchar(12)             | Padrão de placa do Brasil Mercosul.                                                  | Placa                                  |   
06       | renavam *                    |                         | varchar(30)             | Registro Nacional de Veículos Automotores(11 dígitos).                               | Renavam                                |
07       | chassi *                     |                         | varchar(30)             | Chassi ou Número de Identificação do Veículo (VIN - 17dígito)                        | Chassi                                 |
08       | modelo *                     |                         | varchar(100)            | Modelo do veículo.                                                                   | Modelo                                 |
09       | ano_modelo *                 |                         | varchar(4)              | Ano do modelo do veículo.                                                            | Ano/Modelo                             |
10       | cor *                        |                         | varchar(20)             | Cor do veiculo.                                                                      | Cor                                    |
11       | responsavel                  |                         | varchar(100)            | **Remover coluna**                                                                   |                                        |
12       | status                       |                         | tinyint                 | **Campo gera função**                                                                |                                        |   

# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | Editar                       |               |
2        | Excluir                      |               |

    
# Observação:
    Placam renavam e chassi devem ser unico. Não pode ser duplicado.
    Status verifica funcionalidade