Задача №3: Postman Echo
Важно: эту задачу нужно выполнять в отдельном репозитории.

В этой задаче мы сэмулируем ситуацию, в которой SUT уже запущен, а мы из теста просто обращаемся к нему.

Есть специальный сервис, предназначенный для тестирования HTTP-запросов. Называется он Postman Echo. Никогда не тестируйте автоматизированными средствами веб-сервисы, если у вас нет на это письменного разрешения или если веб-сервисы специально не предназначены для этого.

Мы можем отправлять туда запросы и получать ответы.

С GET-запросами мы немного потренировались, теперь нас будут интересовать POST-запросы, а именно отправка тела запроса:

// Given - When - Then
// Предусловия
given()
.baseUri("https://postman-echo.com")
.body("some data") // отправляемые данные (заголовки и query можно выставлять аналогично)
// Выполняемые действия
.when()
.post("/post")
// Проверки
.then()
.statusCode(200)
.body(/* --> ваша проверка здесь <-- */)
;
[![Java CI with Gradle](https://github.com/ValentinaandreEVA/Restgradle-1.2.3./actions/workflows/gradle.yml/badge.svg)](https://github.com/ValentinaandreEVA/Restgradle-1.2.3./actions/workflows/gradle.yml)