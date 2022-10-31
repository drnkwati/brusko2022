# brusko.ru
Тестовое задание 6

## Оглавление

**[Установка](#Установка)** 

**[Инструкции](#инструкции)** 

### Установка

Этот пакет не требует Composer. Однако вы можете загрузить его с помощью Composer или git.
Для загрузки с помощью Composer выполните следующую команду:
```
composer create-project drnkwati/brusko2022
```

Чтобы загрузить с помощью git, выполните следующую команду:
```
git clone git https://github.com/drnkwati/brusko2022.git
```

Откройте свой терминал в корневой папке проекта.
Используйте встроенный сервер разработки PHP для запуска приложения. Выполните следующую команду:
```
php -S localhost:7070 -c dev.php.ini 'server.php'
```

Откройте веб-браузер по адресу: 
```
http://localhost:7070/
```
```
http://127.0.0.1:7070/
```
Вы должны увидеть главный экран.

![Screenshot dashboard brusko](public/img/screenshot-dashboard-brusko.png?raw=true "Dashboard brusko")
![Screenshot palindrome brusko](public/img/screenshot-palindrome-brusko.png?raw=true "Palindrome brusko")
![Screenshot files brusko](public/img/screenshot-files-brusko.png?raw=true "Files brusko")
![Screenshot migrate brusko](public/img/screenshot-migrate-brusko.png?raw=true "Migrate brusko")

### Инструкции

### 1. PHP
Написать функцию на PHP, которое принимает строку и проверяет, зеркальна ли эта строка.
(ПАЛИНДРОМЫ (перевертыши) - слова, читающиеся одинаково в обоих направлениях. Пример: шалаш)
Если зеркальное, то возвращать 1, иначе 0.
И объяснить, как работает эта функция.

### 2. SQL
Сохраняй все запросы, чтобы потом их показать:
1) Создать табличку пользователей user c столбцами: ID(Автозаполнение), DATA_CREATE(дата создания с авто заполнением), NAME(Имя);
2) Создать табличку заказов orders со столбцами: ID(Автозаполнение), DATA_CREATE(дата создания), USER_ID(привязка к ID пользователей), PRICE(цена);
3) Создать таблицу комментариев к пользователю: ID(Автозаполнение), USER_ID(привязка к ID пользователей), COMMENT(Комментарий, Просто строка);
4) Заполнить хаотичными данными эти таблицы, так, чтобы у каждого пользователя было заказов от 0 до 3.. И у некоторых пользователей были комментарии(в таблице комментариев);
5) Одним запросом вывести таблицу с фильтром от и до определённой даты(либо времени) и сортировкой по ID пользователя:
ID(Ид пользователя), ORDERS(Количество его заказов), ORDERS_PRICE(Сумма его заказов), NAME(Имя пользователя), COMMENT(Комментарий к нему).

### 3. PHP
Создать php страницу, которая связывается с таблицей с 1 задачки и отображает:
1) поля для ввода с какой по какую дату фильтровать (с защитой и проверкой даты при отправке в SQL);
2) Кнопка "Показать" - которая обновляет информацию на странице с отфильтрованными данными;
3) Вывод в табличку полученных данных;
4) Кнопка скачать CSV (которая скачивает отфильрованные данные в CSV)
4) Кнопка скачать xlsx (которая скачивает отфильрованные данные в xlsx)

### 4. PHP
Необходимо: 
1) написать функцию, 
аргументом которой будет число (количество новых файлов сессий)
которая создаёт дирректорию sessions (если её нет)
и в ней создаёт файлы (названия файлов не должны повторятся)
в которых записывает данные: 
рандомная дата начала (Каждая дата представлена количеством секунд от 1970 года..)
и с вероятностью 84% добавляет в файл рандомную дату окончания (Дата окончания должна быть позднее даты начала)
 
2) написать функцию, которая с созданных файлов, 
отображает Дату и время начала и окончания, 
когда было максимальное количество активных сессий
(если таких периодов несколько, то отображать только первый)
