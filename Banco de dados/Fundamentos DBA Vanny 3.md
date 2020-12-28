# PLANEJANDO E MODELANDO UM BANCO DE DADOS
## Diagrama ER (Diagrama de Relacionamento de Entidades)

> Diagrama que usa tabelas, campos e relacionamentos para planejar um banco de dados

Partindo do nosso exemplo do restaurante, quais seriam as necessidades desse banco de dados?

      * Clientes 
      * Pratos
      * Eventos
      * Pedidos
      * Reservas
      * Prato Favorito


Bom, começando pela tabela clientes podemos obter as seguintes informações para o registro dos clientes:

      * Nome
      * Sobrenome
      * Email
      * Telefone
      * Aniversario
      * Endereco
      * Cidade
      * Estado

Agora, vamos partir para o registro de um prato, podemos obter as seguintes informaçoes:

      * Nome
      * Descricao
      * Preco


Registro de Eventos:

      * Nome 
      * Descricao 
      * Data


Agora, vamos ver um pouco sobre **Tipos de Dados**, pois precisamos definir qual tipo de dado cada campo irá receber.

### Tipos de Dados ou DATATYPE

      * String - Caracteres alfanuméricos e texto
          * Char - Numero definido de caracteres
          * Varchar - Numero variavel de caracteres até um comprimento máximo
      * Date - Datas 
          * Date - Datas [Não há necessidade de armazenar as horas]
          * Datetime - Data e Hora [Há necessidade de armazenar a hora]
          * Timestamp - Momento em que o registro é a adicionado ao banco
      * Decimal - Numeros Exatos
      * Float - Numeros Aproximados 
      * Int - Numeros Inteiros 
      * Null - Ausencia de um valor

---

Retomando nosso exemplo, nossas tabelas ficariam desta maneira:

**Clientes**:

      * Nome VARCHAR(50)
      * Sobrenome VARCHAR(50)
      * Email VARCHAR(50)
      * Telefone VARCHAR(200)
      * Aniversario DATE()
      * Endereco VARCHAR(50)
      * Cidade VARCHAR(50)
      * Estado VARCHAR(50)

**Pratos**:

      * Nome VARCHAR(50)
      * Descricao VARCHAR(500)
      * Preco DECIMAL(3,2) //3 casas, 2 casas depois da virgula

**Eventos**:

      * Nome VARCHAR(50)
      * Descricao VARCHAR(500)
      * Data DATE()