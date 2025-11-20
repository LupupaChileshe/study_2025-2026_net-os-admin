---
## Front matter
lang: ru-RU
title: Администрирование сетевых подсистем
subtitle: Лабораторная работа №1
author:
  - Чилеше Лупупа
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 13 ноября 2025
## i18n babel
babel-lang: russian
babel-otherlangs: english
## PDF formatting
toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цели и задачи работы

## Цель лабораторной работы

Приобретение практических навыков по развертыванию Rocky Linux в среде Vagrant и автоматизации конфигурации с использованием Packer и provisioning-скриптов.

# Выполнение лабораторной работы

## Подготовка конфигурационных файлов

![Фрагмент Vagrantfile](Screenshot_1.png){ width=70% }

## Создание пользователя

![Provisioning-скрипт создания пользователя](Screenshot_2.png){ width=70% }

## Автоматическая смена hostname

![Provisioning-скрипт изменения hostname](Screenshot_3.png){ width=70% }

## Создание box-файла

![Добавление box-файла в Vagrant](Screenshot_4.png){ width=70% }

## Запуск server через Vagrant

![Запуск VM server](Screenshot_5.png){ width=70% }

## Графический интерфейс server

![Рабочий стол Server](Screenshot_6.png){ width=70% }

## Подключение через SSH

![Подключение SSH](Screenshot_7.png){ width=70% }

# Вывод

Развернут полноценный лабораторный стенд на основе VirtualBox и Vagrant, включающий сборку box-файла через Packer, автоматическую установку Rocky Linux и запуск виртуальных машин с использованием provisioning-скриптов. Работа подтверждает эффективность применения инструментов автоматизации для подготовки инфраструктуры.
