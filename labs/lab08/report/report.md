---
## Front matter
title: "Лабораторная работа №8"
subtitle: " Поиск файлов. Перенаправление
ввода-вывода. Просмотр запущенных процессов"
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

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных.
Приобретение практических навыков: по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.

# Задание

- Выполнить задания по перенаправлению потоков и записи в файл
- Выполнить задания по управлению задачами и их открытию в фоновом режиме

# Теоретическое введение

В системе по умолчанию открыто три специальных потока:
– stdin — стандартный поток ввода (по умолчанию: клавиатура), файловый дескриптор
0;
– stdout — стандартный поток вывода (по умолчанию: консоль), файловый дескриптор
1;
– stderr — стандартный поток вывод сообщений об ошибках (по умолчанию: консоль),
файловый дескриптор 2.
Большинство используемых в консоли команд и программ записывают результаты
своей работы в стандартный поток вывода stdout. Например, команда ls выводит в стандартный поток вывода (консоль) список файлов в текущей директории. Потоки вывода
и ввода можно перенаправлять на другие файлы или устройства. Проще всего это делается
с помощью символов >, >>, <, <<

Конвейер (pipe) служит для объединения простых команд или утилит в цепочки, в которых результат работы предыдущей команды передаётся последующей.

Команда find используется для поиска и отображения на экран имён файлов, соответствующих заданной строке символов.

Найти в текстовом файле указанную строку символов позволяет команда grep

Команда df показывает размер каждого смонтированного раздела диска

Любую выполняющуюся в консоли команду или внешнюю программу можно запустить
в фоновом режиме. Для этого следует в конце имени команды указать знак амперсанда
&.

Любой команде, выполняемой в системе, присваивается идентификатор процесса
(process ID). Получить информацию о процессе и управлять им, пользуясь идентификатором процесса, можно из любого окна командного интерпретатора.

Команда ps используется для получения информации о процессах

# Выполнение лабораторной работы

Запись списка файлов с расширением .conf в файл conf.txt (рис. @fig:fig1).

![Запись списка файлов с расширением .conf](image/img1.png){#fig:fig1 width=70%}

Нахождение файлов, начинающихся с conf в домашней папке двумя способами

![Нахождение файлов, начинающихся с conf](image/img2.png){#fig:fig2 width=70%}

Список файлов каталога /etc начинающихся на h в постраничном режиме и команда для его вывода (рис. @fig:fig3)(рис. @fig:fig4).

![Список файлов каталога /etc начинающихся на h в постраничном режиме](image/img3.png){#fig:fig3 width=70%}

![Проверка целостности файловой системы](image/img4.png){#fig:fig4 width=70%}

Нахождение файлов, начинающихся на log в домашней папке и запись их в файл(рис. @fig:fig6)(рис. @fig:fig7)

![Нахождение файлов, начинающихся на log](image/img5.png){#fig:fig6 width=70%}

![Удаление файла с названиями файлов, начинающимися на log](image/img6.png){#fig:fig7 width=70%}

 Открытие gedit в фоновом режиме и получение PID процесса тремя разными способами(рис. @fig:fig8)

![Открытие gedit в фоновом режиме и получение PID процесса](image/img7.png){#fig:fig8 width=70%}

Завершаем процесс gedit(рис. @fig:fig9)

![Завершаем процесс gedit](image/img8.png){#fig:fig9 width=70%}

Получаем информацию о командах du и df и выполняем их (рис. @fig:fig10)

![команды du и df](image/img9.png){#fig:fig10 width=70%}

Вывод списка директорий в домашней папке и команда для этого

![Вывод списка директорий в домашней папке](image/img10.png){#fig:fig11 width=70%}


# Выводы

Научились работать с потоками данных и процессами в Linux.

# Список литературы{.unnumbered}

::: {#refs}
:::
