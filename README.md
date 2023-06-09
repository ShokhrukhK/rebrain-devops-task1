# REBRAIN-DEVOPS-TASK4

В данном репозитории находится дефолтный конфигурационный файл nginx


### REBRAIN-DEVOPS-TASK4

![Built with Cookiecutter Django](https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter)
![code style Black ](https://img.shields.io/badge/code%20style-black-000000.svg)


:Лицензия: MIT

Настройки
---------

Настройки [settings](http://cookiecutter-django.readthedocs.io/en/latest/settings.html).


Базовые команды
---------------

#### 1. Запуск приложения

* Для запуска приложения из под консоли введите следующую команду 
 
    ```$ python manage.py runserver```

#### 2. Создание пользователя


* Для создания **простого пользователя** пройдите по следующей ссылке [signup](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)

* Для создания **привилегированного пользователя**, запустите командную строку и запустите следующую команду::

    ```$ python manage.py createsuperuser```
    
>  **простого пользователя** - пользователь, не обладающий расширенными правами доступа к системе
>  **привилегированного пользователя** - пользователь, обладающий расширенными правами доступа к системе


Тестирование кода
-----------------

#### 1. Тестирование используя mypy
```
    $ mypy project
```



#### 2. Тестовое Покрытие - для тестового покрытия кода и генерации отчетов в формате HTML запустите следующее
```
    $ coverage run -m pytest
    $ coverage html
    $ open htmlcov/index.html
```

Итоговый отчет тестирования кода:

|Name                      | Packages     | Files        | Classes      | Lines          | Conditionals|
|--------------------------|--------------|--------------|--------------|----------------|-------------|
|Cobertura Coverage Report | 100% - 11/11 | 100% - 48/48 | 100%	- 48/48 | 90% - 997/1113 | 53% - 47/88 |



#### 3. Тестирование используя py.test
```
    $ pytest
```

Celery
------

В этом приложение используется Celery.

Для запуска celery worker:

    cd project
    celery -A config.celery_app worker -l info

> Обратите внимание: чтобы зпустить Celery, важно *где* выполняются команды celery. Если вы находитесь в одной папке с *manage.py*, команда зупутится.





Развертывание проекта
----------

Далее подробно описано, как развернуть это приложение.



Docker
------

[Документация cookiecutter-django Docker](http://cookiecutter-django.readthedocs.io/en/latest/deployment-with-docker.html)
