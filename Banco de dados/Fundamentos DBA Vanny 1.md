## Banco de Dados

### Tipos 
Existem varios tipos de banco de dados como por exemplo:
_Gráficos_: Neo4j
_Objetos_: Realm
_Documentos_:MongoDB
_Relacional_:MySQL

Entretanto o mais difundido é o relacional.
Trataremos aqui somente desse tipo de banco de dados, visto sua popularidade e o quanto é difundido.

### Por que é chamado de RELACIONAL?

Isso se deve pela maneira em que organiza os dados seja em relações ou tabelas de dados relacionadas

Nesse tipo de banco de dados as tabelas sao representadas por linhas que são instancias de uma entidade e por linhas que representam atributos dessa entidade.
|Entidade 1  |                           |                          |
|------------|--------------------------|--------------------------|
|  **_Atributo 1_**               | **_Atributo 2_**               | **_Atributo 3_** 
|  Atributo 1 do Registro 1 | Atributo 2 do Registro 1 | Atributo 3 do Registro 1 |
|  Atributo 1 do Registro 2 | Atributo 2 do Registro 2 | Atributo 3 do Registro 2 |
|  Atributo 1 do Registro 3 | Atributo 3 do Registro 3 | Atributo 3 do Registro 3 |
|  Atributo 1 do Registro 4 | Atributo 4 do Registro 4 | Atributo 3 do Registro 4 |
__________________________________________________________________________________

#### Exemplo
Para trazer mais proximo a nossa realidade, vamos exemplificar aqui que você tenha um restaurante, nesse restaurante você atende clientes cada cliente possui atributos unicos porém que são comuns a cada cliente, ou seja, cada cliente é unico porém eles possuem informações que o descrevem ou os identificam que são comuns a todos os clientes como por exemplo **Nome**, **Sobrenome**, **Telefone**. Esses _atributos_ serão os atributos que consituiram nossa tabela:

|Clientes                   |                               |                |         
|:-------------------------:|:-----------------------------:|:--------------:|
|  **_Nome_**               | **_Sobrenome_**               | **_Telefone_** |
|  João                     | Da Silva                      | (42)99999-8888 |
| Marcio                    | Oliveira                      | (42)99999-8888 |
|  Matheus                  | Bakaus                        | (42)99999-8888 |
| Maria                     | Ribeiro                       | (42)99999-8888 |
---


## Chaves e Valores Unicos 

Imaginemos agora que nessa tabela Clientes queremos solicitar ao banco de dados um registro especifico, por exemplo, queremos o telefone do Cliente de nome João, logo o banco retornará para nós esse registro,porém sabemos que várias pessoas se chamam João e no caso, podemos ter vários registros com esse mesmo nome, ou seja, quando solicitarmos isso ao banco de dados ele nos retornara todos os clientes de nome João, **mas então como resolver isso?**

Simples! Definimos um campo que seja unico para cada cliente, nem sempre haverá um atributo no mundo real que possa identificar cada registro, ou cada cliente no nosso caso.Então dispomos de um campo, por exemplo um ID que seja uma identificação unica de cada cliente, vide exemplo.

|Clientes |                           |                               |                |
|:---------:|-|:---------------------:|:-----------------------------:|:--------------:|
|**_ID_** |  **_Nome_**               | **_Sobrenome_**               | **_Telefone_** |
|   1     | João                      | Da Silva                      | (42)99999-8888 |
|   2     | Marcio                    | Oliveira                      | (42)99999-8888 |
|   3     | Matheus                   | Bakaus                        | (42)99999-8888 |
|   4     | Maria                     | Ribeiro                       | (42)99999-8888 |

Perceba que nossa tabela clientes agora possui um campo que é unico para cada cliente, ou seja, somente o cliente João possui o ID 1, isso faz com que facilita muito a nossa vida na hora de procurarmos por determinado registro visto que quando solicitarmos ao banco o registro de ID 1 ele nos retornará um unico registro com as informações do cliente João.<br>
No nosso exemplo ID é uma _Chave Unica(Primary Key)_ dos registros, isso significa que não aparece em nenhuma outra coluna.Podemos definir isso com qualquer campo, porém se definirmos essa restrição a um campo que pode haver o mesmo valor em outros registros, o banco de dados não deixará que os novos registros com o mesmo valor sejam criados,visto que ja existe um registro com aquele valor.<br>
No nosso exemplo nossa _Chave_ **ID** é uma chave primária é a chave mais importante de uma tabela porém nem sempre será possivel modificar o *schema* da tabela, então teremos que utilizar os campos ja fornecidos para validar isso, nesse caso criaremos uma _Chave Composta (compose Key)_: 
>Quando dois ou mais campos para atuar como um identificador exclusivo' 