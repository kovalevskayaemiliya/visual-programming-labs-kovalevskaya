# Отчёт по лабораторной работе №3. Bubble

## Тема: Список путешествий

### Краткое описание выполненного

В ходе лабораторной работы я освоила Bubble как no-code платформу. Были выполнены следующие задачи:

1. Сгенерировано приложение «Список путешествий» через AI-агента Bubble.
2. Проведено исследование через Build Guides, применена идея «Add, edit, and delete places».
3. Доработан UI вручную: изменён заголовок, создана Global Variable primary-color, создан стиль travel-primary-button, добавлен компонент «Отзывы путешественников».
4. Создан Data Type Place с полями (Name, Location, Description, Visited, User) и связью Travel List у User.
5. Реализован полный CRUD (Create, Read, Update, Delete) через workflows.

### Промпт (дословно)

Создай приложение на тему «Список путешествий». Пусть этот сайт будет требующий регистрацию. Страницу обязательно создай по структуре header + body + footer. Обязательно укажи в заготовке следующую строку: «ТВП: Ковалевская». Добавь несколько интерактивных элементов (реализующих CRUD).

### Ссылка на dev-версию приложения

https://travellist.bubbleapps.io/

### AI-промпты

- Создай приложение на тему «Список путешествий»... (Часть 1)
- Create a new Data Type named Place with fields: Name, Location, Description, Visited, User. Also add Travel List to User. (Часть 4.1)
- Add a Testimonial section to the bottom of the index page... (Часть 3.4)

### Освоенные элементы и workflows

| Элемент / Workflow | Назначение |
|---|---|
| Input, Checkbox, Button | Формы для ввода данных |
| Repeating Group | Список мест (Read) |
| Popup | Форма редактирования |
| Create a new thing | Create |
| Make changes to a thing | Update |
| Delete a thing | Delete |
| Global Variable | Цвет primary-color |
| Style | travel-primary-button |

### Скриншоты

Все скриншоты находятся в папке screenshots/.

### Выводы

В ходе лабораторной работы я освоила Bubble как no-code платформу. Научилась генерировать каркас приложения через AI-агента, работать с Build Guides, создавать Global Variables и стили, проектировать базу данных, реализовывать CRUD через workflows, работать с Popup и с Git/GitHub.

Самым сложным было настроить workflows для Update и Delete. Самым интересным — работа с AI-агентом и Drag & drop компонентами.

---

Студент: Ковалевская Эмилия
Дата: 17.10.2026
