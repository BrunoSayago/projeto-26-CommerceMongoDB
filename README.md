# Projeto 26 - MongoDB Commerce

Oi. Este foi um dos projetos que eu fiz durante meu curso na Trybe. Confira os detalhes dele abaixo.




## Nome do Projeto
MongoDB Commerce (Comércio em MongoDB)

## Linguagens e Ferramentas Utilizadas

 - Shell
 - JavaScript
 - [MongoDB](https://www.mongodb.com/)
 - [Docker](https://www.docker.com/)

## Objetivos do Projeto
Neste projeto foram feitas manipulações em um banco de dados MongoDB, que continha dados de um cardápio do McDonald's. Ao todo, foram escritos 32 funções de manipulação dos dados. O objetivo foi colocar em prática todo conhecimento adquirido sobre mongoDB. Além disso, durante o bloco, foi possível entender o que é um banco de dados não relacional e para que serve, entender como recuperar dados de um banco de dados não relacional, entender como modelar dados de uma aplicação para um banco de dados não relacional e também entender como manipular dados com queries no MongoDB.

<br/>
## Docker
Foi utilizado o docker para se conectar ao banco de dados MongoDB. Para isso, após a cópia do diretório para o arquivo local, acessou-se o terminal na pasta raíz do projeto, e criou-se um container do mongo, utilizando o código:
<br/>

- `docker run -d --name=nomeDoContainer -v "$PWD:/app" -p 27017:27017 mongo:5.0`

<br/>
Onde "nomeDoContainer" é escolhido pelo usuário. Com o container em execução, foi acessado o terminal do container, com o comando:
<br/>

- `docker exec -it nomeDoContainer bash`

<br/>
Dentro do terminal do container, foi acessado o diretório "/app". Então, roda-se o comando:
<br/>

- `DBNAME=commerce ./scripts/resetdb.sh assets/produtos`

<br/>
Que restaura o banco de dados. A execução desse script criará um banco de dados chamado `commerce` e importará os dados para a coleção `produtos`.
Após esses passos, os códigos escritos no diretório "/challenges" podem ser escritos no shell do mongoDB para serem executados.
 
