**Running with Docker-Compose**

- In the root directory of the project run "**docker-compose up**" command.
- Wait all containers to start.
- Browse React UI -> http://localhost:5001/

**Some Notes**
- api service keeps waiting till mssql container ready to accept connections. This waiting feature was implemented with wait-for-it.
(https://github.com/vishnubob/wait-for-it)
- redis and rabbitmq containers are faster than mssql container on starting and accepting connections.That's why api service waits only mssql.
- mssql, redis and rabbitmq volumes are exist and active by defauls in docker-compose.yml

**Todo**
- React hot-loading for development environment (It works on linux host but not in windows. Any help?)

## Sample Screencast

![alt text](https://github.com/suadev/docker-workshop-with-react-aspnetcore-redis-rabbitmq-mssql/blob/master/react_ui/public/screencast.gif)

### Overall Architecture

![alt text](https://github.com/suadev/docker-workshop-with-react-aspnetcore-redis-rabbitmq-mssql/blob/master/react_ui/public/docker_workshop.png)
