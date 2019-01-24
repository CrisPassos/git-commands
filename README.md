# git-commands
Esse repositório visa listar os comandos e utilizações do GIT.

# Configurando o GIT

<b>git config --global user.name 'nome do usuario' </b> = cria um usuário global.

<b>git config --global user.email 'testes@email' </b> = configura um e-mail global.

<b>git init </b> = transforma o diretório atual em um repositório do GIT (cria-se um arquivo .git).

# Comandos mais utilizados

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






## Fazer em outro Note
git remote add origin https://github.com/NomeConta/Projeto.git = connecta os meus arquivos localmente ao  que criei no repositório GIT

git clone https://github.com/NomeConta/Projeto.git = clona o código que está no repositório

git log -n 2 = mostra o log dos dois últimos commits

git log --oneline = exibe todos os commits por comentários

git log --stat = exibe qual arquivo foi alterado


#Verificando mudanças nos arquivo
git diff = exibe o conteúdo que está diferente mas ainda não foi para a master

git diff <numero-commit> = exibe o conteúdo que foi modificado e já está no stage

git diff <commit-inicio> .. <commit-final> = exibe o que foi modificado entre um range de commits

git diff <numero-commit>2 = exibe as mudan;as nos arquivos do commit em relação aos dois commits anteriores

#Remove Arquivo
git rm <nome-arquivo> = remove o arquivo

#Renomeando e movendo arquivos
git mv filmes.txt comandos.txt = renomeia o nome do arquivo
git mv principal.js js/principal.js = move o arquivo para uma pasta chamada js(é preciso que a pasta js já tenha sido criada)

#Desfazendo mudanças
git checkout --comandos.txt = desfaz as alterações ainda não rastreadas, ou seja, que ainda não estão na área de stage, voltando ao 
conteúdo anterior do arquivo. Podemos utilizar o comando git checkout para recuperar os arquivos removidos acidentalmente

git reset = retira o arquivo da stage mas preserva tudo o que foi modificado nesse arquivo.

git reset --hard = descarta todas as mudanças nos arquivos ao invorcarmos esse comando. 

--hard retira todas as alterações fica como se estivesse no último commit

#Desfazendo mudanças já comitadas
git revert --no-edit <ultimo-commit> = defaz as alterações no repositório


#Repositório remoto
git init --bare <nome-repositorio.git> = criação de um repositorio local. --bare serve para que o GIT nao crie um working tree
impedindo que commits sejam efetuados diretamente no servidor

git remote add servidor file://nome-do-caminho.git = mostra ao git qual o caminho do repositorio remoto está.

git clone file://nome-do-caminho.git = faz um clone do projeto que está no servidor local da máquina

git pull servidor master = sincroniza com o repositorio local do servidor

