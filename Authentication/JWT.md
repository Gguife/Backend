# JWT (Json Web Token)

- É uma metodologia de criptografia baseada em tokens.
- Usado para transferir informações de segurança como um objeto JSON.
- Clientes e servidores usam JWT para compartilhar informações com segurança.
- São ideais para contextos SSO (Single Sign-On).

  - O que é um SSO?
    - SSO permite que o usuário faça o login apenas uma vez e acesse vários recursos sem a necessidade de autenticação adicional.

## Sua estrutura

- JWT é uma string codificada.
- Consiste em 3 partes separadas por "."
- Com uma estrutura básica formada por `header`, `payload` e `signature`.
  - header: Contém informações sobre o tipo de token e o tipo de criptografia usado.
  - payload: Tem os dados que serão transmitidos no token, como informações de usuário e outras informações de autorização.
  - signature: É usada para verificar a integridade do token e garantir que ele não tenha sido alterado durante a transmissão.
  ```
  OBS: header e payload são codificados em base64, enquanto o signature é calculado utilizando uma chave secreta.
  ``` 

## Como implementar o JWT

- A implementação do JWT pode variar dependendo da linguagem de programação e framework.
- Irei citar aqui as principais etapas para implementação do JWT:
  - **Criação**: Envolve criar um objeto JSON com as informações desejadas, como ID de usuário e tempo de expiração. É necessário assinar o token usando uma chave secreta para garantir que ela não seja alterada.
  - **Armazenamento**: Essa estrutura deve ser armazenada do lado do cliente, em um cookie ou armazenamento local, para que possa ser enviada de volta ao servidor em cada requisição.
  - **Verificação de Autenticidade**: No servidor, é necessário verificar se o token é autêntico e se não foi alterado.
  - **Decodificação**: Assim que houver a verificação do Token, o JWT pode ser decodificado para obter as informações armazenadas nele.
  - **Uso das informações**: Com as informações do Token decodificadas, podemos utilizar as informações para autorizar e autenticar o usuário do sistema.

## Créditos e mais sobre

- Localweb: [https://www.locaweb.com.br/blog/temas/codigo-aberto/jwt-vantagens-json-web-token/#:~:text=A%20estrutura%20JWT%20%C3%A9%20uma,entre%20diferentes%20sistemas%20e%20plataformas](https://www.locaweb.com.br/blog/temas/codigo-aberto/jwt-vantagens-json-web-token/#:~:text=A%20estrutura%20JWT%20%C3%A9%20uma,entre%20diferentes%20sistemas%20e%20plataformas)
- JWT: [https://jwt.io/introduction](https://jwt.io/introduction)