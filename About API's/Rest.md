# REST O que é?
  - Rest foi criado em 2000 por Roy Fielding.
  - Rest (Representational State Transfer) é um estilo arquitetonico para fornecer padrões entre sistemas de computador na web.
  - Ele Facilita a comunicação entre os sistemas.
  - Os sistemas compatives com REST geralmente são chamados de RESTful.

<img src="../public/Rest.png" alt="API Rest ilustration">

## Fundamentos REST
  - Ele utiliza o protocolo HTTP como interface de comunicação para transferir dados através dos métodos HTTP, ou seja, utiliza manipulações de dados básicas como criar, atualizar, editar e excluir informações.
  - Rest nos ajuda a desenvolver serviços mais escaláveis, seguros e flexíveis. Para isso, a arquitetura REST possui 6 restrições:
    - Client-Server (Cliente-Servidor)
    - Stateless 
    - Cache 
    - Interface Uniform (Interface uniforme)
    - Layerd System (Sistema em camadas)
    - Code on demand (Código sobe demanda)

### Client-Server
  - O princípio fundamental da arquitetura Client-Server é a Separação de Procupações.
  - O cliente que envia a solicitação é completamente independente do Servidor que retorna a respota

### Stateless
  - Todas as infromações exigidas em um pedido deveram ser enviadas pelo cliente.
  - O servidor nao deve armazenar nenhum dado durante a comunicação Client-Server.
  - Cada solicitação é uma solicitação independente.

### Cache
  - Cache é uma estrutura de armazenamento computacional.
  - É focado em manter armazenado os dados que são acessados frequentimente.
  - Pelo CACHE é possível reduzir ou até mesmo eliminar a necessidade do cliente enviar solicitações ao servidor.

### Interface Uniform
  - É o contrato entre o cliente e o servidor que definem os padrões para a comunicação.

### Layerd System
  - Está relacionado ao fato de que pode haver mais componentes e subsistemas entre um cliente e um servidor. Por exemplo: Um cliente envia uma solicitação a um servidor, mas primeiro passa por uma camada chamada proxy para verificação de segurança.
  
    <img src="../public/proxy.png" alt="RESTapi proxy" width="30%">

### Code on demand
  - Significa que um Servidor pode enviar um código executável como resposta ao cliente. 
  - É o que acontece quando o navegador recebe uma resposta do servidor com uma tag HTML, para que, quando carregar o documento HTML ele possa executar o script.


## Request
  - Rest requer que o cliente faça um solicitação ao servidor.
  - Uma solicitação geralmente consistem em :
    - Verbo HTTP: Define o tipo de operação realizada. (Get, Post, Put, Delete)
    - Um header: Permite que o cliente repasse informações sobre a solicitação.
    - Um caminho para o recurso.
    - Um corpo de mensagem opcional contento os dados. 

## Verbo HTTP (CRUD)
  - GET: exibe um recruso específico (por ID) ou uma coleção de recusos já existentes.
  - POST: cria um novo recurso.
  - PUT: atualiza um recurso ja existente (por ID).
  - DELETE: remove um recurso (por ID).

## Código de resposta 
  - As respostas do servidor cotém códigos de status para alertar ao cliente sobre informações de sucesso da operação.
  - Alguns dos mais comuns códigos:
    - 200 (OK) 
    - 201 (Criado)
    - 204 (Sem conteúdo)
    - 400 (Pedido incorreto) - A solicitação não pode ser preocessada devido a uma sintaxe de solicitação incorreta.
    - 403 (Proibido)
    - 404 (Não encontrado)
    - 500 (Erro interno no servidor)

### Créditos
  - https://www.codecademy.com/article/what-is-rest
  - https://dev.to/cassiocappellari/fundamentals-of-rest-api-2nag