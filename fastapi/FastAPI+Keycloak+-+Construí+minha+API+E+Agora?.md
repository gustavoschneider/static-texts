## FastAPI + Keycloak - Construí minha API. E Agora?

### Introdução
A algum tempo atrás construí uma API e me fiz essa pergunta.
> "Contruí minha API. E agora? Como disponibilizá-la para terceiros? Como autenticar, contabilizar o acesso e **COBRAR** pela utilização da minha API?"

O que eu queria era permitir que usuários se cadastrassem no meu sistema e, a partir daí, pudessem criar um _**client_id**_ e um _**client_secret**_ para que seus sistemas consumissem a API que eu desenvolvi. Exatamente como Facebook, Github e outras empresas fazem.

Talvez, para você, isso seja algo simples mas pesquisando para descobrir como essas empresas fizeram/fazem eu não encontrei nenhum texto/tutorial simples o suficiente que explicasse o passo-a-passo.

Então, aqui estou, explicando o passo-a-passo de como **EU** implementei essa funcionalidade.

:warning: _**Disclaimer**: Eu não acredito que esta seja a melhor forma ou a forma correta de se implementar esta funcionalidade. Esta foi apenas a forma mais simples que encontrei de ter o **MEU** problema resolvido._

### A Stack de Tecnologias.

* [Python](https://www.python.org/) + [FastAPI](https://fastapi.tiangolo.com/) + [PostgreSQL](https://www.postgresql.org/) pois a API foi construída com essa stack. Além disso, atualmente, é minha stack preferida.
* [Keycloak](https://www.keycloak.org/) para gerenciar os usuários/aplicações e autenticação/autorização.
* [Angular](http://angular.io/) para o frontend onde os usuários criarão suas aplicações.
* [Docker](https://www.docker.com/). Por que sim!



