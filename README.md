# airflow_plus_mlflow_pipeline


## Оглавление
### [1 Описание проекта](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [2 Какой кейс решаем](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [3 Краткая информация о данных](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [4 Этапы работы над проектом](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [5 Результат](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)

### 1 Описание проекта
Необходимо собрать информацию о рейтинге фильма или телепередачи из доступных открытых источников. Такими источниками могут быть:
классический датасет отзывов на фильмы IMDB, YouTube, Wikipedia,тематические сайты,тематические группы в мессенджерах,и многие другие источники.

Чтобы собрать информацию о рейтингах фильмов, необходимо создать конвейер, состоящий из операций запуска коннекторов для разных источников по расписанию. Коннекторы будут запускаться в определенное время, брать из конфигурационного файла перечень фильмов, для которых необходимо получить информацию о рейтинге, делать опрос доступных источников и сохранять информацию в базу данных. Далее будет запускаться обработка полученных данных и преобразование в числовые признаки (векторы эмбеддингов), на основании которых алгоритм регрессии будет предсказывать рейтинг фильма в будущем.

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### 2 Какой кейс решаем

**Главная задача в реализуемом проекте — организация автоматизированного сбора данных, обработка этих данных, обучение модели ML и первичное тестирование.**
:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### 3 Краткая информация о данных

Необходимость регулярного сбора данных связана с тем, что рейтинги постоянно обновляются, а также могут выходить новые фильмы и передачи. Интерфейсы, по которым можно получить эту информацию, тоже различны, это могут быть: реляционные и нереляционные базы данных, стандартные датасеты, например, в xml или csv формате, API к агрегаторам новостей, социальным сетям, мессенджерам, SparQL интерфейс DBpedia (API для доступа к информационным базам wikipedia), RSS каналы, html страницы. В зависимости от типа интерфейса для интеграции с соответствующим источником информации в программном обеспечении создается соответствующий коннектор, поддерживающий интерфейс для интеграции с источником данных.

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### 4 Этапы работы над проектом

- ***4.1 Организация автоматизированного сбора данных***
- ***4.2 Обработка данных***
- ***4.3 Обучение модели ML***
- ***4.4 Первичное теститрование***

Инструмент для автоматизации операций сбора данных, обработки этих данных, обучения модели и первичного тестирования - Airflow.  Инструмент для мониторинга сбора данных, сохранения и трекинга артефактов, и обучения моделей - MLflow.

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### Результат

С помощью Airflow организован конвеер автоматизированного сбора информации о рейтинге фильма, обработка этих данных, обучение модели ML и ее первичное тестирование.
Мониторинг "процессов" осуществлен с помощью Mlflow

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)
