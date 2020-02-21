# MNK-Tool
Apps for studying (Telegram, tkinter)

Этот проект - набор полезных приложений и программ для помощи во время обучения. 

# bot.py 
Запускает бота (необходимо предварительно создать его в Телеграме с помощью BotFather и заменить токен в коде на Ваш).
После запуска программы становится доступен весь функционал бота. 

Доступны следующие команды:

**/figure** - строит график по точкам;

**/figure_mnk** - строит график, линеаризованный с помощью метода наименьших квадратов;

**/mnk_constants** - вычисляет коэффициент наклона и погрешность его определения;

Для всех вышеперечисленных команд необходимо предварительно создать таблицу Excel с данными для обработки.

**/timetable** - выодит расписание пар нужной вам группы;

**/exam** - выводит расписание экзаменов нужной вам группы;

**/flash_card** - предлагает пользователю вспомнить доказательство случайно предоставленной теоремы из экзаменационной программы по математическому анализу, после чего отправляет картинку с доказательством;

# graphicsmodule.py
Запускает экранное приложение со следующими опциями:

**Построить график** - в этой вкладке вы сможете построить график, загрузив данные в формате «.xlsx», выбрать тип графика(линеаризованный или обычный, по точкам), добавить название к графику в интерактивном поле «Название графика», указать подписи к осям в полях для ввода «Название оси Ох» и «Название оси Оу». Также есть возможность добавить кресты погрешностей, поставив галочку в окошке «Построить кресты погрешностей». *Заметьте, что таблица с данными должна содержать только численные значения, которые необходимы для обработки!*

**Посчитать МНК** - в этой вкладке можно получить погрешность для коэффициента наклона прямой, загрузив файл с данными в формате «.xlsx». *Заметьте, что таблица с данными должна содержать только численные значения, которые необходимы для обработки!*

**Посчитать погрешности методом частных производных** - в этой вкладке, указав формулу, название переменных в ней, их значения и погрешности соответственно, можно узнать погрешность для введенных данных. Названия переменных, их значения и погрешности необходимо вводить через запятую, разделяя ее и следующий символ пробелом.

**Создать таблицу в LATEX** - в этой вкладке можно получить код для таблицы LaTex, загрузив файл в формате «.xlsx».
*Заметьте, что таблица с данными должна содержать не только численные значения, но и названия строк или столбцов.*

**Выход** - нажав на кнопку выход, вы покидаете программу.

**Помощь** - во вкладке помощь можно ещё раз прочитать полезную информацию.

# terminal_connection.py
Это - консольное приложение, принимающее запросы в формате terminal_connection.py [-h] [-f_mnk] [-f] [-s] [-t]. Далее пречислены опции:

**-h, —help** - выводит справочную информацию.

**-f_mnk, —figure_with_mnk** - опция позволяет строить линеаризованный график.

**-f, —figure** - опция позволяет строить обычный график по точкам.

**-s, —sigma** - с помощью опции можно получить коэффициенты прямой и их погрешности.

**-t, —table** - опция вызывает функцию, которая создает Latex таблицу.
