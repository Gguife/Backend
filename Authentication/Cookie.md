# Cookie
  - São dados utilizados para identificar um usuário e suas preferências.
  - Cookies específicos são utilizados para manter a sessão de cada usuário.

## Cookie em etapas
  - Etapa 1: Cliente
    - Usuário se cadastra.
    - O cliente envia uma solicitação HTTP ao servidor contendo seu nome de usuário e senha.
  - Etapa 2: Servidor
    - Servidor recebe a solicitação e faz o hash da senha antes de armazenar as informações de login em seu banco de dados.
  - Etapa 3: Cliente
    - Usuário faz o login.
    - Novamente é feita uma solicitação HTTP ao servidor.
  - Etapa 4: Servidor
    - Aqui ocorre a validação do Login.
    - Servidor procura as informações em seu banco de dados.
    - Caso o hash não seja válido, o servidor nega o acesso.
  - Etapa 5: Servidor
    - Obtendo o acesso, criamos um token de acesso.
    - O token identifica exclusivamente a sessão do usuário.
    - O servidor faz duas coisas com o token de acesso:
      1. Armazena no banco de dados associado a esse usuário.
      2. Anexa-o a um cookie de resposta para ser retornado ao cliente, definindo data/hora de expiração para limitar a sessão do usuário.
  - Etapa 6: Cliente
    - Cada vez que o usuário acessa a página, há uma solicitação ao servidor contendo o envio do token de acesso do cookie.
    - O servidor compara com o que tem em seu banco de dados e o autoriza.
    - O cliente não precisa ficar digitando suas credenciais pelo tempo escolhido no processo de criação do cookie.
