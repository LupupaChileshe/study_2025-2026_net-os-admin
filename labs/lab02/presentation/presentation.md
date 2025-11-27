---
## Front matter
lang: ru-RU
title: Администрирование сетевых подсистем
subtitle: Лабораторная работа №2
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

Приобретение практических навыков по установке, конфигурированию и тестированию DNS-сервера на базе BIND.

# Выполнение лабораторной работы

## Первичная проверка DNS-разрешения

![Результат dig www.yandex.ru](Screenshot_1.png){ width=70% }

## Проверка локального DNS-сервера

![Запрос dig через 127.0.0.1](Screenshot_2.png){ width=70% }

## Назначение локального DNS в NetworkManager

![Настройка DNS в NM](Screenshot_3.png){ width=70% }

## Настройка файла named.conf

![named.conf](Screenshot_4.png){ width=70% }

## Проверка активности порта DNS

![lsof | grep domain](Screenshot_5.png){ width=70% }

## Подключение пользовательских зон

![Файл зон chileshe.net](Screenshot_6.png){ width=70% }

## Настройка прямой зоны

![Прямая зона](Screenshot_7.png){ width=70% }

## Настройка обратной зоны

![Обратная зона](Screenshot_8.png){ width=70% }

## Настройка прав и SELinux

![SELinux и права](Screenshot_9.png){ width=70% }

## Проверка прямой зоны dig

![Проверка A-записи](Screenshot_10.png){ width=70% }

## Проверка прямой и обратной зоны host

![Проверка host](Screenshot_11.png){ width=70% }

## Подготовка provisioning-каталогов

![Каталоги provisioning](Screenshot_12.png){ width=70% }

## Скрипт автоматизации dns.sh

![dns.sh](Screenshot_13.png){ width=70% }

# Выводы

## Итог

В ходе работы был установлен и настроен DNS-сервер BIND, создана прямая и обратная зоны, настроены конфигурационные файлы и параметры SELinux, проведена проверка корректности работы с помощью dig и host. Создан provisioning-скрипт для автоматизации развертывания DNS-сервера в Vagrant. Все этапы выполнены успешно.
