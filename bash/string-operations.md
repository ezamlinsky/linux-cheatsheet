# Работа со строками

## Длина строки
<pre>
<b>${#string}</b>                          Возвращает длину строки $string
</pre>

## Извлечение подстроки
<pre>
<b>${string:position}</b>                  Извлекает подстроку из строки $string, начиная с позиции $position
<b>${string:position:length}</b>           Извлекает $length символов из строки $string, начиная с позиции $position
</pre>

## Удаление части строки
<pre>
<b>${string#substring}</b>                 Удаляет самую короткую подстроку $substring в строке $string. Поиск ведется с начала строки
<b>${string##substring}</b>                Удаляет самую длинную подстроку $substring в строке $string. Поиск ведется с начала строки
<b>${string%substring}</b>                 Удаляет самую короткую подстроку $substring в строке $string. Поиск ведется с конца строки
<b>${string%%substring}</b>                Удаляет самую длинную подстроку $substring в строке $string. Поиск ведется с конца строки
</pre>

## Замена подстроки
<pre>
<b>${string/substring/replacement}</b>     Заменяет первое вхождение $substring строкой $replacement
<b>${string//substring/replacement}</b>    Заменяет все вхождения $substring строкой $replacement
<b>${string/#substring/replacement}</b>    Вставляет строки $replacement вместо $substring. Поиск ведется с начала строки $string
<b>${string/%substring/replacement}</b>    Вставляет строки $replacement вместо $substring. Поиск ведется с конца строки $string
</pre>

## Изменение регистра символов
<pre>
<b>${string^pattern}</b>                   Устанавливает заглавные буквы для первого(ых) совпадающих символов в параметре
<b>${string^^pattern}</b>                  Устанавливает заглавные буквы для всех совпадающих символов в параметре
<b>${string,pattern}</b>                   Устанавливает строчные буквы для первого(ых) совпадающих символов в параметре
<b>${string,,pattern}</b>                  Устанавливает строчные буквы для всех совпадающих символов в параметре
<b>${string@u}</b>                         Преобразует первый симол строки в верхний регистр
<b>${string@U}</b>                         Преобразует всю строку в верхний регистр
<b>${string@L}</b>                         Преобразует всю строку в нижний регистр
</pre>
