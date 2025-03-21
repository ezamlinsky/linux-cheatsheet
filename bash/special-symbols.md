# Базовые синтаксис
<pre>
#               Начинает однострочный комментарий
:               Пустая команда (эквивалент "NOP"). Всегда возвращает "true"
;               Разделитель команд
;;              Ограничитель в операторе выбора "case"
.               Эквивалент команды "source"
\               Экранирует символ
&               Выполнение задачи в фоновом режиме
</pre>

# Опциональные ключи команд
<pre>
-               После дефиса начинаются опциональные ключи команд
</pre>

# Подстановки путей
<pre>
.               Текущий каталог
..              Родительский каталог
~               Домашний каталог
~user           Домашний каталог пользователя "user"
~+              Текущий рабочий каталог ($PWD)
~-              Предыдущий рабочий каталог ($OLDPWD)
-               Предыдущий рабочий каталог для команда "cd"
/               Разделитель путей к каталогам и файлам
{str1,str2,...} Подстановка строк в путь к файлу
</pre>

# Шаблоны файлов
<pre>
*               Соответствует любой строке, включая пустую строку
?               Соответствует любому одиночному символу
[ ]             Соответствует любому из указанного диапазона символов
?(list)         Соответствует нулю или одному вхождению указанных шаблонов
*(list)         Соответствует нулю или нескольким вхождениям указанных шаблонов
+(list)         Соответствует одному или нескольким вхождениям указанных шаблонов
@(list)         Соответствует одному из указанных шаблонов
!(list)         Соответствует чему угодно, кроме одного из указанных шаблонов
</pre>

# Перенаправление ввода и вывода
<pre>
[N]<            Перенаправление ввода
[N]>            Перенаправление вывода
[N]>>           Перенаправление вывода с добавлением
>|              Принудительное перенаправление, даже если установлена опция "noclobber"
&>, >&          Перенаправление стандартного вывода и потока ошибок
<<              Перенаправление ввода на встроенный документ
|               Передает вывод предыдущей команды на ввод следующей (конвеер)
</pre>

# Дескрипторы файлов
<pre>
[N]<>FILE       Связывает файловый дескриптор с файлом
[N]<&-          Закрывает дескриптор входного файла N
[N]>&-          Закрывает дескриптор выходного файла N
0<&-, <&-       Закрывает stdin
1>&-, >&-       Закрывает stdout
</pre>

# Регулярные выражения
<pre>
.               Обозначает одиночный символ
*               Обозначает любое количество (в том числе и 0) символов
^               Обозначает начало строки
$               Обозначает конец строки
\<, \>          Границы отдельных слов в регулярных выражениях
[ ]             Диапазон символов в регулярных выражениях
[:alnum:]       Соответствует алфавитным символам и цифрам. Эквивалентно выражению [A-Za-z0-9]
[:alpha:]       Соответствует символам алфавита. Эквивалентно выражению [A-Za-z]
[:blank:]       Соответствует символу пробела или символу табуляции
[:cntrl:]       Соответствует управляющим символам (control characters)
[:digit:]       Соответствует набору десятичных цифр. Эквивалентно выражению [0-9]
[:graph:]       Соответствует набору символов из диапазона ASCII 33 - 126
[:lower:]       Соответствует набору алфавитных символов в нижнем регистре. Эквивалентно выражению [a-z]
[:print:]       Соответствует набору символов из диапазона ASCII 32 - 126
[:space:]       Соответствует пробельным символам (пробел и горизонтальная табуляция)
[:upper:]       Соответствует набору символов алфавита в верхнем регистре. Эквивалентно выражению [A-Z]
[:xdigit:]      Соответствует набору шестнадцатиричных цифр. Эквивалентно выражению [0-9A-Fa-f]
</pre>

# Кавычки
<pre>
'               Одинарные кавычки. Экранирует все служебные символы в строке
"               Двойные кавычки. Не выполняется интерпретация большинства служебных символов
`               Обратные кавычки. Команда исполняется в подоболочке, результат записывается в переменную
</pre>

# Скобки

## Квадратные скобки
<pre>
Array[1]=a1     Обращение к элементу массива
</pre>

## Фигурные скобки
<pre>
{ cmd1; cmd2 }  Блок кода для вызова внутри текущей оболочке
</pre>

## Круглые скобки
<pre>
Array=(v1 v2)   Инициализация массива
result=$(CMD)   Команда исполняется в подоболочке, результат записывается в переменную
(cmd1; cmd2)    Группа команд, исполняемая в подоболочке
>(CMD)          Вывод данных во входной поток процесса
<(CMD)          Ввод данных из выходного потока процесса
</pre>
