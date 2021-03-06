---
## Front matter
lang: ru-RU
title: Лабораторная работа № 7. Командная оболочка Midnight Commander
author: |
	ОЗЬЯС Стев Икнэль Дани\
	\
	НКНбд-02-21\
	\

institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
	\
date: 13  May, 2022 Moscow, Russia

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# Цель работы

Цель данной работы --- освоение основных возможностей командной оболочки Midnight Commander. Приобретение навыков практической работы по просмотру каталогов и файлов; манипуляций
с ними. 


# Ход работы

# Задание по mc

## Выполнение задание 1

1. Изучил информацию о mc, вызвав в командной строке man mc (рис. [-@fig:001])

![Справка по mc](image/1.png){ #fig:001 width=70% }

## Выполнение задание 2

2. Запустите из командной строки mc, изучите его структуру и меню. (рис. [-@fig:002])

![Mc](image/2.png){ #fig:002 width=70% }

## Выполнение задание 3

3. Выполнил, используя управляющие клавиши (операции
с панелями: 
   1. Выделение файлов с помощью прапвой кнопки мыши (рис. [-@fig:003])
   
![Выделение](image/3.png){ #fig:003 width=70% }

##   
   2. Отмена выделения с помощью прапвой кнопки мыши (рис. [-@fig:004])
   
![Отмена выделения](image/4.png){ #fig:004 width=70% }

##    
   3. Копирование файлов с помощью F5 (рис. [-@fig:005]
   
![Копирование файлов](image/5.png){ #fig:005 width=70% }

##    
   4. Перемещение файлов с помощью F6 (рис. [-@fig:006]
   
![Перемещение файлов](image/6.png){ #fig:006 width=70% }
    
##
   5. Получение с помощью команды Информация подменю Левая панель информации о размере и правах доступа на каталог play (рис. [-@fig:007])

![Получение информации о размере и правах доступа](image/7.png){ #fig:007 width=70% }

## Выполнение задание 4

4.  Выполнил основные команды меню левой панели:
   - Список файлов (рис. [-@fig:008])

![Список файлов](image/8.png){ #fig:008 width=70% }

##
   - Дерево каталогов (рис. [-@fig:009])

![Дерево каталогов](image/9.png){ #fig:009 width=70% }

##
   - Быстрый просмотр (рис. [-@fig:010])

![Быстрый просмотр](image/10.png){ #fig:010 width=70% }

##
   - Расширенный формат списка (рис. [-@fig:011])

![Расширенный формат списка](image/11.png){ #fig:011 width=70% }

##
   - Порядок сортировки (рис. [-@fig:012])

![Порядок сортировки](image/12.png){ #fig:012 width=70% } 

## Выполнение задание 5

5. Используя возможности подменю Файл, я выполнил: 
   - Просмотр содержимого текстового файла (рис. [-@fig:013])

![Просмотр содержимого текстового файла](image/13.png){ #fig:013 width=70% }

##
   - Редактирование содержимого текстового файла (без сохранения результатов
редактирования); (рис. [-@fig:014])

![Редактирование содержимого текстового файла](image/14.png){ #fig:014 width=70% }

## 
   - Создание каталога; (рис. [-@fig:015])

![Создание каталога](image/15.png){ #fig:015 width=70% }

##
   - Копирование файлов в созданный каталог (рис. [-@fig:016])

![Копирование файлов в созданный каталог](image/16.png){ #fig:016 width=70% }

## Выполнение задание 6

6. Используя возможности подменю Файл, я выполнил:
   - Поиск в файловой системе файла с расширением .cpp, содержащего строку main (рис. [-@fig:017])

![Поиск в файловой системе файла с расширением .cpp, содержащего строку main](image/17.png){ #fig:017 width=70% }

##
   - Выбор и повторение одной из предыдущих команд (рис. [-@fig:018])

![Выбор и повторение одной из предыдущих команд](image/18.png){ #fig:018 width=70% }

##
   - Переход в домашний каталог (рис. [-@fig:019])

![Переход в домашний каталог](image/19.png){ #fig:019 width=70% }

##
   - Анализ файла меню (рис. [-@fig:020])

![Анализ файла меню](image/20.png){ #fig:020 width=70% }

##
   - И файла расширений.(рис. [-@fig:021])

![Анализ файла расширений](image/21.png){ #fig:021 width=70% }

##
   - Вызовил подменю Настройки и освоил операции, определяющие структуру экрана mc
(Full screen, Double Width, Show Hidden Files и т.д.) (рис. [-@fig:022])

![Определение Show Hidden Files](image/22.png){ #fig:022 width=70% }

#  Задание по встроенному редактору mc

## Выполнение задание 1

  - Создал текстовой файл text.txt. (рис. [-@fig:023])
  
![Создание текстового файла text.txt](image/23.png){ #fig:023 width=70% }

## Выполнение задание 2
   - Открыл этот файл с помощью встроенного в mc редактора. (рис. [-@fig:024])
   
![Отображение текстового файла text.txt с помощью встроенного в mc редактора](image/24.png){ #fig:024 width=70% }

## Выполнение задание 3
   - Вставил в открытый файл небольшой фрагмент текста, скопированный из любого
другого файла или Интернета. (рис. [-@fig:025])
   
![Редактирование текстового файла text.txt](image/25.png){ #fig:025 width=70% }

## Выполнение задание 4

   - Удалил строку текста. (рис. [-@fig:026])
   
![Удаление строки текста](image/26.png){ #fig:026 width=70% }

##
   - Выделил фрагмент текста и скопировал его на новую строку. (рис. [-@fig:027])
   
![Скопирование строки текста на новую строку](image/27.png){ #fig:027 width=70% }

##
   - Выделил фрагмент текста и перенес его на новую строку. (рис. [-@fig:028])
   
![Перемешение строки текста на новую строку](image/28.png){ #fig:028 width=70% }

##
    - Сохранил файл. (рис. [-@fig:029])
  
![Сохранение текстового файла text.txt](image/29.png){ #fig:029 width=70% }

##
   - Отменил последнее действие. (рис. [-@fig:030])
  
![Отменение последнего действия](image/30.png){ #fig:030 width=70% }

##
   - Перешел в конец файла (нажав Ctrl + end) и написал некоторый текст. (рис. [-@fig:031])
  
![Редактирование текстового файла text.txt в конец](image/31.png){ #fig:031 width=70% }

##
   - Перешел в начало файла (нажав Ctrl + home) и написал некоторый текст. (рис. [-@fig:032])
  
![Редактирование текстового файла text.txt в начало](image/32.png){ #fig:032 width=70% }

##
   - Сохранил и закрыл файл. (рис. [-@fig:033])
  
![Сохранение текстового файла text.txt](image/33.png){ #fig:033 width=70% }

## Выполнение задание 5

5. Открыл файл с исходным текстом на языке программирования C рис. [-@fig:034])
  
![Файл с исходным текстом на некотором языке программирования С](image/34.png){ #fig:034 width=70% }

## Выполнение задание 6

6. Используя меню редактора, выключил подсветку синтаксиса (рис. [-@fig:035])

![Выключение подсветки синтаксиса](image/35.png){ #fig:035 width=70% }

# Выводы

Я освоил основные возможности командной оболочки Midnight Commander и приобретил навыки практической работы по просмотру каталогов и файлов; манипуляций с ними.


## {.standout}

Wer's nicht glaubt, bezahlt einen Taler
