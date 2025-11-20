---
## Front matter
title: "Отчёт по лабораторной работе 1"
subtitle: "Подготовка лабораторного стенда"
author: "Чилеше Лупупа"

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
papersize: a
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

Целью данной работы является приобретение практических навыков установки Rocky Linux на виртуальную машину с помощью инструмента Vagrant.

# Выполнение работы

## Развёртывание лабораторного стенда в среде Windows

Для развертывания лабораторного стенда использовалась операционная система Windows с установленными VirtualBox и Vagrant. После установки необходимого ПО система была перезагружена.

## Подготовка и настройка конфигурационных файлов

В рабочем каталоге были размещены файл `Vagrantfile` и provisioning-скрипты для автоматической настройки виртуальных машин. На изображении показан фрагмент файла конфигурации Vagrant с настройками VirtualBox и libvirt:

![Фрагмент Vagrantfile](Screenshot_1.png){ #fig:001 width=80% }

Ниже приведён фрагмент скрипта создания пользователя, выполняемого при поднятии машины:

![Provisioning-скрипт создания пользователя](Screenshot_2.png){ #fig:002 width=80% }

Дополнительно используется скрипт для автоматической смены имени хоста:

![Provisioning-скрипт изменения hostname](Screenshot_3.png){ #fig:003 width=80% }

## Сборка образа виртуальной машины с помощью Packer

Для автоматической установки Rocky Linux был использован Packer. После выполнения команд `packer init` и `packer build` в каталоге появился box-файл.

## Регистрация созданного образа в Vagrant

Созданный образ был зарегистрирован в локальном репозитории Vagrant:

![Добавление box-файла в Vagrant](Screenshot_4.png){ #fig:004 width=80% }

## Запуск виртуальной машины Server

После регистрации образа была запущена виртуальная машина Server:

![Запуск VM server через Vagrant](Screenshot_5.png){ #fig:005 width=80% }

Затем сервер успешно загрузился в графическом окружении:

![Графический интерфейс виртуальной машины Server](Screenshot_6.png){ #fig:006 width=80% }

## Проверка доступа к машине через SSH

Для проверки корректности конфигурации выполнено подключение по SSH и смена пользователя:

![Подключение по SSH и проверка пользователя](Screenshot_7.png){ #fig:007 width=80% }

# Вывод

В ходе выполнения работы был развёрнут лабораторный стенд на базе VirtualBox и Vagrant, автоматизирующий процесс создания и настройки виртуальных машин. Использование Packer позволило собрать собственный box-файл с Rocky Linux, а provisioning-скрипты обеспечили подготовку окружения без ручного вмешательства. Все этапы — от генерации образа до запуска и проверки доступа к виртуальным машинам — выполнены успешно, что подтвердило корректность конфигурации и работоспособность стенда.

# Контрольные вопросы

**1. Для чего предназначен Vagrant?**  
Vagrant используется для автоматизированного развертывания и управления виртуальными машинами. Он позволяет создавать повторяемые и предсказуемые среды разработки, устраняя необходимость ручной настройки каждой системы. С его помощью разработчики и администраторы могут быстро поднимать виртуальные стенды, используя единый конфигурационный файл.

**2. Что такое box-файл? В чём назначение Vagrantfile?**  
Box-файл — это шаблон (образ) виртуальной машины, включающий предустановленную операционную систему и базовые настройки. Он служит основой для создания новых виртуальных машин в Vagrant.  
Vagrantfile — главный конфигурационный файл проекта Vagrant. В нём указываются параметры виртуальных машин: используемый box-файл, объём памяти, количество процессоров, настройки сетевых интерфейсов, синхронизация папок и запуск provisioning-скриптов.

**3. Приведите описание и примеры вызова основных команд Vagrant.**  
Основные команды Vagrant включают:  
- `vagrant init` — создание нового Vagrantfile;  
- `vagrant box add` — добавление box-файла в локальный репозиторий;  
- `vagrant up` — запуск и создание виртуальной машины;  
- `vagrant ssh` — подключение к машине по SSH;  
- `vagrant halt` — остановка виртуальной машины;  
- `vagrant destroy` — удаление созданной машины;  
- `vagrant status` — просмотр состояния виртуальной машины.

Примеры использования:  
- Запуск виртуальной машины: `vagrant up server`  
- Подключение по SSH: `vagrant ssh client`  
- Остановка машины: `vagrant halt server`

**4. Дайте построчные пояснения содержания файлов vagrant-rocky.pkr.hcl, ks.cfg, Vagrantfile, Makefile.**  
- **vagrant-rocky.pkr.hcl** — конфигурация Packer. Описывает источник ISO-образа, параметры виртуальной машины для установки, путь к kickstart-файлу, а также процесс сборки box-файла.  
- **ks.cfg** — kickstart-файл, используемый для автоматической установки Rocky Linux. Содержит параметры разметки диска, выбора пакетов, создания пользователей, сетевых настроек и других этапов инсталляции.  
- **Vagrantfile** — конфигурационный файл Vagrant. Определяет используемый box-файл, настройки провайдера (VirtualBox или libvirt), параметры оперативной памяти, процессоров, сетевых интерфейсов, а также provisioning-скрипты, выполняющиеся при создании машины.  
- **Makefile** — набор автоматизированных задач для управления проектом. Может включать цели для запуска, остановки и пересоздания виртуальных машин, упрощая выполнение сложных последовательностей команд.
