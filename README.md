# airflow_plus_mlflow_pipeline


## Оглавление
### [1 Описание проекта](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [2 Какой кейс решаем](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [3 Краткая информация о данных](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [4 Этапы работы над проектом](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [5 Результат](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)

### Описание проекта
Необходимо собрать информацию о рейтинге фильма или телепередачи из доступных открытых источников. Такими источниками могут быть:
классический датасет отзывов на фильмы IMDB, YouTube, Wikipedia,тематические сайты,тематические группы в мессенджерах,и многие другие источники… Необходимость регулярного сбора данных связана с тем, что рейтинги постоянно обновляются, а также могут выходить новые фильмы и передачи. Поэтому в практических проектах необходимо запускать такой сбор по расписанию.

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### Какой кейс решаем

Технически задача проекта заключается в сборе данных и их обработке, а также последующем обучении модели ML. Airflow используется для автоматизации операций, а MLFlow для мониторинга процессов.

Чтобы собрать информацию о рейтингах фильмов, необходимо создать конвейер, состоящий из операций запуска коннекторов для разных источников по расписанию. Коннекторы будут запускаться в определенное время, брать из конфигурационного файла перечень фильмов, для которых необходимо получить информацию о рейтинге, делать опрос доступных источников и сохранять информацию в базу данных. Далее будет запускаться обработка полученных данных и преобразование в числовые признаки (векторы эмбеддингов), на основании которых алгоритм регрессии будет предсказывать рейтинг фильма в будущем.


:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### Краткая информация о данных

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### Этапы работы над проектом

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### Результат

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)
