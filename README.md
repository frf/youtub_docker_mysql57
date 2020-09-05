## Docker Mysql

Criando banco de dados com container docker (Mysql)

Dados de acesso padrão 

- MYSQL_DATABASE: laravel
- MYSQL_ROOT_PASSWORD: 123456

Comndos de acesso ao container

- docker ps (Listar Containers)
- docker-compose up -d (Subir Container em Background)
- docker-compose up (Subir Container)
- docker exec -it <nome do container> bash (Entrar dentro do container)


## Deletar Tudo para não ocupar muito espaço na sua maquina

Lembrando que ao deletar quando for subir novamente ele vai demorar um pouco pois vai precisar baixar novamente a imagem.

Individual
- docker rmi -f <name>
- docker rm -f <name>
- docker volume rm <name>

Todos
- docker rmi -f $(docker images -q)
- docker rm -f $(docker ps -a -q)
- docker volume rm $(docker volume ls -q)
