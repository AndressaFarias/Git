# Comandos Git

## erificar a branch
`git branch`


## Crie um branch
Vamos nomear o nosso novo branch como «style».

EXECUTE:

~~~
git checkout -b style
git status
~~~

:exclamation: Nota: `git checkout -b <branch name>` é o atalho de `git branch <branch name>` seguido por `git checkout <branch name>`.

:exclamation: Note que o comando `git status` avisa que você está no branch style.

`git branch -a` - verificando as branch locais e remotas

## Navegando nas branches
`git branch`- mostras a branch em que estamos trabalhando
`git branch -a`-mmostras as branches remotas

## atualizar repositório local
`git pull`
O comando git pull é usado para buscar e baixar conteúdo de um repositório remoto e atualizar imediatamente o repositório local. 


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