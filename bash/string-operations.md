# Работа со строками

## Длина строки
<pre>
${#string}                          Длина строки $string
</pre>

## Извлечение подстроки
<pre>
${string:position}                  Извлечение подстроки из строки $string, начиная с позиции $position
${string:position:length}           Извлечение $length символов из строки $string, начиная с позиции $position
</pre>

## Удаление части строки
<pre>
${string#substring}                 Удаление самой короткой подстроки $substring в строке $string. Поиск ведется с начала строки
${string##substring}                Удаление самой длинной подстроки $substring в строке $string. Поиск ведется с начала строки
${string%substring}                 Удаление самой короткой подстроки $substring в строке $string. Поиск ведется с конца строки
${string%%substring}                Удаление самой длинной подстроки $substring в строке $string. Поиск ведется с конца строки
</pre>

## Замена подстроки
<pre>
${string/substring/replacement}     Замещает первое вхождение $substring строкой $replacement
${string//substring/replacement}    Замещает все вхождения $substring строкой $replacement
${string/#substring/replacement}    Подстановка строки $replacement вместо $substring. Поиск ведется с начала строки $string
${string/%substring/replacement}    Подстановка строки $replacement вместо $substring. Поиск ведется с конца строки $string
</pre>
