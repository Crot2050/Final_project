Final_Test_Automation_Project
Проект содержит файлы необходимые для автоматизации тестирования нового интерфейса авторизации и регистрации для входа в личный кабинет сайта Ростелеком Информационные Технологии.

В папке pages находится 4 файла:
auth_page.py содержит класс страницы авторизации сайта Ростелеком Информационные Технологии;

reg_page.py содержит класс страницы регистрации сайта Ростелеком Информационные Технологии;

base_page.py содержит базовый класс страницы и методы для тестирования;

elements.py соддержит классы методов для взаимодействия с веб-элементами на странице.

В папке tests находятся 2 файла:
test_auth_page.py содержит автоматизированные тесты для страницы авторизации сайта Ростелеком Информационные Технологии, под каждым тестом есть описание, что он проверяет;

test_reg_page.py содержит автоматизированные тесты для страницы регистрации сайта Ростелеком Информационные Технологии, под каждым тестом есть описание, что он проверяет.

conftest.py содержит конфигурационные данныедля проведения тестирования.

settings.py содержит данные с которыми проводилось тестирование(валидные логин, пароль и т.д.).

requirments.py содержит все пакеты и зависимости для запуска данного проекта.

Инструменты, которые применялись для тестирования:

Selenium WebDriver

Хорошо подходит для тестирования UI;
Бесплатный;
Гибкий в использовании, его можно использовать со многими браузерами включая мобильные. Все автотесты этого проекта сделаны с помощью этого инструмента.
Техники тест-дизайна, которые применялись для тестирования:

Классы эквивалентности и анализ граничных значений были примененны для полей ввода, чтобы уменьшить количество возможных тестов. Ими проверялись поля "имя", "фамилия", требования у этого поля от 2 до 30 символов, только Кириллицей, поэтому проверялись значения из - 1, 2, 3, 15, 29, 30 символов. Поле "телефон" проверялись значения из 10, 12 цифр для российского номера и 8,10 цифр для беллоруского номера. Поле "пароль" исходя из требований должно состоять от 8 до 20 символов, латинские буквы, обязательно одна заглавная буква и одна цифра, часть проверок состоит из анализа граничных значений это 7, 8, 20, 21 символов, все символы из цифр, Кириллица, все буквы верхнего регистра.

Предугадывание ошибки исходя из знания и опыта можно предположить возможный баг или уязвимость системы. Проверялись поля для регистрации - отправка полей с пустыми знаениями, SQL-иньекция, XSS-иньекция.

Больше всего сложностей для написания тестов вызвала капча.

Ссылка на тест-кейсы и баги: 
