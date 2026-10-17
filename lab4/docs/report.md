# Отчет по лабораторной работе №4 (n8n)

## Краткое описание выполненного
В ходе работы я освоила платформу n8n как low-code инструмент для автоматизации. Я установила n8n локально через npm (так как Docker не использовался), изучила базовые ноды (Manual Trigger, Set, Code, IF, HTTP Request, Schedule Trigger) и создала 6 рабочих процессов (workflow). Также я выполнила Часть 3 (Redis), используя бесплатный облачный сервис Upstash (так как WSL на моей машине выдавал ошибку виртуализации). Были созданы два workflow: Set/Get и Delete/Exists.

## Какие AI-промпты использовались
1. *«Как установить n8n без Docker на Windows?»* — помогло выбрать путь через npm.
2. *«Как написать код на JavaScript в узле Code, чтобы использовать let, const, if/else и цикл for?»* — использовалось для создания flow-02 и flow-03.
3. *«Как настроить HTTP Request для получения случайного факта о котах?»* — подсказка по URL и методу.
4. *«Как подключиться к Upstash Redis из n8n?»* — инструкция по заполнению полей Host, Port, Password.
5. *«Как исправить ошибку WRONGPASS при подключении к Redis?»* — проверка токена и режима Read-Only.

## Какие ноды освоены
* **Manual Trigger** — ручной запуск.
* **Set (Edit Fields)** — создание и изменение полей данных.
* **Code** — выполнение JavaScript (работа с массивами, объектами, циклами).
* **IF** — условное ветвление.
* **HTTP Request** — отправка GET-запросов к внешним API.
* **Schedule Trigger** — запуск по расписанию.
* **NoOp** — заглушка для завершения ветки.
* **Redis** — операции Set, Get, Delete (работа с облачной базой Upstash).

## Скриншоты всех workflow

### 2.1. Manual Trigger - Set - Code
![Схема workflow](../screenshots/02.1-manual-set/01-workflow-canvas.jpg)
![Настройки Set](../screenshots/02.1-manual-set/02-set-node-settings.jpg)
![Результат Code](../screenshots/02.1-manual-set/03-code-node-result.jpg)

### 2.2. Code node (JS)
![Схема workflow](../screenshots/02.2-code/01-workflow-canvas..jpg)
![Настройки Code (часть 1)](../screenshots/02.2-code/02-code-settings-part1.jpg)
![Настройки Code (часть 2)](../screenshots/02.2-code/02-code-settings-part2.jpg)

### 2.3. IF node
![Схема workflow](../screenshots/02.3-if/01-workflow-canvas.jpg)
![Настройки IF](../screenshots/02.3-if/02-if-settings.jpg)

### 2.4. Set node (изменение полей)
![Схема workflow](../screenshots/02.4-set/01-workflow-canvas.jpg)
![Настройки Set](../screenshots/02.4-set/02-set-settings.jpg)
![Результат Code](../screenshots/02.4-set/03-code-result.png)

### 2.5. HTTP Request node
![Схема workflow](../screenshots/02.5-http/01-workflow-canvas.jpg)
![Настройки HTTP Request](../screenshots/02.5-http/02-http-settings.jpg)
![Результат Code](../screenshots/02.5-http/03-code-result.jpg)

### 2.6. Schedule Trigger
![Схема workflow](../screenshots/02.6-schedule/01-workflow-canvas.jpg)
![Настройки Schedule](../screenshots/02.6-schedule/02-schedule-settings.jpg)
![Результат Code](../screenshots/02.6-schedule/03-code-result.jpg)

### 3. Redis (Set/Get)
![Успешное подключение](../screenshots/03-redis/01-redis-credential-success.jpg)
![Настройки Set](../screenshots/03-redis/02-redis-set-settings.jpg)
![Результат Get](../screenshots/03-redis/03-redis-get-result..jpg)

### 3. Redis (Delete/Exists)
![Схема workflow](../screenshots/03-redis/delete-exists-canvas.jpg)
![Настройки Delete](../screenshots/03-redis/redis-delete-settings.jpg)
![Консоль Upstash](../screenshots/03-redis/upstash-console.jpg)

## Выводы
В ходе выполнения лабораторной работы я научилась создавать автоматизированные сценарии в n8n. Самым интересным было работать с узлом Code, так как он позволяет использовать JavaScript для гибкой обработки данных. Узел IF показал, как строить логические ветвления. HTTP Request дал понимание, как интегрировать внешние API. Я также поняла, как работает Schedule Trigger для фоновых задач.

**Сравнение с Node-RED:**
Работа с n8n показалась мне знакомой, так как ранее я изучала Node-RED. Обе платформы используют визуальное программирование на основе потоков данных. В n8n, как и в Node-RED, есть узлы, которые соединяются стрелками, и данные передаются в формате JSON. Это сделало освоение n8n интуитивно понятным и быстрым.

**Разница с Node-RED:**
1. **Визуальный стиль:** n8n выглядит более современно и минималистично, а Node-RED имеет более "инженерный" интерфейс.
2. **Работа с данными:** В n8n узлы оперируют массивами объектов (items), что удобно для пакетной обработки. В Node-RED акцент на передаче одного сообщения (msg) через поток.
3. **Экосистема:** n8n имеет больше встроенных интеграций с бизнес-сервисами (Google, Slack, CRM), а Node-RED больше ориентирован на IoT и работу с оборудованием.

**Про Redis:**
Изначально я планировала установить Redis через WSL, но столкнулась с ошибкой виртуализации (`UtilAcceptVsock: accept4 failed 110`). Поэтому я использовала бесплатный облачный сервис Upstash. Это позволило выполнить Часть 3 без установки Docker и WSL. Я научилась подключаться к Redis по TCP, настраивать credential (Host, Port, Password, SSL) и выполнять операции Set, Get, Delete.