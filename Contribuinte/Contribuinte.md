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


#   ✅ - Tabelas dependente
 **\#**  |**Nome Físico**               |   **Relação** |
---------|------------------------------|---------------|      
 


# Tabela de Contribuinte 
 **\#**  | **Campo**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        | **Campo sistema**                      |
---------|-----------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
01       | id                          |                         | BIGINT \(20\) UN AI PK  | Identificador cadastro do contribuinte\.                                             |                                        |
02       | fk\_pais                    | [pais](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/18%20-%20pais.md)                    | BIGINT \(20\) UN        |                                                                                      |                                        |
03       | fk\_cidade                  | [cidade](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/16%20-%20cidade.md)                  | BIGINT\(20\) UN         |                                                                                      |                                        |
04       | fk\_tipo\_logradouro        | [tipo_logradouro]()        | BIGINT\(20\) UN         |                                                                                      |                                        |
05       | fk\_bairro                  | [bairro](https://github.com/VenturaCerqueira/Documento_gestao_tributaria/blob/main/Cadastro/23%20-%20Bairro.md)                  | BIGINT\(20\) UN         |                                                                                      |                                        | 
06       | fk\_imovel\_caracteristica  | [imovel_caracteristica]()  | BIGINT\(20\) UN         | Cadastro da entidade => empresa                                                      |Cadastro da entidade => empresa               |
07       | razao\_social               |                         | VARCHAR\(100\)          |                                                                                      |                                        |
08       | fantasia                    |                         | VARCHAR\(100\)          | ADD + Campo caso "tipo" == 1 (Tipo => Juridico)                                      |                                        |
09       | cpf\_cnpj                   |                         | VARCHAR\(100\)          | Observação: Preencher com CPF/CNPJ válido.                                           |                                        |
10       | email                       |                         | VARCHAR\(100\)          | Endereço eletrônico.<br> **Validação:** e-mail deve ser possuir o caractere "@"<br>  e este não pode estar no início e no fim do e-mail. Deve possuir no mínimo<br>  um caractere "." depois do @ e não pode estar no início ou no final do e-mail.| | 
11       | unidade                     |                         | VARCHAR\(20\)           |                                                                                      ||  
12       | contato                     |                         | VARCHAR\(20\)           | Número de telefone do contribuinte, com DDD. <br> **Validação:** Se preenchido, deve conter apenas números, com o mínimo de dez dígitos.| |
13       | contato2                    |                         | VARCHAR\(20\)           | Número de telefone do contribuinte, com DDD. <br> **Validação:** Se preenchido, deve conter apenas números, com o mínimo de dez dígitos.||  
14       | contato\_wpp                |                         | VARCHAR\(20\)           | **Validação:** <br> 0 - não é whats app; <br> 1 - Sim é Whats app; | |
15       | tipo                        |                         | TINYINT\(4\)            | Tipo Juridico ou Fisico.<br> **Valores:** 0 - Fisico <br> 1 - Juridico||
16       | CEP                         |                         | VARCHAR\(9\)            | Código de Endereçamento Postal - CEP. <br> **Validação:** Deve ser preenchido apenas com números, com 8 (oito) posições.||
17       | endereco                    |                         | VARCHAR\(100\)          | Endereço do contribuinte||
18       | numero                      |                         | VARCHAR\(100\)          | Número do logradouro.<br> Se não houver número a ser informado, preencher com "S/N".||
19       | complemento                 |                         | VARCHAR\(200\)          | Complemento do logradouro.            ||
20       | site                        |                         | VARCHAR\(255\)          |                                       ||
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
