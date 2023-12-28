
# Resumos de git e github

Coisas para não esquecer sobre git e github

1 - procurar na documentação para criar acesso por ssh

2 - com github aberto, apertando a tecla "." abre o editor do github no navegador

3 - diretorio `origin/branch` é um diretorio remoto

# INICIANDO O GIT
`git config --list`
Lista as configurações do git

`git config --global user.name "Nome Sobrenome"`
`git config --global user.email seuemail@email.com` 
configura o nome e email do usuario git, serve para ser registrado nos commits

`git config --global init.defaultBranch main` 
Define o nome da branch padrão para main

`git clone URLdoDiretorio`
Clona um diretorio do git hub, fazendo assim o link entre diretorio remoto e local.

## COMANDOS GIT

`git init`
cria um novo repositorio .git na pasta em que esta acessando

`rm -rf .git`
remove o diretorio .git da pasta em que esta acessando

`git status`
mostra quais pastas/arquivos não foram sicronizados com o git

`git add NomeDoArquivo`
adiciona arquivos não rastreados o branch, se usar `git add .` adiciona todos arquivos nao rastreados

`git reset NomeDoArquivo`
remove o arquivo do branch

`git restore --staged <file>`
remove o arquivo do branch

`git remote add origin <httpdorepositorioremoto>`
Faz uma ligação entre o git local com o git remoto

### GIT REPOSITORIOS

`git push -u origin nomeDoBranch`
Envia para o diretorio remoto (git hub) a ultima versão do branch escolido. Ex: `git push origin main` envia a ultima atualização do branch main. Esse comando também cria o branch no diretorio remoto caso ainda não exista. Apos isso pode-se usar apenas `git push`

`git pull`
Recebe as atualizações feita no github remoto para o git local.

`git fetch origin NomeDaBranch`
Baixa do diretorio remoto apenas as ultimas mudanças feitas, mas não aplica nos arquivos do diretorio local

`git diff oldBranch nemBranch`
Mostra as mudanças feitas entre duas branchs (maisVelha Vs maisNova)

`git stash`
Salva modificações feitas temporariamente e as remove do diretorio.

`git stash apply`
Aplica as modificações salvas.

### GIT BRANCH
`git checkout nomeDoBranch`
Seleciona o branch a ser trabalhado

`git checkout -b nomeDoBranch`
Cria um novo branch com o nome selecionado

`git checkout -f nomeDoBranch`
Força a troca de branch, o git desconsidera as entradas feitas que o merge não foi realizado

`git merge nomeDoBranch`
Faz o Merge do branch atual com o branch selecionado.

`git branch`
Lista as branchs do repositorio. O asterisco aponta em qual branch estamos trabalhando

`git branch -v` 
Lista as branchs com os seus ultimos commits

`git branch -d nomeDoBranch`
Deleta a branch pedida

`git clone URLdoRepositorio --branch NomeDaBranch --single-branch`
clona uma branch especifica de um repositorio, se não for indicado nome da branch, irá clonar a main

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

`git restore`
Desfaz as ultimas modificações até o ultimo commit

## COMANDOS DE DIRETORIO

`mkdir NomeDoArquivo` 
cria uma nova pasta no diretorio

`touch NomeDoDiretorio/.gitkeep`
cria um arquivo .gitkeep que serve para o git status reconhecer uma pasta vazia(que agora n esta vazia)

`touch NomeDoDiretorio/arquivo`
adiciona um arquivo ou mais arquivos. Ex: $ touch resumos/aula-01.md resumos/aula-02.md (cria dois arquivos dentro da pasta resumos)

`echo "textoDentroDoArquivo" > NomeDoArquivo.Extenção`
O comando echo adiciona um novo arquivo ao diretorio. Por exemplo: `echo "boas festas" > mensagem_finalDeAno.txt` cria um arquivo com nome messagem_finalDeAno.txt com a escrita 'boas festas' dentro.

`echo NomeDoArquivo > .gitignore `
.gitignore serve para excluir/ignorar as pastar ou arquivos(criara um arquivo de texto com com a lista de arquivos que vão ser ignorados)


### GIT ALIASES
`$ git config --global alias.nomeDaAbreviação NomeDoComando`
O aliases serve para criar apelidos para certos comandos dentro do git, por exemplo para o comando status sendo abreviado para st assim: `git st` funciona como `git status` através do comando: `$ git config --global alias.st status` 

`$ git config --global --unset alias.nomeDaAbreviação` 
Remove o apelido criado.

## ERROS
### GIT
erro ao usar `git log` onde aparece 'END' ao final, aperte 'q'

