#   ✅ Estrutura da URL:
####  🌐 Base da URL:
    www.e-contrib.com.br
*   **Caminho (rota principal):** /gestaotributaria
*   **Parâmetro dinâmico:** [entidade] ⇒  uma string (nome VARCHA(50)) da tabela entidades.
*   **Rota final:** /login

####    Nome da entidade seja "keep” a URL final seria:
     www.e-contrib.com.br/gestaotributaria/keep/login

![alt text](image.png)

###  Descrição:
*   A URL é composta pela base (www.e-contrib.com.br) seguida pela rota fixa /gestaotributaria, indicando que estamos acessando o módulo de gestão tributária;
*   Em seguida, o parâmetro **[entidade]** (como "keep”) é passado dinamicamente para identificar a entidade no sistema;
*   Por fim, a rota termina com /login, indicando a ação que está sendo realizada;

![alt text](image-1.png)

 **\# ** | **Campo**                   | **Tabela Raiz**         | **Tipo/Tamanho**        | **Descrição**                                                                        |
---------|-----------------------------|-------------------------|-------------------------|--------------------------------------------------------------------------------------|
 1       | ID                          |                         | BIGINT \(20\) UN AI PK  | Identificador cadastro do contribuinte\.                                             |     
 2       | fk\_pais                    | pais                    | BIGINT \(20\) UN        |                                                                                      |      
 3       | fk\_cidade                  | cidade                  | BIGINT\(20\) UN         |                                                                                      |    
 4       | fk\_tipo\_logradouro        | tipo\_logradouro        | BIGINT\(20\) UN         |                                                                                      |      
 5       | fk\_bairro                  | bairro                  | BIGINT\(20\) UN         |                                                                                      |     
 6       | fk\_imovel\_caracteristica  | imovel\_caracteristica  | BIGINT\(20\) UN         | Cadastro da entidade => empresa                                                      |  
 7       | razao\_social               |                         | VARCHAR\(100\)          |                                                                                      |    
 8       | fantasia                    |                         | VARCHAR\(100\)          | ADD + Campo caso "tipo" == 1 (Tipo => Juridico)                                      |      
 9       | cpf\_cnpj                   |                         | VARCHAR\(100\)          | Observação: Preencher com CPF/CNPJ válido.                                           |      
 10      | email                       |                         | VARCHAR\(100\)          | Endereço eletrônico.<br> **Validação:** e-mail deve ser possuir o caractere "@"<br>  e este não pode estar no início e no fim do e-mail. Deve possuir no mínimo<br>  um caractere "." depois do @ e não pode estar no início ou no final do e-mail.                                                       |      
 11      | unidade                     |                         | VARCHAR\(20\)           |                                                                          |      
 12      | contato                     |                         | VARCHAR\(20\)           | Número de telefone do contribuinte, com DDD. <br> **Validação:** Se preenchido, deve conter apenas números, com o mínimo de dez dígitos.                                        | 
 13      | contato2                    |                         | VARCHAR\(20\)           |          |      
 14      | contato\_wpp                |                         | VARCHAR\(20\)           |  |     
 15      | tipo                        |                         | TINYINT\(4\)            |                                                                                     |     
 16      | CEP                         |                         | VARCHAR\(9\)            |                                                                                      |      
 17      | endereco                    |                         | VARCHAR\(100\)          |                                       |      
 18      | numero                      |                         | VARCHAR\(100\)          |                                                                           |   
 19      | complemento                 |                         | VARCHAR\(200\)          |              |