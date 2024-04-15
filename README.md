  Для того чтобы запустит все необходимые сервисы, нужно выполнить следующий команды:

*  $ docker-compose -f docker-compose.prod.yml up -d --build
*  $ docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
*  $ docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear

---
## Для проверки работоспособности, необходимо:

    Загрузите изображение на http://localhost:1337/.
    Затем просмотрите изображение на http://localhost:1337/media/IMAGE_FILE_NAME.

*** ! Если проект размещен на удаленном хостинге, то вместо "localhost" нужно ввести IP-адрес сервера ('192.168.10.44'). ***

