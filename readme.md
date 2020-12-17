## Задача
Есть веб-api, непрерывно принимающее события (ограничимся 10000 событий) для группы аккаунтов (1000 аккаунтов) и складывающее их в очередь.
Каждое событие связано с определенным аккаунтом и важно, чтобы события аккаунта обрабатывались в том же порядке, в котором поступили в очередь.
Обработка события занимает 1 секунду (эмулировать с помощью setTimeout).

Веб-api и очередь эмулировать консольным скриптом, непрерывно генерирующим события для обработки в фоне. События генерировать пачками, содержащими последовательности по 1-10 для каждого аккаунта.
Сделать обработку очереди событий максимально быстрой на данной конкретной машине.

Код писать на TypeScript/Node.js. Можно использовать фреймворки и инструменты такие как RabbitMQ, Redis, MySQL и т. д. Запуск кода сделать в 1-3 команды, поэтому при необходимости использовать docker и docker-compose.

На выходе нужен лог с id аккаунтов и id событий для проверки очередности выполнения событий.

## Запуск проекта

`node 12`

1. `yarn install`
2. `docker-compose up`
3. `yarn start`
