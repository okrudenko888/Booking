"# Booking"
Задача

Создать консольное Java приложение для бронировки авиабилетов

Описание
Создайте консольное приложение, которое в бесконечном цикле (до выбора команды Выход) предоставляет интерфейс для поиска и бронировки авиабилетов.

Командная работа
На данном проекте все студенты разделены на группы по три человека. Для каждого из участников команды частично определен перечень заданий, которые он должен выполнить. Остальные задания участники команды могут распределить самостоятельно. Участники команды могут самостоятельно решить, кто будет выпонять задание №1, №2 и №3.

Главное меню приложения
Главное меню, которое пользователь видит при запуске программы, должно иметь следующие пункты:


Онайн-табло. Показывает информацию про все рейсы из Киева в ближайшие 24 часа. После этого снова отображается главное меню.

Посмотреть информацию о рейсе. Пользователю предлагается ввести айди рейса. Далее по этому рейсу выводится вся информация - дата, время, место назначения, количество свободных мест. После этого снова отображается главное меню.

Поиск и бронировка рейса. Пользователю предлагается последовательно ввести следующую информацию: место назначения, дата, количество человек (сколько необходимо купить билетов). После этого программа должна выполнить поиск рейсов, которые удовлетворяют заданным условиям (на рейсе свободных мест должно быть не меньше, чем количество указанных пассажиров). Все найденные рейсы должны быть выведены на экран. После этого пользователь может выбрать один из найденных рейсов, указав его порядковый номер, либо вернуться в главное меню (выбрав пункт 0). Если пользователь решает забронировать рейс, ему необходимо ввести данные (имя и фамилия) для того количества пассажиров, которое было указано при поиске.

Отменить бронирование. Пользователю предлагается ввести айди бронирования. Если такое бронирование было найдено, оно отменяется. После этого снова отображается главное меню. Пользователь может отменить любое бронирование.

Мои рейсы. Пользователю предлагается ввести фамилию и имя. После этого на экран выводится список всех бронирований, которые были сделаны данным пользователем или в которых он является пассажиром.

Выход. Завершение работы приложения.


Технические требования:

Приложение должно иметь стандартную трехслойную структуру - то есть для каждой рабочей сущности иметь классы Controller, Service и DAO.
Для каждого класса контроллера, сервиса и DAO должны быть написаны юнит-тесты.
Для работы с консолью (главное меню) должен быть создан отдельный класс, который для получения информации будет обращаться к необходимым контроллерам. Контроллеры могут обращаться к сервисам, сервисы к DAO. Прямых обращений из консольного класса к сервисам или DAO быть не должно.
Остальные сущности/классы тоже должны быть разбиты по соответствующим пакетам.
Везде, где это возможно, необходимо использовать возможности Java 8.
В случае невозможных действий пользователя (например выбор несуществующего пункта меню), бросать собственный класс исключения. Перехватывать его выше в приложении, чтобы программа продолжала работу.
"База данных" приложения должна храниться в текстовом/бинарном файле рядом с приложением. При запуске приложения данные из файлов должны считываться в коллекции, которые находятся в DAO классах.
Приложение должно иметь большую автоматически сгенерированную базу рейсов, которая должна быть скопирована в файл, и считываться приложением при запуске.
Для данного проекта достаточно сделать, чтобы все рейсы летели из Киева, отличаться у них будет только место назначения.
При выходе из приложения, все изменения должны записываться в файл сохранения. При повторном запуске приложения коллекции в DAO должны заново инициализироваться данными из файла сохранения.


Задание для студента №1

Создать класс для работы с консолью


Задание для студента №2

Создать контроллер, сервис и DAO для рейсов


Задание для студента №3

Создать контроллер, сервис и DAO для бронирований


Организация рабочего процесса:

Код участников команды должен находиться в одном репозитории.
При выполнении данного проекта необходимо настроить рабочее окружение на GitHub таким образом, чтобы ветка master была защищенной, и в нее напрямую нельзя было делать ни один коммит. О том как это сделать можно почитать здесь.
Каждый раз для внесения изменений в проект необходимо будет создать новую ветку, а потом Pull Request, основанный на изменениях в ней. Детальнее про процесс можно почитать здесь.
На данном проекте вы будете учиться выполнять Code review кода, который написали ваши коллеги. Проект должен быть настроен таким образом, что любой Pull Request можно слить в мастер только после того, как его посмотрят и поставят свой Approve оба других участника команды. Как настроить для этого репозиторий описано здесь.


Не обязательные задания продвинутой сложности:

Создать отдельный класс для логгирования, и записывать все действия пользователя в лог файл.
Первым шагом перед показыванием главного меню добавить авторизацию пользователя - пользователь должен ввести логин и пароль. Если такой пользователь существует, дальше показывается главное меню, и вся работа происходит от имени этого пользователя. Например, меню Мои бронирования выводит информацию о всех бронированиях текущего пользователя. В главном меню добавляется один новый пункт - Завершить сессию, который делает логаут, после чего можно ввести логин и пароль другого пользователя.
Добавить рейсы не только из Киева, а и между другими городами. При поиске искать стыковочные рейсы со временем ожидания не более 12 часов.


Удачи!
