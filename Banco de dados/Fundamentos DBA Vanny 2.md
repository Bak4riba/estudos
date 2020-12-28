FUNDAMENTOS DE BANCO DE DADOS
-
## Relacionamentos
----
Relacionamentos são muito importantes para as tabelas de um banco de dados pois basicamente é o que vai relacionar os dados da tabela X com os dados da tabela Y.

### Tipos de Relacionamentos
---

_1 para 1_: Um registro da tabela X é relacionado a somente 1 registro da tabela Y;
_1 para muitos_: Um registro da tabela X é relacionado com varios registros da tabela Y;
_Muitos para Muitos_:Varios registros da tabela X são relacionados com varios registros da tabela Y, na realidade normalmente quando se modela esse tipo de relacionamento se usa dois relacionamentos muitos para muitos, criando assim uma **tabela associativa**.

## ACID e Transações
---
**O que é uma transação?**
>Uma transação é uma sequência de operações executadas como uma única unidade lógica de trabalho.

ACID é um conceito que se refere às quatro propriedades de transação de um sistema de banco de dados: **Atomicidade, Consistência, Isolamento e Durabilidade.**<br>

**Atomicidade**: Em uma transação envolvendo duas ou mais partes de informações discretas, ou a transação será executada totalmente ou não será executada, garantindo assim que as transações sejam atômicas.<br>

**Consistência**: A transação cria um novo estado válido dos dados ou em caso de falha retorna todos os dados ao seu estado antes que a transação foi iniciada.<br>

**Isolamento**: Uma transação em andamento mas ainda não validada deve permanecer isolada de qualquer outra operação, ou seja, garantimos que a transação não será interferida por nenhuma outra transação concorrente.<br>

**Durabilidade**: Dados validados são registados pelo sistema de tal forma que mesmo no caso de uma falha e/ou reinício do sistema, os dados estão disponíveis em seu estado correto.<br>