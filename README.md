# git-commands
Esse repositório visa listar os comandos e utilizações do GIT

# Configurando o Usuário do GIT

<b>git config --global user.name nome do usuario </b> = cria um usuário global

git config --global user.email "testes@email" = configura um e-mail global

git init = transforma o diretório atual em um repositório do GIT (é criado um arquivo .git)

git status = exibe os arquivos que estão no stage (antes do commit)

git add nomeArquivo.txt = adiciona um arquivo na área de stage 

git add . = adiciona todos os arquivos novos na área de stage

git commit -m 'Initial Commit' = comita o arquivo para o stage (-m insere o comentário)

git commit -am 'Initial Commit' = comita o arquivo para o stage (-m insere o comentário -a adciona no stage o que foi alterado, porém se for algo novo é necessário colocar o comando de add)

git log = verifica o histórico das alterações exibe os commits realizados

git remote add origin https://github.com/NomeConta/Projeto.git = connecta os meus arquivos localmente ao  que criei no repositório GIT

git push origin master = envia as alterações locais para o repositório (origin <branch> insere na branch desejada)

git push = envia as alterações locais para o repositório

git pull origin master = pega todas as informações que estão localmente

git push -f origin <branch> = envia as alterações sobrescrevendo o que está na branch pelo o que está localmente

## Fazer em outro Note
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

