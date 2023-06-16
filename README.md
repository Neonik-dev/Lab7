## Что это?
Клиент-серверное приложение, которое позволяет работать с коллекцией, хранящей музыкальные группы. Всего доступно около 20 команд. Вся работа происходит в командной строке.

## Что под капотом?
Проект больше учебный, цель стояла познакомится с новыми технологиями и инструментами, поэтому порой использовались не самые подходящие инструменты для этой задачи.
* Взаимодействие между клиентом и сервером происходит по TCP протоколу.
* Данные передавал при помощи ServerSocketChannel и SocketChannel.
* Сериализация данных
* Jdbc, HikaryCP
* Миграции накатываются с помощью Liquebase
* JUnit 5 и Mockito
* Многопоточность

## Какой функционал?


## Что инетерсного я сделал в этом проекте?
* Закрепил и изучил некоторые тонкости с работой Liquebase
* Применил в проекте HikariCP
* Во время разработки проекта использовал паттерны (например, в основе всего проекта лежит паттерн Command)
* Создал авторизацию и регистрацию пользователей. 
* После входа в аккаунт создается сессия, которая всегда передается с запросом клиента.
* Настроил время жизни сессии и sheduler который удалят устаревшие сессии из бд (живут 25 минут, но можно настроить в properties)
* Выполнил код по SOLID
* Постарался применять IoC в классах взаимодействия с бд.
* Познакомился с concurrency и многопоточностью (в проекте применял ReentrantLock, Fixed thread pool, создание собственных Thread)
