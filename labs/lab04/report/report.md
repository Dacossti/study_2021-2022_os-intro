---
## Front matter
title: "**РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ ФАКУЛЬТЕТ ФИЗИКО-МАТЕМАТИЧЕСКИХ И ЕСТЕСТВЕННЫХ НАУК**"
subtitle: "**Лабораторная Работа №4 По курсу Операционные Системы**"
author: "Озьяс Стев Икнэль Дани НКНбд-02-21"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Цель данной работы ---  общаться с системой через командную строку.


# Задание

1. Определите полное имя вашего домашнего каталога. Далее относительно этого каталога будут выполняться последующие упражнения.
2. Выполните следующие действия:
   1. Перейдите в каталог /tmp.
   2. Выведите на экран содержимое каталога /tmp. Для этого используйте команду ls
с различными опциями. Поясните разницу в выводимой на экран информации.
   3. Определите, есть ли в каталоге /var/spool подкаталог с именем cron?
   4. Перейдите в Ваш домашний каталог и выведите на экран его содержимое. Определите, кто является владельцем файлов и подкаталогов?
3. Выполните следующие действия:
   1. В домашнем каталоге создайте новый каталог с именем newdir.
   2. В каталоге ~/newdir создайте новый каталог с именем morefun.
   3. В домашнем каталоге создайте одной командой три новых каталога с именами
letters, memos, misk. Затем удалите эти каталоги одной командой.
   4. Попробуйте удалить ранее созданный каталог ~/newdir командой rm. Проверьте,
был ли каталог удалён.
   5. Удалите каталог ~/newdir/morefun из домашнего каталога. Проверьте, был ли
каталог удалён.
4. С помощью команды man определите, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов,
входящих в него.
5. С помощью команды man определите набор опций команды ls, позволяющий отсортировать по времени последнего изменения выводимый список содержимого каталога
с развёрнутым описанием файлов.
6. Используйте команду man для просмотра описания следующих команд: cd, pwd, mkdir,
rmdir, rm. Поясните основные опции этих команд.
7. Используя информацию, полученную при помощи команды history, выполните модификацию и исполнение нескольких команд из буфера команд..

# Теоретическое введение

В операционной системе типа Linux взаимодействие пользователя с системой обычно
осуществляется с помощью командной строки посредством построчного ввода команд.
В табл. [-@tbl:std-dir] приведено краткое описание основных команд командной строки.

: Описание основных команд командной строки {#tbl:std-dir}

| Команда      | Действие                                                                                                                                                                         |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `man`        | для просмотра (оперативная помощь) в диалоговом режиме руководства (manual) по основным командам операционной системы типа Linux.                                                |
| `pwd `       | Для определения абсолютного пути к текущему каталогу                                                                                                                             |
| `cd`         | для перемещения по файловой системе операционной системы типа Linux                                                                                                              |
| `ls`         | для просмотра содержимого каталога                                                                                                                                               |
| `mkdir`      | для создания каталогов                                                                                                                                                           |
| `rm/rmdir`   | для удаления файлов и/или каталогов                                                                                                                                              |
| `history`    | для вывода на экран списка ранее выполненных команд                                                                                                                              |
| `touch`      | для создания файлов                                                                                                                                                              |

Более подробно об Unix см. в [@gnu-doc:bash;@newham:2005:bash;@zarrelli:2017:bash;@robbins:2013:bash;@tannenbaum:arch-pc:ru;@tannenbaum:modern-os:ru].

# Выполнение лабораторной работы

## Определение полного имена моего домашнего каталога
Так как мы уже находимся в домашнем каталоге, надо просто вводить команду pwd:  (рис. [-@fig:001])

![Определение полного имена моего домашнего каталога](image/1.png){ #fig:001 width=70% }

## Вывод на экран содержимого каталога /tmp
Так как мы уже находимся в домашнем каталоге, надо сначала вводить команду cd /tmp, а затем ls -a (все файлы и следовательно скритые) (рис. [-@fig:002]), ls -F (тип файлов)(рис. [-@fig:003]), ls -l(размер, тип, владелец, дата последней ревизии ) (рис. [-@fig:004]):

![Содержимое каталога (опция-a) /tmp](image/2.png){ #fig:002 width=70% }

![Содержимое каталога (опция-F) /tmp](image/3.png){ #fig:003 width=70% }

![Содержимое каталога (опция-l) /tmp](image/4.png){ #fig:004 width=70% }

## Поиск подкаталога cron в каталоге /var/spool
Надо сначала вводить команду cd и перейти в каталог /var/spool,  а затем вводить команду ls и узнать, что нет такого подкаталога в каталоге /var/spool (рис. [-@fig:005])

![Поиск подкаталога в каталог /var/spool](image/5.png){ #fig:005 width=70% }

## Содержимое домашнего каталога и владелец каталогов и файлов
Надо сначала вводить команду cd,  а затем вводить команду ls -l:  (рис. [-@fig:006]

![Содержимое домашнего каталога и владелец каталогов и файлов](image/6.png){ #fig:006 width=70% }

## Создание каталога newdir в домашнем каталоге
Так как мы уже находимся в домашнем каталоге, надо просто вводить команду mkdir newdir :  (рис. [-@fig:007])

![Создание каталога newdir в домашнем каталоге](image/7.png){ #fig:007 width=70% }

## Создание каталога morefun в каталоге newdir
Надо просто вводить команду cd newdir и вводить команду mkdir morefun :  (рис. [-@fig:008])

![Создание каталога morefun в каталоге newdir](image/8.png){ #fig:008 width=70% }

## Создание одной командой трех новых каталогов letters, memos, misk
Надо сначала вводить команду cd для перемещения в домашный каталог, а затем вводить команду mkdir letters, memos, misk:  (рис. [-@fig:009])

![Создание одной командой каталогов letters, memos, misk](image/9.png){ #fig:009 width=70% }

## Удаление каталогов letters, memos, misk
Надо вводить команду rmdir letters, memos, misk:  (рис. [-@fig:010])

![Удаление каталогов letters, memos, misk](image/10.png){ #fig:010 width=70% }

## Удаление каталога newdir
Надо вводить команду rm -r newdir, так как он не пустой каталог:  (рис. [-@fig:011])

![Удаление каталога newdir](image/11.png){ #fig:011 width=70% }

## Определение опции команды ls для просмотра содержимого каталога и их подкаталогов

Надо сначала вводить команду man ls, и потом команду ls -R:  (рис. [-@fig:012])

![Опция -R команды ls](image/12.png){ #fig:012 width=70% }

## Определение заданного набора опций команды ls
Можно вводить команду ls -Rcl (рис. [-@fig:013]) 

![Определение заданного набора опций команды ls](image/13.png){ #fig:013 width=70% }

или  ls -Rlt (рис. [-@fig:014]):

![Определение заданного набора опций команды ls](image/14.png){ #fig:014 width=70% }

## Описание команд cd, pwd, mkdir, rmdir, rm
Надо последовательно вводить команды man cd (рис. [-@fig:015]),

![описания команды cd](image/15.png){ #fig:015 width=70% }

man pwd (рис. [-@fig:016]),

![описания команды pwd](image/16.png){ #fig:016 width=70% }

man mkdir (рис. [-@fig:017]),

![описания команды mkdir](image/17.png){ #fig:017 width=70% }

man rmdir (рис. [-@fig:018]),

![описания команды rmdir](image/18.png){ #fig:018 width=70% }

man rm (рис. [-@fig:019]) :

![описания команды rm](image/19.png){ #fig:019 width=70% }

## Выполнение модификации и исполнения нескольких команд из буфера команд
Надо сначала вводить команду history, а затем можно например вводить команду !288:s/newdir/newdir1 (рис. [-@fig:020]) для модификации 

![Выполнение модификации](image/20.png){ #fig:020 width=70% }

и для исполнения команды man rmdir с:  (рис. [-@fig:021])

![Выполнение исполнения нескольких команд из буфера команд](image/21.png){ #fig:021 width=70% }


# Выводы

Мы научились взаимодействовать с системой через командную строку.

# Список литературы{.unnumbered}

::: {#refs}
:::

# Контрольные вопросы

1. **Что такое командная строка?**
    Командная строка строка, оканчивающаяся символом $, по которому пользователь вводит команды.
    
2. **При помощи какой команды можно определить абсолютный путь текущего каталога? Приведите пример.**
    Можно определить абсолютный путь текущего каталога при помощи команды ls
   1. [sozjyas@fedora ~]$ pwd
   2. /home/sozjyas

3. **При помощи какой команды и каких опций можно определить только тип файлов и их имена в текущем каталоге? Приведите примеры.**
    Можно определить только тип файлов и их имена в текущем каталоге при помощи команды ls -F
   1. [sozjyas@fedora ~]$ ls -F
   2. Bureau/      install-tl-unx/         Modèles/   newdir1/    Téléchargements/
   3. Documents/  'install-tl-unx (1)'/    morefun/   Pictures/   Vidéos/
   4. Images/      install-tl-unx.tar.gz   Musique/   Public/     work/

4. **Каким образом отобразить информацию о скрытых файлах? Приведите примеры.**
    Можно отобразить информацию о скрытых файлах при помощи команды ls -al
   1. -rw-------. 1 sozjyas sozjyas    3412 30 avril 10:12  .bash_history
   2. -rw-r--r--. 1 sozjyas sozjyas      18 21 juil.  2021  .bash_logout
    
5. **При помощи каких команд можно удалить файл и каталог? Можно ли это сделать одной и той же командой? Приведите примеры.**
   Можно удалить файл и каталог   rm, rmdir, rm -r. Да, но с различными опциями.
   
   
6. **Каким образом можно вывести информацию о последних выполненных пользователем командах? работы?**
   Надо просто вводить команду history
   
7. **Как воспользоваться историей команд для их модифицированного выполнения? Приведите примеры.**
   !<номер_команды>:s/<что_меняем>/<на_что_меняем>
   !288:s/newdir/newdir1
   
8. **Приведите примеры запуска нескольких команд в одной строке.**
    cd ; ls
    cd ; mkdir newdir
    
9. **Дайте определение и приведите примера символов экранирования.**
    Экранирование символов — замена в тексте управляющих символов на соответствующие текстовые подстановки. 
    Пример символов- \
    
10. **Охарактеризуйте вывод информации на экран после выполнения команды ls с опцией**
    Можно отобразить имена всех файлов и следовательно скрытых файлов при помощи команды ls с опцией a
    ls -F --> тип файлов, ls -l --> размер, тип, владелец, дата последней ревизии итд
    
11. **Что такое относительный путь к файлу? Приведите примеры использования относительного и абсолютного пути при выполнении какой-либо команды.**
    Относительный путь к файлу это путь к файлу относительно к текущему каталогу.
    Пример абсолютного пути
    [sozjyas@fedora lpd]$ pwd
    /var/spool/lpd
    
    Пример относительного пути
    Путь к lpd относительно к каталогу var - spool/lpd
    
12. **Как получить информацию об интересующей вас команде?**
    Надо просто вводить команду man "команда"
    
13. **Какая клавиша или комбинация клавиш служит для автоматического дополнения вводимых команд?**
    Tab служит для автоматического дополнения вводимых команд.
