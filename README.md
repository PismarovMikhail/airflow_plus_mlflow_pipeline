# airflow_plus_mlflow_pipeline


## Оглавление
### [1 Описание проекта](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [2 Какой кейс решаем](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [3 Краткая информация о данных](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [4 Этапы работы](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)
### [5 Результат](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/edit/main/README.md)

### 1 Описание проекта
Необходимо собрать информацию о рейтинге фильма или телепередачи из доступных открытых источников. Такими источниками могут быть:классический датасет отзывов на фильмы IMDB, YouTube, Wikipedia,тематические сайты,тематические группы в мессенджерах,и многие другие источники… Необходимость регулярного сбора данных связана с тем, что рейтинги постоянно обновляются, а также могут выходить новые фильмы и передачи. Поэтому в практических проектах необходимо запускать такой сбор по расписанию.



:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### 2 Какой кейс решаем

**Технически задача проекта заключается в сборе данных и их обработке, а также последующем обучении модели ML. Airflow используется для автоматизации операций, а MLFlow для мониторинга процессов.**

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### 3 Краткая информация о данных

Данные представляют собой cырые данные в формате csv, тренировочный и тестовый наборы данных из задачи «Titanic disaster» с сайта https://www.kaggle.com/c/titanic/data

Датасет содержит обычные для реальных проектов проблемы с данными: пропущенные значения, текстовые значения признаков, которые не умеют обрабатывать большиство моделей машинного обучения;
выбросы, искажающие общую статистику.

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### 4 Этапы работы

- ***4.1 Организация автоматизированного сбора данных***
- ***4.2 Обработка данных***
- ***4.3 Обучение модели ML***
- ***4.4 Первичное теститрование***

Инструмент для автоматизации операций сбора данных, обработки этих данных, обучения модели и первичного тестирования - Airflow.  Инструмент для мониторинга сбора данных, сохранения и трекинга артефактов, и обучения моделей - MLflow.

:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)

### 5 Результат

С помощью Airflow организован конвеер, включающий автоматизированную сборку информации о рейтинге фильма, обработку этих данных, обучение модели ML и ее первичное тестирование. Мониторинг "процессов" осуществлен с помощью Mlflow.

При реализации конвеера были созданы следующие **скрипты**:
- **get_data.py** Предназначен для получения данных из внешнего источника, платформы YouTube. Для этих целей используется API. По поисковому запросу «Mission Impossible» вы можете получить списки комментариев роликов YouTube, которые дает платформа по этому поисковому запросу. В полученном json файле можно достать значение параметра likeCount, которое и сохраняется в используемом далее наборе данных, в файле data.csv.
- **process_data.py** Этот скрипт предназначен для обработки данных, при которой полученные значения нормализуются, переводятся в диапазон от 0 до 1. Также в выходной файл записывается индекс значения.
- **train_test_split.py** Предназначен для разделения полученных и обработанных данных на тренировочную и тестовую выборки.
- **train_model.py** Предназначен для обучения модели ML.
- **test_model.py** Предназначен для тестирования модели ML.
- **youtube_comments_score.py** - Управление последовательностью операций по заданному расписанию.


:arrow_up:[к оглавлению](https://github.com/PismarovMikhail/airflow_plus_mlflow_pipeline/tree/main/README.md#Оглавление)
