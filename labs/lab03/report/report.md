---
## Front matter
title: "Отчет по лабораторной работе"
subtitle: "Архитектура компьютеров и операционных систем"
author: "Виктор Ващаев Андреевич"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Целью работы является освоение процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

# Задание
1) Установка необходимого ПО.
2) Заполнение отчета по выполнению лабораторной работы №4 с помощью
языка разметки Markdown.
3) Задание для самостоятельной работы.

# Теоретическое введение

Markdown — облегчённый язык разметки, созданный с целью обозначения форматирования в простом тексте, с максимальным сохранением его читаемости человеком, и пригодный для машинного преобразования в языки для продвинутых публикаций. в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы


Выполняю первые 6 пунктов. Сложности возникали, но упорство взяло вверх надо мной.

![Название рисунка](/home/victor/Pictures/Снимки экрана/3laba.png){#fig:001 width=70%}
В этой лабораторной работе я выполнил следующие действия:
 1 Перешел в нужную директорию, где находятся файлы лабораторной работы, используя команду cd. Для этого ввел в терминале:
cd "/home/victor/work/study/2023-2024/Архитектура компьютера/study_2023_2024_arh-pc/labs/lab03/report"
Это действие позволило работать в каталоге, где находятся Makefile и все необходимые файлы для компиляции отчета.
 2 Обновил репозиторий, выполнив команду git pull, чтобы синхронизировать изменения из удаленного репозитория с локальными файлами. Для этого ввел команду:
git pull
 3 Запустил процесс компиляции, используя Makefile. Для этого ввел в терминале команду make, которая запустила сборку отчетов в форматах .docx и .pdf с использованием утилиты pandoc и фильтра pandoc-crossref. Команда:
make
 4 В процессе компиляции я получил предупреждение: "WARNING: pandoc-crossref was compiled with pandoc 3.5 but is being run through 3.1.3."
Это предупреждение говорит о том, что установленная версия pandoc-crossref была собрана для другой версии pandoc, однако сборка продолжилась. Важно отметить, что несовместимость версий может привести к странному поведению программы.
Далее редактировал report.md и загрузил ссылку на гит хаб, вот ссылка на мой гит хаб: 

# Выводы

Выводы:
 Я успешно перешел в нужную директорию и обновил файлы через команду git.
 Команда make выполнилась корректно, хотя было получено предупреждение о несовместимости версий pandoc и pandoc-crossref.
 Но главное что я для себя понял что если включать мозги, то не происходит никаких проблем в ходе лабораторной)
 

# Список литературы{.unnumbered}

простите, я не сильно в этом разбираюсь, не могу ничего посоветовать(
Самостоятельная работа будет выполнена в другом файле 
