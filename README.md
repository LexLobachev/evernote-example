# evernote-example

Это набор скриптов, которые позволяют взаимодействовать с API Evernote.

## Окружение

### Зависимости

Python2.7 уже должен быть установлен. Затем воспользуйтесь pip, чтобы установить зависимости:

```bash
pip install -r requirements.txt
```

### Переменный окружения

 - EVERNOTE_CONSUMER_KEY
 - EVERNOTE_CONSUMER_SECRET
 - EVERNOTE_PERSONAL_TOKEN
 - JOURNAL_TEMPLATE_NOTE_GUID
 - JOURNAL_NOTEBOOK_GUID
 - INBOX_NOTEBOOK_GUID

1. Создайте `.env` файл рядом с `requirements.txt`.
2. `.env` содержит текст без кавычек.


#### How to get

* Register [here](https://www.evernote.com/Registration.action)
* To generate a Developer Token(EVERNOTE_PERSONAL_TOKEN), you have to go [here](https://sandbox.evernote.com/api/DeveloperToken.action)

## Как пользоваться

1. Запустите на Linux(Python 3) или Windows:

    ```bash
    $ python {название файла}.py
    ```

## Краткая сводка по файлам

### list_notebooks.py

Скрипт, благодаря которому выводятся все GUID и название блокнота пользователя в формате `notebook.guid - notebook.name`

### add_note2journal.py

Скрипт, который создает новую заметку по шаблону в журнал, меняя в заголовке дату и день недели на текущие

### dump_inbox.py

Скрипт, который по умолчанию выводит в консоль метаданные 10 заметок из `Inbox`. Но можно при запуске скрипта указать аргументом 
количество записей, по которым мы хотим получить информацию:

    ```bash
    $ python dump_inbox.py number 15
    ```
