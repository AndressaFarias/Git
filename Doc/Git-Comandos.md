# Comandos Git





# BRANCH

**Criar uma nova branch**
    Vamos nomear o nosso novo branch como «style».
    EXECUTE:

`git checkout -b style`
`git status`

:exclamation: Nota: `git checkout -b <branch name>` é o atalho de `git branch <branch name>` seguido por `git checkout <branch name>`.

:exclamation: Note que o comando `git status` avisa que você está no branch style.


**Verificar a branch atual**
`git branch` - mostras a branch em que estamos trabalhando

**Verificar a branch locais e remotas**
`git branch -a` - verificando as branch locais e remotas



# CONFIGURAÇÃO

**mudar editor**
    `git config --global core.editor vim`

**mudar e-mail**
    `git config --global user.email nome@serv.kkk`

**verificar variaveis**
    `git config --global -l` 


# DIFF

git --no-pager log prod-20210323.02..prod-20210324.01 --oneline --pretty=format:'[%h](http://github.com/loggi/loggi-web/commit/%H): %s by %an' --reverse



# REBASE
 - o rebase em resumo é fazer um git checkout na master
 - faz um git pull pra ter as ultimas modificacoes da master
 - ae voce faz git rebase <sua branch>



vc faz um git push -f depois pra tua branch qdo tiver dentro dela
14h09
pq ele refaz sua linha de commit
14h09
da tua branch





14h09
com o q entrou na master

# REPOSITÓRIOS

## atualizar repositório local
`git pull`
O comando git pull é usado para buscar e baixar conteúdo de um repositório remoto e atualizar imediatamente o repositório local. 


## atualizar branch com conteudo de outra branch
   Vamos supor que você está trabalhando com 3 branchs: *master, branch1, branch2*

   **Vamos criar uma outra branch chamada *juntar_branchs* e vamos entrar nela** e fazer o merge dessas branchs dessa maneira:

   `git checkout -b juntar_branchs` #para criar a branch e entrar nela
   `git merge branch1` #junta a branch1 com a branch atual
   `git merge branch2` #junta a branch2 com a branch atual

    
    [https://cursos.alura.com.br/forum/topico-estou-com-duvida-no-processo-de-criar-uma-branch-nova-e-depois-atualizar-ela-e-fazer-o-merge-33955]




# Atualizar senha de autenticação no git
**ERRO**:
_remote: HTTP Basic: Access denied_
_fatal: Authentication failed_

**CORREÇÃO**
Para corrigir é simples, porém a solução não se encontra tão facilmente pela internet. 
- Abra o Menu Iniciar do Windows e 
- procure por Gerenciador de Credenciais.
- Ao abrir a janela do Gerenciador, clique em Credenciais do Windows.
- Abaixo na lista de credenciais, irá existir as várias credenciais salvas pelo Windows, dentre elas uma lista de credenciais genéricas, que é onde as credenciais do GitLab são salvas. Basta identificar a linha referente ao seu repositório e excluí-la, ou atualizar a senha ali mesmo.
Image for post
Gerenciador de Credenciais do Windows, navegador até lista de credenciais genéricas
Pronto, problema resolvido, basta rodar o comando para clonar seu repositório novamente!