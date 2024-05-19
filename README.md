# ITMO_ICT_WebDevelopment_tools_2023-2024

Репозиторий для реализации дистанционного обучения по дисциплине "Соедства Web-программирования".

[Учебный журнал](https://docs.google.com/spreadsheets/d/1FuO5V6SSLJBSHT9f92R_iFO8pDD7TuDjcgOWXgdYFSk/edit?usp=sharing) по дисциплине. Тут доступна информация о сроках сдачи работ, о текущей успеваемости студентов и описаны все материалы необходимые для реализации курса.

Составляющие финальной оценки:
- 60 баллов - лабы (их делать обязательно).
- 20 баллов - тесты.
- 20 баллов - дисскусии на практиках (1 доклад за семестр).

При выполнении всех лаб по дисциплине в срок + две недели - экзамен-автомат.

Все лабы необходимо сдать до сессии декабря, иначе есть риск, что преподаватель не успеет их проверить.

Если лабораторная работа выполнена не в срок, требуется получить допуск к ее защите. Для допуска необходимо выполнть задания на https://leetcode.com/. 1 неделя просрочки - 1 задание.
В прошлом семестре студентам было необходимо делать задания из куррса [Top Interview Questions начального уровня](https://leetcode.com/explore/interview/card/top-interview-questions-easy/). В этом семестре нужно делать задания из курса [Top Interview Questions среднего уровня. ](https://leetcode.com/explore/interview/card/top-interview-questions-medium/) Если задания окажутся для Вас слишком сложными, можно сделать любые другие задания из других курсов.

# Лабораторная работа 1. Реализация серверного приложения FastAPI.

Необходимо реализовать полноценное серверное приложение с помощью фреймворка FastAPI с применением дополнительных средств и библиотек. [Текст работы](https://rendex85.github.io/WebDevelopmentLabsDocs/lr2/lr2/)

# Лабораторная работа 2. Потоки. Процессы. Асинхронность.

Цель работы: понять отличия потоками и процессами и понять, что такое ассинхронность в Python.

Работа о потоках, процессах и асинхронности поможет студентам развить навыки создания эффективных и быстродействующих программ, что важно для работы с большими объемами данных и выполнения вычислений. Этот опыт также подготавливает студентов к реальным проектам, где требуется использование многопоточности и асинхронности для эффективной обработки данных или взаимодействия с внешними сервисами. Вопросы про потоки, процессы и ассинхронность встречаются, как минимум, на половине собеседований на python-разработчика уровня middle и Выше.

Теоретические материалы (минимум):
- [Конспект лекции о том, как работают потоки и какие у есть дополнительные функции у библиотеки thearding](https://docs.google.com/document/d/1b4qjEsRi7VvMsDPu5z8JZ8yEedliFS0CiY2dVRAwVXc/edit?usp=sharing)
- Конспект о multiprocessing (в разработке)
- Конспект об асинхронности (в разработке)
- [Ассинхронность с AsyncIO - думаю, это **лучший ролик для тех, кто хочет быстро все понять**](https://www.youtube.com/watch?v=fsOUCxBowD8)
- [GIL в Python: зачем он нужен и как с этим жить (Григорий Петров)](https://youtu.be/AWX4JnAnjBE)

Теоретические материалы (рассширенная версия):
- [Плейлист уроков по ассинхронности в Python (Олег Молчанов)](https://www.youtube.com/playlist?list=PLlWXhlUMyooawilqK4lPXRvxtbYiw34S8)

### Задание:

#### Задача 1. Различия между threading, multiprocessing и async в Python

**Задача:** Напишите три различных программы на Python, использующие каждый из подходов: threading, multiprocessing и async. Каждая программа должна решать считать сумму всех чисел от 1 до 1000000. Разделите вычисления на несколько параллельных задач для ускорения выполнения.

**Подробности задания:**
1. Напишите программу на Python для каждого подхода: threading, multiprocessing и async.
2. Каждая программа должна содержать функцию calculate_sum(), которая будет выполнять вычисления.
3. Для threading используйте модуль threading, для multiprocessing - модуль multiprocessing, а для async - ключевые слова async/await и модуль asyncio.
4. Каждая программа должна разбить задачу на несколько подзадач и выполнять их параллельно.
5. Замерьте время выполнения каждой программы и сравните результаты.


#### Задача 2. Параллельный парсинг веб-страниц с сохранением в базу данных
**Задача:** Напишите программу на Python для параллельного парсинга нескольких веб-страниц с сохранением данных в базу данных с использованием подходов threading, multiprocessing и async. Каждая программа должна парсить информацию с нескольких веб-сайтов, сохранять их в базу данных.

**Подробности задания:**
1. Напишите три различных программы на Python, использующие каждый из подходов: threading, multiprocessing и async.
2. Каждая программа должна содержать функцию parse_and_save(url), которая будет загружать HTML-страницу по указанному URL, парсить ее, сохранять заголовок страницы в базу данных и выводить результат на экран.
3. Используйте базу данных из лабораторной работы номер 1 для заполенния ее данными. Если Вы не понимаете, какие таблицы и откуда Вы могли бы заполнить с помощью парсинга, напишите преподавателю в общем чате потока.
4. Для threading используйте модуль threading, для multiprocessing - модуль multiprocessing, а для async - ключевые слова async/await и модуль aiohttp для асинхронных запросов.
5. Создайте список нескольких URL-адресов веб-страниц для парсинга и разделите его на равные части для параллельного парсинга.
6. Запустите параллельный парсинг для каждой программы и сохраните данные в базу данных.
7. Замерьте время выполнения каждой программы и сравните результаты.

**Дополнительные требования:**
- Сделайте документацию, содержащую описание каждой программы, используемые подходы и их особенности.
- Включите в документацию таблицы, отображающие время выполнения каждой программы.
- Прокомментируйте результаты сравнения времени выполнения программ на основе разных подходов.

**Срок сдачи:** 13 мая 2024.

**Оценка:** Качество и эффективность реализации каждой программы, понимание особенностей threading, multiprocessing и async, анализ и сравнение времени выполнения программ на основе различных подходов.


# Лабораторная работа 3: Упаковка FastAPI приложения в Docker, Работа с источниками данных и Очереди

## Цель
Научиться упаковывать FastAPI приложение в Docker, интегрировать парсер данных с базой данных и вызывать парсер через API и очередь.

Работа с микросервисной архитектурой — это один из самых актуальных и востребованных навыков в современной разработке программного обеспечения. Лабораторная работа, которую вы выполняете сейчас, — это ваш первый шаг к пониманию и освоению микросервисной архитектуры

### Подзадача 1: Упаковка FastAPI приложения, базы данных и парсера данных в Docker

1. **Создание FastAPI приложения**:
   Создано в рамках лабораторной работы номер 1

2. **Создание базы данных**:
   Создано в рамках лабораторной работы номер 1

3. **Создание парсера данных**:
   Создано в рамках лабораторной работы номер 2

4. **Реулизуйте возможность вызова парсера по http**
   Для этого можно сделать отдельное приложение FastAPI для парсера или воспользоваться библиотекой socket или подобными.

   Пример кода:
```
from fastapi import FastAPI, HTTPException
...

app = FastAPI()

@app.post("/parse")
def parse(url: str):
    try:
        response = requests.get(url)
        response.raise_for_status()
        # Вызов парсера
        return {"message": "Parsing completed", ...}
    except requests.RequestException as e:
        raise HTTPException(status_code=500, detail=str(e))
```


6. **Разработка Dockerfile**:
   - Создайте Dockerfile для упаковки FastAPI приложения и приложения с паресером. В Dockerfile укажите базовый образ, установите необходимые зависимости, скопируйте исходные файлы в контейнер и определите команду для запуска приложения.
   - **Зачем**: Docker позволяет упаковать приложение и все его зависимости в единый контейнер, что обеспечивает консистентность среды выполнения и упрощает развертывание.
   - Полезные ссылки:
     - [Документация Dockerfile](https://docs.docker.com/engine/reference/builder/)
     - [FastAPI и Docker-контейнеры](https://fastapi.tiangolo.com/ru/deployment/docker/)
     - [Запускаем PostgreSQL в Docker: от простого к сложному](https://habr.com/ru/articles/578744/)

7. **Создание Docker Compose файла**:
   - Необходимо написать docker-compose.yml для управления оркестром сервисов, включающих FastAPI приложение, базу данных и парсер данных. Определите сервисы, укажите порты и зависимости между сервисами.
   - **Зачем**: Docker Compose упрощает управление несколькими контейнерами, позволяя вам запускать и настраивать все сервисы вашего приложения с помощью одного файла конфигурации.
   - Полезные ссылки:
     - [Зачем нужны системы оркестрации?](https://rebrainme.com/blog/kubernetes/zachem-nuzhny-sistemy-orkestraczii/)
     - [Документация Docker Compose](https://docs.docker.com/compose/)

### Подзадача 2: Вызов парсера из FastAPI

1. ** Эндпоинт в FastAPI для вызова парсера**:
   - Добавьте в FastAPI приложение маршрут, который будет принимать запросы с URL для парсинга, отправлять запрос парсеру (запущенному в отдельном контейнере) и возвращать ответ с результатом.
   - **Зачем**: Это позволит интегрировать функциональность парсера в ваше веб-приложение, предоставляя возможность пользователям запускать парсинг через API.
   - Полезные ссылки:
     - [Документация FastAPI](https://fastapi.tiangolo.com/tutorial/path-params/)

### Подзадача 3: Вызов парсера из FastAPI через очередь

### Как это работает

1. **Celery и Redis**:
   - Celery — это асинхронная очередь задач, которая позволяет легко распределять и выполнять задачи в фоне. Redis используется как брокер сообщений, хранящий задачи, которые должны быть выполнены.
   - При получении HTTP-запроса, задача ставится в очередь Redis, и Celery-воркер обрабатывает её в фоне.

2. **Docker Compose**:
   - Docker Compose позволяет легко настроить и запустить Celery, Redis и ваше FastAPI приложение как отдельные контейнеры, работающие в одной сети. Это упрощает управление зависимостями и конфигурацией всех компонентов системы.

### Почему это важно для студентов

Практические навыки настройки и использования асинхронной очереди задач в реальном приложении - первый шаг для MLops для 45 направления. Студенты научатся разделять ответственность между различными сервисами и компоновать их для достижения общей цели. В реальных проектах часто требуется выполнение сложных и длительных операций. Опыт работы с Celery и Redis подготовит к решению таких задач и даст уверенность в использовании современных технологий.

1. **Установите Celery и Redis**:
   - Добавьте зависимости для Celery и Redis в проект. Celery будет использоваться для обработки задач в фоне, а Redis будет выступать в роли брокера задач и хранилища результатов.
   - **Зачем**: Celery и Redis позволяют организовать фоновую обработку задач, что полезно для выполнения длительных или ресурсоемких операций без блокировки основного потока выполнения.
   - Полезные ссылки:
     - [Celery: проясняем неочевидные моменты](https://habr.com/ru/articles/686820/)
     - [Документация Celery](https://docs.celeryproject.org/en/stable/)
     - [Документация Redis](https://redis.io/documentation)

2. **Настройка Celery**:
   - Создайте файл конфигурации для Celery. Определите задачу для парсинга URL, которая будет выполняться в фоновом режиме.
   - **Зачем**: Настройка Celery позволит асинхронно обрабатывать задачи, что улучшит производительность и отзывчивость вашего приложения.
   - Полезные ссылки:
     - [Документация Celery: Настройка](https://docs.celeryproject.org/en/stable/userguide/configuration.html)

3. **Обновите Docker Compose файл**:
   - Добавьте сервисы для Redis и Celery worker в docker-compose.yml. Определите зависимости между сервисами, чтобы обеспечить корректную работу оркестра.
   - **Зачем**: Это позволит вам легко управлять всеми сервисами вашего приложения, включая асинхронную обработку задач, с помощью одного файла конфигурации.
   - Полезные ссылки:
     - [Документация Docker Compose](https://docs.docker.com/compose/)

4. **Эндпоинт для асинхронного вызова парсера**:
   - Необходимо добавить в FastAPI приложение маршрут для асинхронного вызова парсера. Маршрут должен принимать запросы с URL для парсинга, ставить задачу в очередь с помощью Celery и возвращать ответ о начале выполнения задачи.
   - **Зачем**: Это позволит запускать парсинг веб-страниц в фоне, что улучшит производительность и пользовательский опыт вашего приложения.
   - Полезные ссылки:
     - [Документация FastAPI: Фоновая задачи](https://fastapi.tiangolo.com/tutorial/background-tasks/)

### Залание на максимальную оценку: Настройка переодических задач с Celery

1. **Настройка периодических задач**:
   - Настройте Celery для выполнения периодических задач (periodic tasks). Добавьте соответствующие конфигурации в Celery для запуска задач по расписанию.
   - **Зачем**: Периодические задачи полезны для выполнения регулярных операций, таких как очистка базы данных, обновление данных или отправка уведомлений.
   - Полезные ссылки:
     - [Документация Celery: Периодические задачи](https://docs.celeryproject.org/en/stable/userguide/periodic-tasks.html)


## Сдача работ

Для сдачи работы в связи с переходом на дистанционную форму обучения введены дополднительные правила игры.

Все отчеты сохраняются в **markdown** и **mkdocs** (документы и презентации).

Все студенческие работы хранятся в папке **Students**
Для сдачи работы необходимо:

1. Зарегистрироваться на Git.
2. Сделать форк репозитория с заданиями в свой аккаунт (на странице https://github.com/TonikX/ITMO_ICT_WebDevelopment_tools_2023-2024 кнопка fork справа, сверху).
3. Установить Git на компьютер.
4. Открыть папку, где хранятся Ваши проекты. В контекстом меню нажать "Open Git Bash here". Склонировать форкнутый репозиторий на комьютер (git clone [https://github.com/ваш аккаунт/ITMO_ICT_WebDevelopment_tools_2023-2024](https://github.com/TonikX/ITMO_ICT_WebDevelopment_tools_2023-2024/)).
5. В файловой системе Вашего компрьютера в склонированном репозитории создать в папке students/группа Вашу личную папку в формате Фамилия_Имя латиницей (Пример **students/k3340/Petrov_Vasya**).
6. В личной папке сделать подпапку с текущей работой в формате lr_номер (Пример **students/k3340/Petrov_Vasya/Lr1**).
7. Записать в папку отчетные материалы.
8. Сделать коммит, описать его адекватно (Пример "был добавлен файл перезентация_петров.pdf"). Набрать команлы git add и git commit -m "название комита".
9. Сделать push в Ваш форкнутый репозиторий (git push).
10. Сделать пул-реквест в репозиторий преподавателя из вашего форкнутого, описать его. Структура заголовка пулреквеста: **Фамилия_Имя-Работа_Номер** (Пример: Петров_Василий-Лабораторная_работа_1).
11. Сделатб документацию в mkdocs и оставить ее в комментариях к пулреквесту.

