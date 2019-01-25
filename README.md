# git-commands
Esse repositório visa listar os comandos e utilizações do GIT.

## Configurando o GIT

<b>git config --global user.name 'nome do usuario' </b> = cria um usuário global.

<b>git config --global user.email 'testes@email' </b> = configura um e-mail global.

<b>git init </b> = transforma o diretório atual em um repositório do GIT (cria-se um arquivo .git).

## Comandos mais utilizados

<b> git status </b> = exibe os arquivos que estão no stage (antes do commit).

<b> git add nomeArquivo.txt </b> = adiciona um arquivo na área de stage. 

<b> git add . </b> = adiciona todos os novos arquivos na área de stage.

<b> git commit -m 'Initial Commit' </b> = faz o commit das alterações e envia os arquivos para a área do stage (-m insere o comentário).

<b> git commit -am 'Initial Commit' </b> = faz o commit das alterações e envia o arquivo para o stage (-m insere o comentário -a adiciona no stage o que foi alterado, sem a necessidade de usar o comando 'git add' porém se for algo novo é necessário colocar o comando de add).

<b> git log </b> = verifica o histórico das alterações e exibe os commits que foram realizados.

<b> git push origin 'branch' </b> = envia as alterações locais para o repositório (origin 'branch' insere o commit na branch desejada).

<b> git push </b> = envia as alterações locais para o repositório remoto.

<b> git push -f origin 'branch' </b> = envia as alterações sobrescrevendo o que está na branch pelo o que está localmente.

<b> git pull origin 'branch' </b> = pega todas as informações que foram commitadas no repositório (origin 'branch' insere o commit na branch desejada).

## Repositório remoto
<b> git remote add origin https://github.com/NomeConta/Projeto.git </b> = connecta os meus arquivos localmente ao  repositório criado no GITHUB.

<b> git clone https://github.com/NomeConta/Projeto.git </b> = faz um clone do código que está no repositório.

<b> git init --bare 'nome-repositorio.git' </b> = criação de um repositorio local ( --bare serve para que o GIT nao crie um working tree).

<b> git log -n 2 </b> = mostra o log dos dois últimos commits (eu posso alterar o valor 2).

<b> git log --oneline </b> = exibe todos os commits por comentários.

<b> git log --stat </b> = exibe qual arquivo foi alterado.

<b> git remote add servidor file://nome-do-caminho.git </b> = mostra ao git qual o caminho do repositorio remoto está. (Este caso serve para quando outro computador serve de servidor do repositório).

<b> git clone file://nome-do-caminho.git </b> = faz um clone do projeto que está no servidor local da máquina (Este caso serve para quando outro computador serve de servidor do repositório).

<b> git pull servidor master </b>= sincroniza com o repositorio local do servidor.

## Verificando mudanças nos arquivo
<b> git diff </b> = exibe o conteúdo que está diferente mas ainda não foi para o stage.

<b> git diff 'numero-commit' </b> = exibe o conteúdo que foi modificado e já está no stage.

<b> git diff 'commit-inicio' .. 'commit-final' </b> = exibe o que foi modificado entre um range de commits.

<b> git diff 'numero-commit'2 </b> = exibe as mudanças nos arquivos do commit em relação aos dois commits anteriores.

## Remove Arquivo
<b> git rm 'nome-arquivo' </b> = remove o arquivo.

## Renomeando e movendo arquivos
<b> git mv filmes.txt comandos.txt </b> = renomeia o nome do arquivo'.
<b> git mv principal.js js/principal.js </b> = move o arquivo para uma pasta chamada js(é preciso que a pasta js já tenha sido criada).

## Desfazendo mudanças
<b> git checkout --comandos.txt </b> = desfaz as alterações ainda não rastreadas, ou seja, que ainda não estão na área de stage, voltando ao 
conteúdo anterior do arquivo. Podemos utilizar o comando git checkout para recuperar os arquivos removidos acidentalmente.

<b> git reset </b> = retira o arquivo da stage mas preserva tudo o que foi modificado nesse arquivo.

<b> git reset --hard </b> = descarta todas as mudanças nos arquivos ao invorcarmos esse comando. (--hard retira todas as alterações fica como se estivesse no último commit).

## Desfazendo mudanças já comitadas
<b> git revert --no-edit 'ultimo-commit' </b> = defaz as alterações no repositório.

## Trabalhando com Branches
<b>git branch</b> = lista as branches em nosso repositório. (o * na frente indica que é a branch atual).

<b>git branch -v</b> = lista as branches existentes no nosso repositórios commitados.

<b>git log --oneline --decorate --parents</b> = exibe o histórico resumido do nosso repositório com o commit para o qual a branch está apontando e os commits pai de cada commit (--parents commits pais, --decorate verifica qual é o commit que a branch está apontando).

<b>git branch 'nome da branch'</b> = cria uma nova branch.

<b>git checkout 'nome da branch'</b> = troca de branch.

<b>git checkout -b 'nome da branch'</b> = cria uma nova branch e já troca o apontamento dela.

<b>git branch -d 'nome da branch'</b> = deleta uma branch.

<b>git branch -D 'nome da branch'</b> = deleta uma branch, caso já tenhamos feito um commit.

<b></b>

<b></b>

<b></b>


## Refências
