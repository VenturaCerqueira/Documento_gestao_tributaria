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
*   Em seguida, o parâmetro [entidade] (como "keep”) é passado dinamicamente para identificar a entidade no sistema;
*   Por fim, a rota termina com /login, indicando a ação que está sendo realizada;

![alt text](image-1.png)
#   

#    ✅ Login:

####    🌐URL: 
    www.e-contrib.com.br/gestaotributaria/keep/login

#### Campos:
*   Os campos necessários para o login são:
    *   **E-mail:**
        *   Este campo corresponde à coluna email na tabela users.
        *   **Tipo de dado:** varchar(100)  e não pode ser nulo (is not null);
    *   **Senha:**
        *   Este campo corresponde à coluna password na tabela users;
        *   **Tipo de dado:** varchar(191) não pode ser nulo (is not null);

#### Validações adicionais:
Essas são validações que acontecem após solicitação de login, verificando se o usuário tem as permissões ou condições necessárias para acessar o sistema:

*   **fk_cidade:**
    *   **Tipo de dado:** bigint(20) unsigned  (não negativo).
    *   Chave estrangeira **(fk)**, que faz referência ao campo **id** da tabela **cidade**.
    *   **cidade** possui uma relação com a tabela estado por meio de um campo chamado fk_estado que se refere ao id na tabela estado.

*   **status:**
    *   **Tipo de dado:** tinyint(4) not null, que geralmente representa um valor numérico pequeno (como 0 ou 1).
    *   Pode ser utilizado para indicar o **status** do usuário, como:
        *   Ativo (1);
        *   Inativo (0).

#   

#   🙍🏼Contribuintes:
####    **URL:**
     www.e-contrib.com.br/gestaotributaria/keep/contribuintes

###  Campos:
####    Os campos formulário:
*   **🖼️ - Foto:**
    *   **Descrição:** Campo que corresponde à coluna imagem na tabela contribuinte.
    *   **Tipo de Dado:** *varchar(191)*
    *   **Restrição:** Não pode ser nulo (is not null)

*   **👨🏼‍💼/🙍🏼 - Tipo Pessoa (Jurídica/Física):**
*   **Descrição:** Campo que corresponde à coluna **tipo** na tabela contribuinte.
    *   **Tipo de Dado:** *tinyint(4)*
    *   **Restrição:** Não pode ser nulo (is not null)
    *   **Código:** 
    ~~~
     name: "Tipo pessoa",
            selector: row => [row.tipo == 1 ? 'Jurídica' : 'Física'],
            sortable: true,
    ~~~

    *   **🔢 - CPF/CNPJ:**
    *   **Descrição:**  Campo que corresponde à coluna cpf_cnpj na tabela contribuinte.
    *   **Tipo de Dado:** *varchar(14)*
    *   **Restrição:** Não pode ser nulo (is not null)
    *   **Código:**
     ~~~
     name: "CPF/CNPJ",
            selector: row => [formatoCpfCnpj(row.cpf_cnpj)],
            sortable: true,
      ~~~ 

    *   **🔡 - Nome/Razão Social:**
    *   **Descrição:**  Campo que corresponde à coluna **razao_social** na tabela **contribuinte**.
    *   **Tipo de Dado:** *varchar(100)*
    *   **Restrição:** Não pode ser nulo (is not null)
    *   **Código:**
     ~~~
        name:   "Nome/Razão social",
                selector: row => [row.razao_social],
                sortable: true,
      ~~~ 

    *   **🗺️ - Município/UF:**
    *   **União dos campos:** cidade.nome + ‘ - ‘ + estado.uf ⇒
    *   **Tabela**  ⇒  “cidade” ⇒ ”nome”     ⇒
    *   **Tabela**  ⇒  “estado” ⇒ ”uf”       ⇒ varchar(2) 
    *   **Código:**
     ~~~
        name: "Município/UF",
            selector: row => [row.cidade.nome + ' - ' + row.cidade.estado.uf],
            sortable: true,
      ~~~ 
      
    *   **✅ - Situação:**
    *   **Descrição:**  Campo corresponde à coluna **situacao** na tabela **contribuinte**.
    *   **Tipo de Dado:**  tinyint(4);
    *   **Restrição:** Não pode ser nulo (is not null)
    *   **Código:**<br>
            	0 - Inativo:<br> 
			    1 - Ativo: <br>
		 	    2 - óbito: <br>
                     - Data do falecimento;<br>
                     - Responsável pelo falecido ⇒ 
     ~~~
        row.contribuinte_fisico.obito_data)+ '- '+row.contribuinte_fisico.obito_nome_responsavel
      ~~~ 