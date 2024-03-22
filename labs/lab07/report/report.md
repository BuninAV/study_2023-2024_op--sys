---
## Front matter
title: "Лабораторная работа №7"
subtitle: "Анализ файловой системы Linux.
Команды для работы с файлами и каталогами"
author: "Бунин Арсений Викторович"

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

Ознакомление с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретение практических навыков по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.

# Задание

- Выполнить все примеры, приведенные в тексте лабораторной работы
- Выполнить задание по работе в файловой системе через терминал
- Выполнить задание по работе с правами доступа в файловой системе через терминал
- Проверить целостность файловой системы

# Теоретическое введение

Для создания текстового файла можно использовать команду touch. Для просмотра файлов небольшого размера можно использовать команду cat. Команда cp используется для копирования файлов и каталогов
Команды mv и mvdir предназначены для перемещения и переименования файлов и каталогов. Каждый файл или каталог имеет права доступа (табл. 5.1).
В сведениях о файле или каталоге указываются:
– тип файла (символ (-) обозначает файл, а символ (d) — каталог);
– права для владельца файла (r — разрешено чтение, w — разрешена запись, x — разрешено выполнение, - — право доступа отсутствует);
– права для членов группы (r — разрешено чтение, w — разрешена запись, x — разрешено
выполнение, - — право доступа отсутствует);
– права для всех остальных (r — разрешено чтение, w — разрешена запись, x — разрешено
выполнение, - — право доступа отсутствует).
Для просмотра используемых в операционной системе файловых систем можно воспользоваться командой mount без параметров. 
Другой способ определения смонтированных в операционной системе файловых систем — просмотр файла/etc/fstab. 
Сделать это можно например с помощью команды cat
С помощью команды fsck можно проверить (а в ряде случаев восстановить) целостность файловой системы
# Выполнение лабораторной работы

Создание, копирование и чтение папок и файлов(рис. @fig:fig1).

![Первичная работа с файловой системой](image/img1.png){#fig:fig1 width=70%}

Перемещение файлов и папок

![Перемещение объектов файловой системы](image/img2.png){#fig:fig2 width=70%}

Управление правами доступа в файловой системе (рис. @fig:fig3).

![Изменяем доступ к файлам и папкам](image/img3.png){#fig:fig3 width=70%}

Проверяем целостность файловой системы (рис. @fig:fig4).

![Проверка целостности файловой системы](image/img4.png){#fig:fig4 width=70%}

Самостоятельная работа по созданию, копированию и чтению папок (рис. @fig:fig6)

![Копируем, создаем и читаем файлы и папки](image/img5.png){#fig:fig6 width=70%}

Самостоятельная работа по редактированию прав доступа(рис. @fig:fig7)

![Редактирование прав доступа](image/img6.png){#fig:fig7 width=70%}

 Отказано в доступе к папке по причине закрытия исполнения функций папки, то есть ее открытия(рис. @fig:fig8)

![Отказ в доступе](image/img7.png){#fig:fig8 width=70%}

Получение справочных сведений о четырех командах, работающих с монтированием и целостностью файловой системы

![Получение справочных сведений о команде mount](image/img8.png){#fig:fig9 width=70%}

![Получение справочных сведений о команде fsck](image/img9.png){#fig:fig10 width=70%}

![Получение справочных сведений о команде mkfs](image/img10.png){#fig:fig11 width=70%}

![Получение справочных сведений о команде kill](image/img11.png){#fig:fig12 width=70%}


# Выводы

Научились работать с файловой системой Linux.

# Список литературы{.unnumbered}

::: {#refs}
:::
