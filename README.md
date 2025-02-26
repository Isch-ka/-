# Что такое Git?

Git — это система контроля версий, которая помогает отслеживать историю изменений в файлах. Она позволяет нескольким разработчикам одновременно работать над одним продуктом.

Git хранит все версии проекта (коммиты) и даёт возможность откатить текущую версию кода до предыдущей или сразу на несколько шагов назад. Это удобно, если после изменения коммита допущена ошибка.

Git — это программа, которую нужно установить и подключить к проекту для управления системой контроля версий. Например, можно установить её на сервер и настроить удалённую работу самостоятельно, а можно воспользоваться готовыми сервисами, самый популярный из которых — GitHub.

GitHub — это сайт-хранилище для историй версий проектов: нужно подключить Git, зарегистрироваться на GitHub, создать там онлайн-репозиторий и перенести туда файлы из своего репозитория.

# Установка Git и Visual Studio Code

Установка Git зависит от операционной системы:

* Для Windows. Перейдите на официальный сайт Git в раздел загрузок. Выберите Standalone-версию и запустите скачанный файл. На первом экране выберите компоненты для установки. Если нужны дополнительные иконки на рабочем столе или ежедневная проверка наличия новой версии, отметьте соответствующие опции. Остальные параметры лучше оставить по умолчанию.
* Для macOS. Установите Homebrew и выполните команду brew install git. Чтобы обновить установку Git, используйте параметр обновления Homebrew: brew upgrade git. Графический установщик для Git на macOS также доступен на официальном веб-сайте Git.
* Для Linux. Используйте собственную систему управления пакетами дистрибутива Linux для установки и обновления Git. Например, в Ubuntu: sudo apt-get install git.

После установки Git доступен из командной строки или PowerShell. Рекомендуется выбрать значения по умолчанию во время установки, если их не нужно изменить.

➤Установка Git для Windows, MAC, Linux: 
https://git-scm.com/downloads

➤Установка VSCode для Windows, MAC, Linux: https://code.visualstudio.com/Download

При первом использовании Git необходимо представиться.  Для 
этого нужно ввести в терминале 2 команды:

git config --global user.name «Ваше имя английскими буквами»

git config --global user.email ваша почта@example.com

# Основные команды Git

* git init – инициализация локального репозитория.
* git add. Добавляет содержимое рабочей директории в индекс для последующего коммита. 
* git commit -m “message” –создание коммита.
* git status. Показывает состояния файлов в рабочей директории и индексе: какие файлы изменены, но не добавлены в индекс, какие ожидают коммита в индексе. 
* git diff. Используется для вычисления разницы между любыми двумя Git-деревьями. 
* git commit. Берёт все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок. 
* git reset. Используется для отмены изменений. 
* git rm. Используется в Git для удаления файлов из индекса и рабочей директории. 
* git mv. Это удобный способ переместить файл, а затем выполнить git add для нового файла и git rm для старого. 
* git clean. Используется для удаления мусора из рабочей директории. 
* git branch. Это «менеджер веток». Она умеет перечислять ветки, создавать новые, удалять и переименовывать их. 
* git checkout. Используется для переключения веток и выгрузки их содержимого в рабочую директорию. 
* git checkout master – вернуться к актуальному состоянию и продолжить работу.
* git merge. Используется для слияния одной или нескольких веток в текущую. 
* git log. Используется для просмотра истории коммитов, начиная с самого свежего и уходя к истокам проекта.
* git stash. Используется для временного сохранения всех незакоммиченных изменений для очистки рабочей директории без необходимости коммитить незавершённую работу в новую ветку. 
* git tag. Используется для задания постоянной метки на какой-либо момент в истории проекта. Обычно она используется для релизов. 
* git fetch. Связывается с удалённым репозиторием и забирает из него все изменения, которых у пользователя пока нет, и сохраняет их локально. 
* git pull. Работает как комбинация команд git fetch и git merge: Git вначале забирает изменения из указанного удалённого репозитория, а затем пытается слить их с текущей веткой. 
* git push. Используется для установления связи с удалённым репозиторием, вычисления локальных изменений, отсутствующих в нём, и их передачи в репозиторий. 

# Синтаксис языка Markdown

## Параграфы и разрывы строк (paragraphs and line breaks)

Чтобы поделить текст на параграфы, между ними нужно оставить пустую строку. Строка считается пустой, даже если в ней есть пробелы и табуляции. Если же строки находятся рядом, то они автоматически склеиваются в одну.

Пример 1

Пример 2

Пример 1
Пример 2

Для переноса строки внутри одного параграфа есть три метода:

поставить в конце строки два или больше пробела   
поставить в конце строки обратную косую черту \
использовать HTML-тег <br>

Перенос с помощью пробелов  
Перенос с помощью обратного слеша\
Перенос с помощью тега <br> Последняя строка

## Заголовки (headings)

Чтобы выделить заголовок необходимо перед его название поставить значок "#":

Количество символов “#” задаёт уровень заголовка  
(поддерживается 6 уровней)

# Пример 1
## Пример 2
### Пример 3
#### Пример 4
##### Пример 5
###### Пример 6

У заголовков первого и второго уровня есть альтернативный способ выделения: на следующей строке после них нужно поставить знаки равенства = или дефисы -. Вот несколько правил:

знак = применяется для заголовков H1;
дефис применяется для заголовков H2;
если в одной строке поставить оба знака, то работать ничего не будет;
можно ставить любое количество знаков, и на тип заголовка это не повлияет;
между заголовком и знаками не должно быть пустых строк.

Заголовок первого уровня
=
Заголовок первого уровня
=========
Заголовок второго уровня
-
Заголовок второго уровня
----------

## Жирный (bold)

Чтобы сделать тикст жирным необходимо обрамить его с двух сторон символами "**" или "__":

**Жирный** / __Жирный__

## Курсив (italic)

Чтобы создать курсив необходимо обрамить текст с двух сторон символами "*" или "_":

*Курсив* / _Курсив_

## Жирный курсив (bold and italic)

Чтобы создать жирное курсивное начертание необходимо обрамить текст с двух сторон символом "***":

 ***Жирное курсивное начертание***

  ## Зачёркнутый (strikethrough)

 Чтобы создать зачёркнутый текст необходимо обрамить его с двух сторон символом "~~":

 ~~Зачёркнутый текст~~

 ## Подчёркнутый (underline)

 В синтаксисе Markdown нет встроенного способа подчеркнуть текст. Но если ваш редактор поддерживает HTML, то можно использовать теги:

 <u>Подчёркнутый текст</u>

 ## Разделители (horizontal rules)

 Чтобы оформить горизонтальный разделитель, нужно поставить три или больше специальных символа: звёздочки "*", дефиса "-" или нижних подчёркивания "_". Они должны находиться на отдельной строке, и между ними можно ставить любое количество пробелов и табуляций.

Если ваш редактор поддерживает HTML-теги, то для разметки можно также использовать тег <hr>

***
---
___
*	*  **


## Цитаты (blockquotes)

Чтобы параграф отобразился как цитата, нужно поставить перед ним закрывающую угловую скобку ">".

> Оформление цитатой
последовательных строк
внутри одного параграфа

Внутрь одного блока цитаты можно поместить сразу несколько параграфов и использовать любые элементы оформления. Чтобы сделать это, нужно поместить закрывающую угловую скобку перед началом каждой строки.

> # Заголовок
> Первый параграф
>
> Второй параграф
>
> > Вложенная цитата
> > > Цитата третьего уровня
>
> Продолжение основной цитаты

  ## Нумерованные списки (ordered)

 Для создания нумерованного списка перед пунктами нужно поставить число с точкой. При этом нумерация в разметке ленивая. Неважно, какие именно числа вы напишете: Markdown пронумерует список автоматически.
1. Первый пункт
2. Второй пункт
3. Третий пункт


1. Первый пункт
1. Второй пункт
1. Третий пункт


1. Первый пункт
73. Второй пункт
5. Третий пункт

Список можно начинать и не с единицы. Для нумерации важно только число, которое стоит перед первым пунктом.

27. Первый пункт
27. Второй пункт
27. Третий пункт

Обратите внимание, что между двумя нумерованными списками, идущими подряд, нужно отбить две пустые строки. Если отбить только одну, то Markdown воспримет два списка как один. Некоторые редакторы в таком случае увеличивают интервал между пунктами.

1. Первый пункт
2. Второй пункт
3. Третий пункт

1. Четвёртый пункт
2. Пятый пункт
3. Шестой пункт

## Ненумерованные (unordered)
 
Для создания ненумерованного списка нужно поставить перед каждым пунктом звёздочку "*", дефис "-" или плюс "+".

* Первый пункт
* Второй пункт
* Третий пункт
- Первый пункт
- Второй пункт
- Третий пункт
+ Первый пункт
+ Второй пункт
+ Третий пункт

Обратите внимание, что Markdown относит к разным спискам пункты, перед которыми стоят разные маркеры. Даже несмотря на то, что мы не оставляем пустых строк между списками.

Если же два списка идут подряд, а перед их пунктами стоят одинаковые маркеры, тогда между ними нужно отбить две пустые строки (как в случае с нумерованными списками).

## Чекбоксы (checkboxes)

Чтобы сделать чекбоксы, нужно использовать маркированный список, но между маркером и текстом поставить [x] для отмеченного пункта и [] — для неотмеченного.

Чекбоксы доступны в диалекте GitHub Flavored Markdown (тот самый, который умеет зачёркивать текст) и поддерживаются не всеми редакторами Markdown.

- [x] Отмеченный пункт
- [ ] Неотмеченный пункт

## Вложенные (nested)

Чтобы создать вложенный список, нужно поставить перед его пунктами табуляцию или несколько пробелов. В Markdown одна табуляция соответствует четырём пробелам.

Список одного вида можно вкладывать в любой другой.

1. Пункт
	1. Подпункт
		1. Подподпункт

- Пункт
	- Подпункт
		- Подподпункт


1. Пункт
	- Подпункт
		* Подподпункт

+ Пункт
	1. Подпункт

- Пункт
  - [x] Отмеченный подпункт
  - [ ] Неотмеченный подпункт
    1. Подподпункт

На самом деле количество пробелов, которые нужно поставить для корректного отступа, рассчитывается чуть сложнее. Берётся количество символов в маркере (один для "*", "-" и "+", два для "1.", три для 10.), и к нему прибавляется любое число от 1 до 4.

Таким образом, если в маркере 1 символ, нужно поставить от 2 до 5 пробелов, если 2 символа — от 3 до 6, если 3 символа — от 4 до 7.

## Другие элементы внутри списков

В пункты списков можно добавлять другие элементы оформления. Например, параграфы или цитаты. Для этого нужно сделать отступ, как если бы вы добавляли вложенный список.

1. Первый пункт
	> Цитата внутри первого пункта
1. Второй пункт
 	
    Параграф внутри второго пункта
1. Третий пункт

## Ссылки (links)

Самый лёгкий способ поместить ссылку в Markdown — заключить её в угловые скобки. Несмотря на простоту, он не является основным и был добавлен только в спецификации CommonMark.

<https://skillbox.ru/media/code/>

Чтобы оформить ссылкой часть текста, используется такой синтаксис: [текст](ссылка). Можно сделать всплывающую подсказку при наведении курсора. Для этого в круглых скобках после ссылки нужно поставить пробел и написать текст подсказки в кавычках.

[Skillbox Media](https://skillbox.ru/media/) без подсказки

[Skillbox Media](https://skillbox.ru/media/ "Круто, не правда ли?)") с подсказкой
