# BRANCH
| `git checkout -b NomeDaBranch`    | Cria uma nova branch e já muda para ela |
| `git branch`                      | Mostra qual é a branch em que estamos trabalhando |
| `git branch -a`                   | Retorna as branch locais e remotas |

_Exemplo:_ 
    Vamos criar e nomear o nosso novo branch como «style».
    EXECUTE:
    `git checkout -b style`
    `git status`

   :exclamation: Nota: `git checkout -b <branch name>` é o atalho de `git branch <branch name>` seguido por `git checkout <branch name>`.

   :exclamation: Note que o comando `git status` avisa que você está no branch style.

# CONFIGURAÇÃO
| `git config --global core.editor vim`             | muda o editor padrão para ser o vim |
| `git config --global user.email nome@serv.kkk`    | mudar e-mail  | 
| `git config --global -l`                          | retorna as variaveis  configuradas | 


# TAG
| `git tag` |  lista tags disponiveis |
| `git tag -l " V1.85*"` | busca apenas a série 1.85 |





# REBASE
 - o rebase em resumo é fazer um git checkout na master.
 - faz um git pull pra ter as ultimas modificacoes da master.
 - ae voce faz git rebase <sua branch>
 
 _exemplo_
    faz um `git push -f` - pra branch de trabalho qdo estiver dentro dela;
    ele refaz sua linha de commit da tua branch
    com o q entrou na master


# REPOSITÓRIOS
| `git pull`    | atualiza repositório local | 

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