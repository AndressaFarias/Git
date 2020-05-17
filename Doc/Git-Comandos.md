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

