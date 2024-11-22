🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/02%20-%20multa.md)  
![image](https://github.com/user-attachments/assets/04662de1-1516-48d7-bb8c-50b38989e58b)
# e-contrib - Modelo e-2025 
##  Contribuinte


# 🎲 - Modelo de dados:
 **\#**  |**Nome Físico**               |
---------|------------------------------|
01       | contribuinte                 |


#
#   ✅ - Tabelas relacionada
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | contribuinte_fisico          |      1 - n    |
02       | nota_contribuinte            |      1 - n    |
03       | lancamento                   |      1 - n    |
04       | tomador                      |      1 - n    |
05       | parcelamento_debito          |      1 - n    |
06       | contribuinte_historico       |      1 - n    |
07       | protocolo                    |      1 - n    |
08       | imovel                       |      1 - n    |
09       | contato                      |      1 - n    |
10       | credito                      |      1 - n    |
11       | nota_cancelada               |      1 - n    |
12       | contribuinte_movimentacao    |      1 - n    |
13       | loteamento                   |      1 - n    |
14       | nota_avulsa                  |      1 - n    |
15       | empresa                      |      1 - n    |
16       | receita_condutor             |      1 - n    |
17       | crendenciamento              |      1 - n    |
18       | contribuinte_cnd             |      1 - n    |
19       | nota_fila_api                |      1 - n    |
20       | termo_inscricao_da           |      1 - n    |


#   ✅ - Tabelas dependente
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
01       | imovel_caracteristica        |    1 - n      |
02       | cidade                       |    1 - n      | 
03       | bairro                       |    1 - n      |
04       | pais                         |    1 - n      |
05       | tipo_logradouro              |    1 - n      |


# Tabela de Contribuinte 
 **\#**  | **Campo**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|-----------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                          |                         | BIGINT \(20\) UN AI PK  | Identificador cadastro do contribuinte\.                                             |                                        |
02       | fk\_pais                    | [pais](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md)                    | BIGINT \(20\) UN       |                             |                                        |
03       | fk\_cidade                  | [cidade](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/16%20-%20cidade.md)                  | BIGINT\(20\) UN         |                                                                                      |                                        |
04       | fk\_tipo\_logradouro        | [tipo_logradouro]()        | BIGINT\(20\) UN         |                                                                                      |                                     |
05       | fk\_bairro                  | [bairro](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/23%20-%20Bairro.md)                  | BIGINT\(20\) UN         |                                                                                      |                                        | 
06       | fk\_imovel\_caracteristica  | [imovel_caracteristica]()  | BIGINT\(20\) UN         | Cadastro da entidade => empresa                                                   |           |
07       | razao\_social               |                         | VARCHAR\(100\)          |                                                                                      |Razão social ou Nome completo           |
08       | fantasia                    |                         | VARCHAR\(100\)          | Campo de cadastro apenas para "tipo = 1 - Juridico"                                       |Fantasia                              |
09       | cpf\_cnpj                   |                         | VARCHAR\(100\)          | Observação: Preencher com CPF/CNPJ válido.                                           |CNPJ ou CPF                             |
10       | email                       |                         | VARCHAR\(100\)          | Endereço eletrônico.<br> **Validação:** e-mail deve ser possuir o caractere "@"<br>  e este não pode estar no início e no fim do e-mail. Deve possuir no mínimo<br>  um caractere "." depois do @ e não pode estar no início ou no final do e-mail.|E-mail | 
11       | unidade                     |                         | VARCHAR\(20\)           |                                                                                      ||  
12       | contato                     |                         | VARCHAR\(20\)           | Número de telefone do contribuinte, com DDD. <br> **Validação:** Se preenchido, deve conter apenas números, com o mínimo de dez dígitos.| Telefone fixo |
13       | contato2                    |                         | VARCHAR\(20\)           | Número de telefone do contribuinte, com DDD. <br> **Validação:** Se preenchido, deve conter apenas números, com o mínimo de dez dígitos.| Celular|  
14       | contato\_wpp                |                         | VARCHAR\(20\)           | **Validação:** <br> 0 - não é whats app; <br> 1 - Sim é Whats app; | whatsapp|
15       | tipo                        |                         | TINYINT\(4\)            | Tipo contribuinte.<br> **Valores:**<br> 0 - Fisico <br> 1 - Juridico| Tipo pessoa|
16       | CEP                         |                         | VARCHAR\(9\)            | Código de Endereçamento Postal - CEP. <br> **Validação:**<br>Deve ser preenchido apenas com números, com 8 (oito) posições.|CEP |
17       | endereco                    |                         | VARCHAR\(100\)          | Endereço do contribuinte||
18       | numero                      |                         | VARCHAR\(100\)          | Número do logradouro.<br> Se não houver número a ser informado, preencher com "S/N".|Número |
19       | complemento                 |                         | VARCHAR\(200\)          | Complemento do logradouro.|Complemento|
20       | site                        |                         | VARCHAR\(255\)          | Link utilizando padrão URL (Uniform Resource Locator).<br>(**Observação:** Sem validador) |Site|
21       | imagem                      |                         | VARCHAR(191)            | Apenas Arquivos imagem. |
22       | situação                    |                         | TINYINT(4) NN           | **Valores válidos:** <br>SITUACAO_INATIVO = 0; <br> SITUACAO_ATIVO = 1;<br> SITUACAO_OBITO = 2; <br> **Regras:** <br> - Registro de falecimento;||
23       | observacoes                 |                         | Text                    | **Default/Expression:** Null ||
24       | prefeito_nome               |                         | VARCHAR(100)            |  Campo referente cadastro "entidade" => "empresa";||
24       | prefeito_ass_digitalizada   |                         | Text                    |  Campo referente cadastro "entidade" => "empresa";||
25       | chefe_setor_nome            |                         | VARCHAR(100)            |  Campo referente cadastro "entidade" => "empresa";||
26       | chefe_setor_cargo           |                         | VARCHAR(100)            |  Campo referente cadastro "entidade" => "empresa";||
27       | chefe_setor_portaria        |                         | VARCHAR(30)             |  Campo referente cadastro "entidade" => "empresa";||
28       | chefe_setor_ass_digitalizada|                         | TEXT                    |  Campo referente cadastro "entidade" => "empresa";||


# Ações / botões:
 **\#**  |**Nome**                      |   **Função**  |
---------|------------------------------|---------------|
1        | excluir                      |               |


↩️[Voltar página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/05%20-%20conta_contabil.md) | ➡️[Proxima página](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/07%20-%20receitas.md)|🔢[Voltar menu](https://github.com/VenturaCerqueira/Documento_gestao_tributaria) 
