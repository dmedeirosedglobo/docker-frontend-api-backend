Uma demostração de uma aplicação simples com 3 camadas

* frontend na docker network `frontend`
* API na mid-tier em duas docker networks `frontend` e `backend`
* backend banco de dados em mongodb para a aplicação na docker network `backend`

![image-20230816-201010](https://github.com/dmedeirosedglobo/docker-frontend-api-backend/assets/114950111/79610834-0260-4f0b-9864-c433780751b6)


Para rodar esta aplicação em seu ambiente docker, é simples, ```docker-compose up --build``` no prompt de comando. O Docker realizará o build das imagens, incluíndo a instância do [MongoDB](https://www.mongodb.com/) do repositório [mongo](https://hub.docker.com/_/mongo). A api usa a imagem [nodejs](https://nodejs.org/) com [express](http://expressjs.com/) com build pela imagem base [node:alpine](https://hub.docker.com/_/node). O frontend usa [ReactJS](https://reactjs.org/) com base na imagem [node:alpine](https://hub.docker.com/_/node).
