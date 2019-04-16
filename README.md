
# counter-angular7-nodejs

**Тестовое задание Angular 2+**

## Описание задания. 
1. Выберите UI архитектуру.
2. Выберите backend-технологию.
3. Создайте следующую функцию, используя предоставленные инструкцию.

_Заметки:_
* формула должна быть реализована на сервере.
* Вызовы API должны быть authenticated с использованием аутентификации на основе токенов.
* пользуйте фиктивного юзера; нет необходимости производить аутентификацию на уровне базы данных.

#### Функция: Счетчик приращений
**Сценарий: пользователь может войти**

Данный пользователь не авторизован, пользователь вводит логин и пароль для авторизации.
Пользователь попадает на домашнюю страницу и token используется для последующих вызовов API.

**Сценарий: счетчик равен нулю при запуске**

Пользователь смотрит на главную страницу.
Пользователь видит метку «Count: 0» и кнопку с надписью «приращение» (​ Increment​ ) сразу справа от метки, которая находится по центру по вертикали и горизонтали на странице.

**Сценарий: следующий подсчет определяется по формуле**

Учитывая данный счет (counter), когда идет запрос на следующий подсчет, тогда  когда следующий подсчет больше 1 то counter = counter * 2.

**Сценарий: кнопка приращения**

Если на главной странице счетчик 2, то при нажатии кнопки приращения (Increment), отображается всплывающее окно (popup) с текущим счетчиком 2 и следующим счетчиком 4.

В popup также есть кнопка Отмена (Cancel) и кнопка Подтверждения (Confirm).
Если счетчик приращений открыт и текущий счетчик равен 1 и следующий счетчик 2, то  при нажатии кнопки «Отмена», всплывающее окно закрывается и пользователь видит метку «Counter: 1»

**Сценарий: Счетчик после нажатия кнопки "Confirm"**

Учитывая, что открыт popup и текущий счетчик 2 И следующий счет 4
Когда пользователь нажимает кнопку подтверждения (​ Confirm​ ), тогда всплывающее окно закрывается и пользователь видит метку «Counter: 4» на главной странице.

## Реализация.
* Этот проект был создан с [Angular CLI](https://github.com/angular/angular-cli) v 7.3.8.
* Backend  nodejs v 8.15.1.

### Краткое описание.
Все для наглядности упрощено:
* login и пароль не кешируется
* проверочное поле токена не кешируется
* сервер не разбит на модули
* функции упрощены

Перед начвлом работы необходимо запустить backend-server из папки проекта командой `nodejs server/server`.
В броузере по адресу `http://localhost:3000/`должно появиться сообщение *Server готов к работе!*
* login: 123
* gапрль: 123

Срок жизни **токенов** установлен  в **10** мин, после истечения данного времени придет сообщение о необзодимость повторной аутентификации. После нее счетчик останется **таким, как и до нее**.

Если нажать в меню **«Logout»**, то после аутентификации счетчик будет **равен 0**.

### Другие реализации.

* Сайт резюме [Angular 5](https://aser.zzz.com.ua).
* Тестовое задание [модель MVC ( PHP+AJAX )](https://aser-test.000webhostapp.com ).


