---
lang: ru-RU
title: Администрирование сетевых подсистем
subtitle: Лабораторная работа №4
author:
  - Чилеше Лупупа
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 22 ноября 2025
aspectratio: 169
theme: metropolis
section-titles: true
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цель работы

## Основная цель

Приобретение навыков установки и базовой настройки HTTP-сервера Apache, включая конфигурирование виртуального хостинга и обновление DNS-зон.

# Установка и базовая настройка Apache

## Установка веб-сервера

![Конфигурационные каталоги](Screenshot_1.png){ width=70% }

## Разрешение HTTP-трафика

![firewalld](Screenshot_2.png){ width=70% }

## Проверка на клиентской машине

![Тестовая страница](Screenshot_3.png){ width=70% }

## Просмотр логов

![Логи](Screenshot_4.png){ width=70% }

## Добавление DNS-записей

![DNS-прямая](Screenshot_5.png){ width=70% }

## Добавление DNS-записей

![DNS-обратная](Screenshot_6.png){ width=70% }

## Создание конфигураций виртуальных хостов

![server.chileshe.net.conf](Screenshot_7.png){ width=70% }

## Создание конфигураций виртуальных хостов

![www.chileshe.net.conf](Screenshot_8.png){ width=70% }

## Создание каталогов и страниц

![Каталоги](Screenshot_9.png){ width=70% }

## Доступ к сайтам
![server.chileshe.net](Screenshot_10.png){ width=70% }

## Доступ к сайтам
![www.chileshe.net](Screenshot_11.png){ width=70% }

# Вывод

Настроен web-сервер Apache с виртуальным хостингом и обновлёнными зонами DNS. Проверка с клиентской машины подтвердила корректную работу обоих сайтов. Все компоненты — Apache, DNS и веб-контент — функционируют согласованно и обеспечивают стабильную работу веб-службы.
