DJANGO_WEBPROJECT
20.1 Работа с ORM в Django

-Задание 1
Подключите СУБД PostgreSQL для работы в проекте. Для этого:

Создайте базу данных в ручном режиме.
Внесите изменения в настройки подключения.
-Задание 2
В приложении каталога создайте модели:

Product,
Category.
Опишите для них начальные настройки.

-Задание 3
Для каждой модели опишите следующие поля:

Product:
наименование,
описание,
изображение (превью),
категория,
цена за покупку,
дата создания,
дата последнего изменения.
Category:
наименование,
описание.
Для поля с изображением необходимо добавить соответствующие настройки в проект, а также установить библиотеку для работы с изображениями 
Pillow
.

-Задание 4
Перенесите отображение моделей в базу данных с помощью инструмента миграций. Для этого:

Создайте миграции для новых моделей.
Примените миграции.
Внесите изменения в модель категорий, добавьте поле 
created_at
, примените обновление структуры с помощью миграций.
Откатите миграцию до состояния, когда поле 
created_at
 для модели категории еще не существовало, и удалите лишнюю миграцию.
-Задание 5
Для моделей категории и продукта настройте отображение в административной панели. Для категорий выведите id и наименование в список отображения, а для продуктов выведите в список id, название, цену и категорию.

При этом интерфейс вывода продуктов настройте так, чтобы можно было результат отображения фильтровать по категории, а также осуществлять поиск по названию и полю описания.

-Задание 6
Через инструмент shell заполните список категорий, а также выберите список категорий, применив произвольные рассмотренные фильтры. В качестве решения приложите скриншот.
Сформируйте фикстуры для заполнения базы данных.
Напишите кастомную команду, которая умеет заполнять данные в базу данных, при этом предварительно зачищать ее от старых данных.
Последний пункт можно реализовать в связке с инструментом работы с фикстурами, можно описать вставку данных отдельными запросами.

-* Дополнительное задание
В контроллер отображения главной страницы добавьте выборку последних 5 товаров и вывод их в консоль.
Создайте модель для хранения контактных данных и попробуйте вывести данные, заполненные через админку, на страницу с контактами.


19.2 Знакомство с Django

Задание 1
Для начала работы над задачей выполните первые шаги:

Настройте виртуальное окружение.
Создайте новый Django-проект.
Задание 2
После успешного создания проекта сделайте первую настройку. Для этого:

Создайте первое приложение с названием 
catalog
.
Внесите начальные настройки проекта.
Сделайте настройку урлов (URL-файлов) для нового приложения.
Задание 3
Подготовьте два шаблона для домашней страницы и страницы с контактной информацией.

Для создания шаблонов лучше использовать UIkit Bootstrap. Это удобный набор элементов, которые уже стилизованы и готовы к использованию. UIkit Bootstrap помогает избежать самостоятельной верстки макетов.

Если возникнут проблемы при создании собственного интерфейса, возьмите за основу данный шаблон: https://github.com/oscarbotru/.

Задание 4
В приложении в контроллере реализуйте два контроллера:

 Контроллер, который отвечает за отображение домашней страницы.
 Контроллер, который отвечает за отображение контактной информации.
* Дополнительное задание
Реализуйте обработку сбора обратной связи от пользователя, который зашел на страницу контактов и отправил свои данные для обратной связи.

Дополнительное задание, помеченное звездочкой, желательно, но не обязательно выполнять.

Критерии выполнения заданий
Всё итоговое решение залили в github.com и сдали в виде ссылки на репозиторий.
Создали отдельное приложение.
Реализовали два контроллера.
Адреса описали не внутри главного URL-файла, а вынесли в пространства имен.
Добавили папку с шаблонами, в которой лежат два шаблона.
