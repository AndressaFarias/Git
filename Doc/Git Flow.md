`----------------------------`
 Utilizando o fluxo Git Flow
`----------------------------`

Quando um código é produzido por diversas pessoas, é importante que seja possível ter o controle do que está sendo produzido. Pois ao mesmo tempo que são corrigidos falhas, são implementadas novas funcionlidades. 

A branch **master** deve conter todo o códico já testado, versionado que será entregue ao cliente e a branch **develop** é onde todo fluxo de trabalho irá ocorrer antes de fazer o release versionado que será feito merge na **master**.

A **develop** deve sempre conter o código mais atual, onde as branch de features serão ramificadas tendo ela como base. 

As nomenclaturas padrão recomendadas pelo _Git Flow_ são:
* **feature:** para novas implementações
* **release:** para finalizar o release e tags
* **hotfix:** para resolver problema crítico em produção que não pode esperar novo release

> Exemplo: 
> estando já na _branch_ **develop**, utilizamos o comando:
> `$ git checkout -b feature/novo-componente`
> Após criado, trabalhamos as modificação localmente, caso seja necessário que outra pessoa trabalhe nesta mesma implementação devemos compartilhar para seu repositório remoto:

> `$ git push origin feature/novo-componente`

> Após a implementação feita é hora de fazer o merge desta feature com a **develop**, para isto, faça o checkout para a _branch_ **develop**, faça o merge da feature e atualize o remoto:

> `$ git checkout develop && git merge feature/novo-componente && git push origin develop`

> Caso não ocorra nenhum conflito, estamos prontos para fazer o release desta implementação e submeter ao repositório remoto, para isto, crie a branch de release e envie:

> `$ git checkout -b release/v1.0.1 && git push origin release/v1.0.1`
> Após feito os ultimos testes, já pode ser feito a tag da versão:
> `$ git tag -a v1.0.1 -m “Release do novo componente”`
> Lembrando, que se foi identificado algum bug durante o processo, você deve tratar este bug na branch de release, enviar para a master e para a develop também, fazendo que a develop sempre contenha as correções.
> Agora vamos conferir se a tag foi criada e enviar para o repositório remoto:
> `$ git show v1.0.1 && git push origin v1.0.1`
> Se tudo correu bem, sua tag será criada e estamos aptos a fazer o merge com a master deste pequeno release na master:
> `$ git checkout master && git merge release/v1.0.1`
 