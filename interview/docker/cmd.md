
| Команда                                 | Описание                                    |
| --------------------------------------- | ------------------------------------------- |
| `docker pull <image>`                   | Загрузить образ из реестра                  |
| `docker build -t <name> .`              | Собрать образ из Dockerfile                 |
| `docker run <image>`                    | Запустить контейнер из образа               |
| `docker ps`                             | Список запущенных контейнеров               |
| `docker ps -a`                          | Список всех контейнеров                     |
| `docker stop <container>`               | Остановить контейнер                        |
| `docker rm <container>`                 | Удалить контейнер                           |
| `docker images`                         | Список образов                              |
| `docker rmi <image>`                    | Удалить образ                               |
| `docker exec -it <container> <command>` | Выполнить команду в работающем контейнере   |
| `docker logs <container>`               | Просмотр логов контейнера                   |
| `docker-compose up`                     | Запустить сервисы из docker-compose.yml     |
| `docker-compose down`                   | Остановить сервисы из docker-compose.yml    |
| `docker network create <name>`          | Создать сеть                                |
| `docker volume create <name>`           | Создать том                                 |
| `docker inspect <container>`            | Подробная информация о контейнере           |
| docker attach <container_id>            | Позволяет подключиться к консоли контейнера |
