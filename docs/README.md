###
git add. добавляет изменения в файлах
git status - дает понимание, какие файлы были изменены, добавлены или удалены. Но не сделан коммит.
git commit -m "Описание изменений" фиксирует изменения в репозитории. Сохраняет их в историю.
git log выводит всю историю коммитов. Кто, что, когда изменил.
git show даёт информациию о конкретнои коммите. Дата, автор, что изменилось
git diff разница между текущими изменениями и последним коммитом, Показывает, что именно изменилось в файлах.
git restore отменяет все изменения в файлах, возвращает к состоянию последнего коммита.
git rm удаляет файлы из Git, а так же из рабочей папки в случае необходимости.
git reset отменяет все коммиты и возвращает проект к более раннему этапу
git branch показывает список веток 
git branch -d "имя ветки" создаём новую ветку
git pull переносит актуальные изменения с гита на наш репозиторий, желательно находиться в главной ветке в момент выполнения 
git push отправляет изменения в удалённый репозиторий, работает только после комита
git.help -a показывает все доступные команды git 
git clone url скопировать/склонировать удалённый репозиторий 

### Понятие репозитория. Структура проекта.

## Репозиторий это - хранилище кода проекта включающие:
1. Все файлы и папки проекта
2. Историю изменений(комиты)
3. Информацию о ветках, тегах и настройках
Виды репозиториев:
1. Локальный репозиторий - хранится на пк разработчика (папка.git)
2. Удалённый репозиторий - размещён на сервере (github or gitlab)
# Базовая структура проекта в git
название проекта/           #Корневая папка проекта
|-- .git/ #Cкрытая папка с данными Git(история, настройки)
|-- src/ #Исходный код(например main.py, index.js)
|-- docs/ #Документация (Readme.md, API-описание)
|-- config/ #Файлы конфигурации(настройка сервера, БД)
|-- assets/ #Ресурсы(изображения, шрифты)
|-- .gitignore/ #Файл, указывающий, какие файлы Git должен игнорировать
## Жизненный цикл файлов Git
# Стадии:
1. Неотслеживаемая - Git о них не знает
2. Изменённые - файлы, которые уже были в репозитории, но подверглись изменению
3. Индексированные
4. Зафиксированные - изменения сохранены в репозиторий(git commit)
#Важные правила:
1. Каждое изменение должно быть логически завершённым
2. gitignore обязателен, чтобы не засорять репозиторий ненужными файлами
3. README.md это лицо проекта
### Виды, цели и уровни интеграции програмных модулей
Интеграция программных модулей - процесс объеденения отдельрных компонентов по в единую систему, обеспечивающую их совместимость
Цель интеграции:
1. Обеспечение взаимодействия модулей
2. Повышение надёжности и производительности систем
3. Упрощение разаработки и сопровождение по
4. Минимизация дублирования функционала
## Виды интеграции програмных модулей
# 1. По способу взаимодействия
1.1 Горизонтальная (объединение модулей одинаковых уровней)
1.2 Вертикальная (объединение модулей разных уровней)
# 2. По степени связанности
2.1 Слабая связанность (модули взаимодействуют через стандартные интерфейсы, что упрощает замену компонентов)
2.2 Сильная связанность (модули тесно зависят друг от друга, изменение одного требует модификации других(Пример: монолитная архитектура))
# 3. По времени выполнения
3.1 Статическая интеграциия (компоненты связываются на этапе компиляции(Пример: С++ и ему подобные))
3.2 Динамическая интеграция (компоненты связываются во время выполнения(Пример: плагины которые загружаются в run time))
## Уровни интеграции програмных модулей
# Уровень данных 
Интеграция через общие базы данных, файлы или очереди сообщений (Примеры: SQL базы, брокеры сообщений )
# Уровень API (сервисный)
Модули взаимодействуют через API (Примеры: Веб-сервисы, микросервисная архитектура)
# Уровень пользовательского интерфейса (UI)
Интеграция через единный интерфейс (Пример: веб, мобильные приложения)
# Уровень бизнес-логики
Интеграция на уровне общих бизнес-правил и процессов (Примеры: ERP-системы, Workflow-движки)
## Инструментальные средства интеграции
# Средства сборки и управления зависимостями
npm, yarn (js)
# CI/CD инструменты
GitLab CI, GitHub Actions - автоматизация сборки и тестирования
Docker, Kubernetes - контейнерезация и оркестрация
## Middleware и брокеры сообщений
RabbitMQ, Apache Kafka - асинхронная интеграция
Redis - кеширование и  Pub/Sub








