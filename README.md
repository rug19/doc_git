# Documentação git

Documentação do git para ajudar nos comandos
## O que é um repositório?
Basicamente, um repositório é um local de armazenamento do nosso código-fonte. É nele que nossos códigos serão armazenados e versionados.
Com o GIT, existem dois tipos de repositórios:

Local: Um repositório onde os códigos são armazenados e versionados localmente, sem a necessidade de um serviço externo;
Remoto: Um repositório onde os códigos são armazenados e versionados remotamente, utilizando serviços como Github, Bitbucket ou Gitlab (que serão vistos posteriormente).
## Estados de um arquivo
Um arquivo gerenciado pelo git possui três estados e o entendimento destes são fundamentais. Basicamente, os estados são:
Modificado: Um arquivo possui o estado de modificado quando há alguma alteração, seja ele em seu conteúdo, adicionado ou removido;
Preparado: Um arquivo possui o estado de preparado quando ele é adicionado ao versionamento utilizando o comando git add. É com este comando que adicionamos o arquivo e permitimos que o git o versione;
Consolidado: Após serem modificados (adicionados, removidos ou alterados) e preparados (adicionados ao versionamento), o último passo de um arquivo é sua consolidação. Neste ponto, ao utilizamos o comando git commit, estamos salvando as alterações do arquivo e o versionando, mantendo um histórico de suas alterações.
Sendo assim, a imagem abaixo ilustra como funciona todo este processo:

![imagem git](https://github.com/rug19/doc_git/assets/67665127/9d345c03-ab05-4305-9d88-0917bd47ba32)


## Ele inicia o arquivo (repositorio)".git/" para controlar a pasta:
````
git init
````
## Verifica o status de todos os arquivos dentro do repositorio e  é responsavel por validar os arquivos modificados dentro do projeto. Em vermelho ele mostra os arquivos modificados. Em verde mostra os arquivos que foram adicionado pelo "git add":
````
git status
````
## Ele é responsavel por colocar o arquivo modificado em uma area segura:
````
git add
````
## Ele é responsavem por colocar todos os arquivos em uma area segura:
````
git add .
````
## Ele é responsavel por criar uma nova versão do projeto com as referências do criador:
````
git commit -m "texto_da_modificação"
````
## Ele é responsavel por criar uma nova versão do projeto com as referências do criador:
````
git commit -m "texto_da_modificação"
````
## validar os meus comentários e modificações:
````
git log
````
## Cria uma nova branch ou ramo:
````
git checkout -b <nome_da_branch>
````
## Muda de branch /ramo:
````
git checkout <nome_da_branch>
````
## Ele adiciona a branch atual o conteúdo de outra branch:
````
git merge: <nome_de_branch>
````
## Baixa o projeto do repositorio:
````
git clone: <url>
````
## Ele envia alteração para o repositorio:
````
git push
````
## Ele puxa as alterações do repositorio:
````
git pull
````
## Ele lista os arquivos que possuem dentro do diretório:
````
ls
````
## Ele lista detalhadamente mostrando hora, mês  e data dos arquivos do repositório:
````
ls -l
````
## Ele desfaz o que foi feito em um commit e cria um novo commit para o repositório, porén ele não exclui o commit desfeito. 
````
git revert + identificador do commit

````
Possiveis erros no git revert:

$ git revert 383177df7e94c78a32626b2712ade2aff66b6c02
CONFLICT (modify/delete): cadastro.html deleted in parent of 383177d (adicionand
o o arquivo cadastro.html) and modified in HEAD.  Version HEAD of cadastro.html
left in tree. 
error: could not revert 383177d... adicionando o arquivo cadastro.html

A idéia do revert é desfazer alterações feitas no commit em questão e voltar para a versão anterior, porém provavelmente nesse caso tem outro commit que modificava esse arquivo, o que impedia o git de voltar ao commit inicial. Nesses casos o git acusa que há conflitos e trava o revert, assim é necessário que você abra o arquivo que tem conflito e verifique qual das alterações deseja aplicar. é preciso entrar no arquivo e arrumar os conflitos utilizar o git add para adiconar o arquivo e utilizar o git revert --continue para continuar o processo. 

## Ele é um editor de texto para terminal e consegue adicionar um arquivo um aquivo dentro do repositório.
````
nano "index.html"
````
## Possiveis erros: 

403: Apagando as credenciais, gerenciamento de credenciais.


## Configurações do usuário do git:
Para que os commits feitos possuam nosso nome e e-mail em seu escopo, precisamos realizar esta configuração.
Para isso, no terminal (macOS ou Linux) ou Git Bash (Windows), digite os seguintes comandos:

````
git config --global user.name "seu_nome"
````
````
git config --global user.email "seu_email"
````
Com isso, todos os commits feitos no computador terão nosso e-mail e nome como autores.
