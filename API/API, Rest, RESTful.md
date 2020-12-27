## API

- Cliente (Client)
- Garçom (pedidos, levar pedidos até a cozinha) (API)
- Cozinha (Server)

Acronimo para **Application Programming Interface** é basicamente um conjunto de rotinas e padrões estabelecidos por uma aplicação, para que outras aplicações possam utilizar as funcionalidades dessa aplicação.

- Responsável por estabelecer comunicação entre diferentes serviços.
- Meio de campo entre as tecnologias
- Intermediador para troca de informações

## REST

REST — Representational State Transfer realiza, geralmente, transferencia de dados via HTTP.

O REST, delimita algumas obrigações nessas transferencias de dados

Resources seria então um objeto, uma entidade.

### 6 NECESSIDADES (constraints) para ser RESTFUL

- _Uniform Interface_: Manter uma uniformidade, uma constância, um padrão na construção da interface. Nossa API precisa ser coerente para quem vai consumi-lá. Precisa fazer sentido para o cliente e não ser confusa. Logo, coisas como: o uso correto dos verbos HTTP; endpoints coerentes (todos os endpoints no plural, por exemplo); usar somente uma linguagem de comunicação (json) e não várias ao mesmo tempo; sempre enviar respostas aos clientes; são exemplos de aplicação de uma interface uniforme.

- _Client-Server_: Separação Cliente-Servidor, criando assim, uma portabilidade do nosso sistema, qualquer cliente consegue ter acesso sem muita dificuldade.

- _Stateless_: Toda request para o servidor deverá conter todas as informações necessárias para o servidor entender e responder devidamente.

- _Cacheable_: As respostas devem ser claras ao dizer se aquela requisição pode ou não ser cacheado pelo cliente.

- _Layered System_: Sistema dividido em camadas,ou seja, cliente acessa o endpoint, não há necessidade do cliente saber qual os passos ou processos são realizados pelo servidor para prover as informações necessárias para o cliente, o cliente não precisa saber da complexidade envolvida só necessita que as informações sejam providas a ele.

- _Code on Demand(Optional)_: Possibilidade de executar codigos no lado do cliente.


