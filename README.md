
# Resumos de git e github

Coisas para não esquecer sobre git e github

1 - procurar na documentação para criar acesso por ssh

2 - com github aberto, apertando a tecla "." abre o editor do github no navegador

## 😊 a preencher

# comandos git
`git init`
cria um novo repositorio .git na pasta em que esta acessando

`rm -rf .git`
remove o diretorio .git da pasta em que esta acessando

`git status`
mostra quais pastas/arquivos não foram sicronizados com o git

`touch NomeDoDiretorio/.gitkeep`
cria um arquivo .gitkeep que serve para o git status reconhecer uma pasta vazia(que agora n esta vazia)

`git add NomeDoArquivo`
adiciona arquivos não rastreados o branch, se usar `git add .` adiciona todos arquivos nao rastreados

`git reset NomeDoArquivo`
remove o arquivo do branch

`git restore --staged <file>`
remove o arquivo do branch

`git remote add origin <httpdorepositorioremoto>`
Faz uma ligação entre o git local com o git remoto

`git push -u origin nomeDoBranch`
Envia para o diretorio remoto (git hub) a ultima versão do branch escolido. Ex: `git push origin main` envia a ultima atualização do branch main. Esse comando também cria o branch no diretorio remoto caso ainda não exista. Apos isso pode-se usar apenas (eu acho, precisa de mais testes) `git push`

`git pull`
Recebe as atualizações feita no github remoto para o git local.

### GIT BRANCH

`git checkout -b nomeDoBranch`
Cria um novo branch

`git merge nomeDoBranch`
Faz o Merge da brench com a main

`git branch`
Lista as branchs do repositorio. O asterisco aponta em qual branch estamos trabalhando

`git branch -v` 
Lista as branchs com os seus ultimos commits

`git branch -d nomeDoBranch`
Deleta a branch pedida


### GIT COMMITS COMANDOS

`git commit -m"MENSAGEM QUE DESCREVE A ALTERAÇÂO"`
adiciona um uma mensagem a alteração
`git commit --amend -m"alteração do texto da ultima alteração"
altera a descrição do texto da ultima commit -m""

`git log` 
mostra os logs de commit

`git reset --soft CommittName`
Desfaz a criação dos commits posteriores a esse ponto, mas não os exclui, mas adiciona ao branch (eles podem ser visto usando git status)

`git reset --mixed CommittName`
Desfaz a criação dos commits posteriores a esse ponto, mas não os exclui, não os adiciona ao branch (eles podem ser visto usando git status)

`git reset --hard CommittName`
Desfaz a criação dos commits posteriores a esse ponto, e não os exclui

## COMANDOS DE DIRETORIO

`mkdir NomeDoArquivo` 
cria uma nova pasta no diretorio

`touch NomeDoDiretorio/arquivo`
adiciona um arquivo ou mais arquivos. Ex: $ touch resumos/aula-01.md resumos/aula-02.md (cria dois arquivos dentro da pasta resumos)

`echo "textoDentroDoArquivo" > NomeDoArquivo.Extenção`
O comando echo adiciona um novo arquivo ao diretorio. Por exemplo: `echo "boas festas" > mensagem_finalDeAno.txt` cria um arquivo com nome messagem_finalDeAno.txt com a escrita 'boas festas' dentro.

`echo NomeDoArquivo > .gitignore `
.gitignore serve para excluir/ignorar as pastar ou arquivos(criara um arquivo de texto com com a lista de arquivos que vão ser ignorados)

## ERROS
### GIT
erro ao usar `git log` onde aparece 'END' ao final, aperte 'q'

