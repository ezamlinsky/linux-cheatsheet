# Работа со строками

## Длина строки
<pre>
${#string}                          Возвращает длину строки $string
</pre>

## Извлечение подстроки
<pre>
${string:position}                  Извлекает подстроку из строки $string, начиная с позиции $position
${string:position:length}           Извлекает $length символов из строки $string, начиная с позиции $position
</pre>

## Удаление части строки
<pre>
${string#substring}                 Удаляет самую короткую подстроку $substring в строке $string. Поиск ведется с начала строки
${string##substring}                Удаляет самую длинную подстроку $substring в строке $string. Поиск ведется с начала строки
${string%substring}                 Удаляет самую короткую подстроку $substring в строке $string. Поиск ведется с конца строки
${string%%substring}                Удаляет самую длинную подстроку $substring в строке $string. Поиск ведется с конца строки
</pre>

## Замена подстроки
<pre>
${string/substring/replacement}     Заменяет первое вхождение $substring строкой $replacement
${string//substring/replacement}    Заменяет все вхождения $substring строкой $replacement
${string/#substring/replacement}    Вставляет строки $replacement вместо $substring. Поиск ведется с начала строки $string
${string/%substring/replacement}    Вставляет строки $replacement вместо $substring. Поиск ведется с конца строки $string
</pre>

## Изменение регистра символов
<pre>
${string^pattern}                   Устанавливает заглавные буквы для первого(ых) совпадающих символов в параметре
${string^^pattern}                  Устанавливает заглавные буквы для всех совпадающих символов в параметре
${string,pattern}                   Устанавливает строчные буквы для первого(ых) совпадающих символов в параметре
${string,,pattern}                  Устанавливает строчные буквы для всех совпадающих символов в параметре
</pre>
