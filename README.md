## Подготовка

Перед запуском сервера необходимо поместить в переменную окружения `LOGS_DIRECTORY` абсолютный путь до директории, в которой будут сохраняться **LOG-файлы**. Важно, чтобы такая директория существовала на вашем локальном компьютере. Для этого выполните команду: 

Linux/MacOS:

    export LOGS_DIRECTORY="/Absolute/Path/For/Logs/Dir/"
    
Windows:
    
- Зайдите в файл `docker-compose.yaml` 
- Найдите поле `source` у объекта `webserver`
- Замените ${LOGS_DIRECTORY} на  /Absolute/Path/For/Logs/Dir/
    
#### Примечание:
В пути до директории обязательно должен присутствовать последний слеш. При указании "/Absolute/Path/For/Logs/Dir" контейнер запущен не будет. 
 
## Запуска сервера
 
Далее для запуска серверной части необходимо выполнить из основной директории проекта команду:

    docker compose up --build -d
    
После выполнения команды, по окончании сборки контейнера, сайт будет доступен по адресу: `http://localhost:3000/`

## Выключение сервера

Для того, чтобы прекратить работу сервера, можно выполнить команду:
    
     docker compose down

  
