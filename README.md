
# Resumos de git e github

Coisas para não esquecer sobre git e github

1 - procurar na documentação para criar acesso por ssh

## 😊 a preencher

## comandos git
´´´git init´´´
cria um novo repositorio .git na pasta em que esta acessando
´´´rm -rf .git´´´
remove o diretorio .git da pasta em que esta acessando
´´´echo NomeDoArquivo > .gitignore ´´´
.gitignore serve para excluir/ignorar as pastar ou arquivos(criara um documento com a lista)
´´´git status´´´
mostra quais pastas/arquivos não foram sicronizados com o git
´´´touch NomeDoDiretorio/.gitkeep´´´
cria um arquivo .gitkeep que serve para o git status reconhecer uma pasta vazia(que agora n esta vazia)
´´´git add .NomeDoArquivo´´´
sicroniza o arquivo ao git, se usar (git add .) sicroniza todos arquivos

### git commits comandos
´´´git commit -m"MENSAGEM QUE DESCREVE A ALTERAÇÂO"´´´
adiciona um uma mensagem a alteração
´´´git commit --amend -m"alteração do texto da ultima alteração"
altera a descrição do texto da ultima commit -m""
´´´git log´´´ 
mostra os logs de commit
´´´git reset --soft CommittName´´´
Desfaz a criação dos commits posteriores a esse ponto, mas não os exclui, mas adiciona ao branch (eles podem ser visto usando git status)
´´´git reset --mixed CommittName´´´
Desfaz a criação dos commits posteriores a esse ponto, mas não os exclui, não os adiciona ao branch (eles podem ser visto usando git status)
´´´git reset --hard CommittName´´´
Desfaz a criação dos commits posteriores a esse ponto, e não os exclui
## comandos diretorio
´´´mkdir NomeDoArquivo´´´ 
cria uma nova pasta no diretorio


## ERROS
# GIT
erro ao usar 'git log' onde aparece 'END' ao final, aperte 'q'

