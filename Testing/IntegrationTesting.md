# Testes de Integração
- É um tipo de teste onde os módulos de software são integrados e testados como um grupo.
- O objetivo é expor defeitos na interação entre esses módulos quando eles são integrados.
- Um projeto de software consiste em vários módulos de software, codificados por diversos programadores.
- Concentra-se na verificação da comunicação de dados entre esses módulos.
- É denominado I&T (integração e teste), 'teste de string' ou às vezes "teste de thread".

## Por que fazer testes de integração?
- Um módulo, em geral, é projetado por um desenvolvedor individual, assim a compreensão e a lógica podem ser diferentes. Os testes verificam se os módulos funcionam em unidade.
- No momento do desenvolvimento do módulo, há grandes chances de troca de requisitos por parte do cliente. Esses requisitos podem não ser testados em unidade.
- As interfaces dos módulos com o banco de dados podem estar erradas.
- Interfaces de hardware externo, se tiver, podem estar erradas.
- O tratamento inadequado de exceções pode causar problemas.

## Tipos de testes de integração:
- Abordagem do Big Bang
- Abordagem incremental, dividida em:
  - Abordagem de cima para baixo.
  - Abordagem de baixo para cima.
  - Abordagem sanduíche -> Combinação das duas.

### Teste do Big Bang
- É a abordagem na qual todos os componentes ou módulos são integrados de uma vez só e depois testados como unidade.
- Se todos os componentes das unidades não forem concluídos, o processo de integração não será executado.
- Vantagens:
  - Conveniente para sistemas pequenos.
- Desvantagens:
  - Difícil localização das falhas.
  - Dado o grande número de interfaces que precisam ser testadas, alguns links de interfaces podem ser facilmente perdidos.
  - A equipe de teste terá menos tempo na execução da fase de testes, por precisar que todos os componentes e módulos estejam finalizados.
  - Como todos os módulos são testados de uma só vez, os módulos críticos de alto risco não são isolados e testados com prioridade.

### Teste incremental
- O teste é feito integrando dois ou mais módulos que estão relacionados entre si.
- Em seguida, os outros módulos relacionados são integrados de forma incremental e o processo continua até o fim.
- Teste de integração de baixo para cima (bottom-up)
  - É o teste no qual os módulos de nível inferior são testados primeiro.
  - Vantagens:
    - A localização de falhas é mais rápida.
    - Não se perde tempo esperando que todos os módulos sejam desenvolvidos.
  - Desvantagens:
    - Os módulos críticos (nível superior) que controlam o fluxo da aplicação são testados por último.
    - Um protótipo inicial não é possível.
- Teste de integração de cima para baixo (Top Down)
  - É o inverso do teste de baixo para cima.
  - Possibilita obter o protótipo antecipado.
