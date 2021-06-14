## FastAPI + Keycloak - Construí minha API. E Agora?

#### About
```console
schneider@localhost:~$ finger `id -un` | head -1 | cut -d: -f3-
 Gustavo Schneider
```

### Introdução
A algum tempo atrás construí uma API e me fiz essa pergunta.
> "Contruí minha API. E agora? Como disponibilizá-la para terceiros? Como autenticar o sistema de terceiros?"

O meu objetivo era permitir que usuários se cadastrassem no meu sistema e, a partir daí, pudessem criar um _**client_id**_ e um _**client_secret**_ para que seu sistema consuma a API que eu desenvolvi. Assim como Facebook, Github e outras empresas fazem.

**Note que não é o usuário se autenticar mas sim o seu sistema**.

### A resposta é simples: OAuth2, certo? Certo!

Boa sorte lendo a especificação e sofrendo com a falta de exemplos simples (e práticos) pra ajudar a entender como implementar.

Se para você, esta funcionalidade é algo trivial, saiba que ao pesquisar como essas empresas fizeram (ou fazem) eu não encontrei nenhum texto simples (e prático) que explicasse o passo-a-passo então, aqui estou, documentando como **EU** implementei essa funcionalidade e, talvez, facilite a vida de alguém.

:warning: _**Disclaimer**: Eu não acredito que esta seja a melhor forma ou a forma correta de se implementar esta funcionalidade. Esta foi apenas a forma mais simples que encontrei de ter o **MEU problema resolvido**._

### A stack de tecnologias.

* [Python](https://www.python.org/) + [FastAPI](https://fastapi.tiangolo.com/) + [PostgreSQL](https://www.postgresql.org/). A API foi construída com essa stack, além disso, atualmente é minha stack preferida.
* [Keycloak](https://www.keycloak.org/) para gerenciar os usuários/aplicações e autenticação/autorização.
* [Angular](http://angular.io/) para o frontend onde os usuários criarão suas aplicações.
* [Docker](https://www.docker.com/). Por que sim!



