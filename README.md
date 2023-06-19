# Documentação git

Documentação do git para ajudar nos comandos

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

## Possiveis erros: 

403: Apagando as credenciais, gerenciamento de credenciais.


## Configurações do usuário do git:

````
git config --global user.name "seu_nome"
````
git config --global user.email "seu_email"
````
