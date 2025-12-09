---
lang: ru-RU
title: Администрирование сетевых подсистем
subtitle: Лабораторная работа №6
author:
  - Чилеше Лупупа
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 27 ноября 2025
toc: false
slide_level: 2
aspectratio: 169
theme: metropolis
section-titles: true
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цель работы

Приобретение практических навыков по установке, настройке и администрированию СУБД MariaDB.

# Выполнение лабораторной работы

## Установка пакетов

![Установка MariaDB](Screenshot_1.png){ width=70% }

## Установка пакетов

![Конфигурация MariaDB](Screenshot_2.png){ width=70% }

## Скрипт mysql_secure_installation

![Настройка безопасности](Screenshot_2.png){ width=70% }

## Просмотр баз данных

![Список баз данных](Screenshot_3.png){ width=70% }

## Статус MariaDB

![Статус MariaDB](Screenshot_4.png){ width=70% }

## Создание файла utf8.cnf

![utf8.cnf](Screenshot_5.png){ width=70% }

## Проверка изменений

![Проверка кодировки](Screenshot_6.png){ width=70% }

## Создание таблицы и данных

![Таблица city](Screenshot_7.png){ width=70% }

## Создание пользователя

![Создание пользователя](Screenshot_8.png){ width=70% }

## Создание каталога

![Каталог backup](Screenshot_10.png){ width=70% }

# Вывод

MariaDB была успешно установлена и настроена, создана база данных addressbook, выполнено управление пользователями и привилегиями, разработаны резервные копии и проверено восстановление. Конфигурации интегрированы в Vagrant, что обеспечивает автоматизированное развертывание окружения.
