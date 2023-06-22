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

## Utilizando HTTPS para comunicação
O protocolo HTTPS é o mais fácil e prático para ser utilizado no Github. Para isso, não há a necessidade de nenhuma configuração adicional. Apenas com o link do repositório é possível realizar esta comunicação, desde que você possua permissão de acesso ao repositório.
## Utilizando SSH para comunicação.
O processo de comunicação com o Github utilizando o SSH é mais complexo que utilizando HTTPS. Para isso, precisamos gerar as chaves SSH e adicioná-las ao nosso perfil do Github. Sendo assim, vamos ao passo-a-passo:

1 - Para gerar uma nova chave SSH, o primeiro passo é, no terminal (ou Git Bash) utilizar o seguinte comando: ssh-keygen -t rsa -b 4096 -C "your_email@example.com", onde você deve substituir o email e adicionar o utilizado no github.
2 - Após isso, será perguntado onde você deseja salvar a chave SSH. Neste ponto, pode clicar em "enter", o destino padrão já é suficiente.
3 - Feito isso, será solicitado uma chave secreta. Esta chave é utilizada em conjunto com o hash para gerar sua chave SSH. Pode adicionar qualquer frase (desde que você se lembre, haha).
4 - Com isso, sua chave foi gerada. O próximo passo é adicioná-la ao nosso perfil do github.
Agora, com as chaves SSH geradas, vamos adicioná-la ao github. Para isso, vamos ao passo-a-passo:

1 - Ao realizar o login, vamos até a seguinte rota: https://github.com/settings/keys Na página, clicamos em "NEW SSH KEY".
2 - Agora, voltando ao terminal, precisamos copiar nossa chave gerada anteriormente.
3 - Caso você utilize o macOS, no terminal (ou git bash), digitamos o seguinte comando: pbcopy < ~/.ssh/id_rsa.pub.
4 - Caso você utilize o Windows, no gitbash, digitamos o seguinte comando: clip < ~/.ssh/id_rsa.pub.
5 - Caso você utilize o Linux, no terminal, digitamos os seguintes comandos: sudo apt-get install xclip e xclip -sel clip < ~/.ssh/id_rsa.pub.
6 - Feito isso, a chave ssh estará em nossa área de transferência. Agora, voltamos à página aberta do Github (https://github.com/settings/keys ) e colamos a chave, conforme a imagem abaixo:

![imagem git](https://d2v0x26thbzlwf.cloudfront.net/prod/527/img/rId15uih22wf4.enz.png)

Feito isso, já podemos salvar e a chave já está configurada.
O último passo é testar a comunicação. Para isso, no terminal (ou gitbash), utilizamos o seguinte comando: ssh -T git@github.com. Será solicitado que digitemos, então, a chave secreta que utilizamos ao criar a chave ssh no processo anterior. Ao fazer isso, a comunicação será feita com sucesso e nossa chave estará configurada:

![imagem git](https://d2v0x26thbzlwf.cloudfront.net/prod/527/img/rId17jbhg53xl.ocz.png)

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
## Baixa o projeto do repositório de uma branch especifica.
````
git clone -b <nome_da_branch> <url_do_repositório>
````
## Ele envia as alterações para o repositorio:
````
git push
````
## Ele puxa as alterações do repositorio:
````
git pull
````
## Ele envia o repositorio local para o repositorio online do github. Este comado é quando você precisa fazer a ligação com o repositório online do github. 
````
git remote add origin "url" do repositório
````
## É utilizado quando queremos enviar a branch que criamos para o repositório remoto. Isso criará um “elo” entre o seu repositório local e o repositório remoto.
````
git push origin "branch"
````
## Abri um repositório clonado diretamente no visual code através do terminal.
````
code <caminho-do-repositório>
````
## Ele cria um novo repositório caso não tenha nenhum criado
````
echo "#nome_do_repositorio" >> README.md
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
## Ele é um editor de texto para terminal e consegue adicionar um arquivo um aquivo dentro do repositório.
````
nano "index.html"
````
## Possiveis erros: 

- Erro 403: Ir em gerenciador de crendeciais > crendeciais do windows > apagar as crendenciais do github. 
  
- Erro: failed to push some refs to <repositório>. Esse ocore quando querendo enviar diretamenteas alterações para a branch principal maim.
  
![WhatsApp Image 2023-06-22 at 08 44 08](https://github.com/rug19/doc_git/assets/67665127/a61b9d38-782d-4ac8-9f56-e1ce8d67e147)

Para enviar o commit diretamente para a branch principal "main" é necessário primeiro da um git pull para puxar os arquivos do repositório remoto para depois da um git push para enviar juntamente com o arquivo adicionado. 

- Error: could not revert 383177d... adicionando o arquivo cadastro.html

CONFLICT (modify/delete): cadastro.html deleted in parent of 383177d (adicionand
o o arquivo cadastro.html) and modified in HEAD.  Version HEAD of cadastro.html
left in tree. 
A idéia do revert é desfazer alterações feitas no commit em questão e voltar para a versão anterior, porém provavelmente nesse caso tem outro commit que modificava esse arquivo, o que impedia o git de voltar ao commit inicial. Nesses casos o git acusa que há conflitos e trava o revert, assim é necessário que você abra o arquivo que tem conflito e verifique qual das alterações deseja aplicar. é preciso entrar no arquivo e arrumar os conflitos utilizar o git add para adiconar o arquivo e utilizar o git revert --continue para continuar o processo.

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
