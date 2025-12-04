---
lang: ru-RU
title: Администрирование сетевых подсистем
subtitle: Лабораторная работа №3
author:
  - Чилеше Лупупа
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 2025
toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цель работы

## Основная цель

Приобретение навыков по установке и конфигурированию DHCP-сервера Kea, а также интеграции его с DNS-сервером Bind9 с поддержкой динамических обновлений (DDNS).

# Выполнение работы

## Резервное копирование конфигурации

![Резервное копирование конфигурации](Screenshot_1.png){ width=70% }

## Изменение конфигурации DHCP

![Редактирование конфигурации Kea](Screenshot_2.png){ width=70% }

## Настройка подсети

![Настройка подсети DHCP](Screenshot_3.png){ width=70% }

## Проверка конфигурации

![Проверка Kea](Screenshot_4.png){ width=70% }

## Настройка прямой DNS-зоны

![Прямая зона](Screenshot_5.png){ width=70% }

## Настройка обратной DNS-зоны

![Обратная зона](Screenshot_6.png){ width=70% }

## Проверка разрешения имён

![Проверка DNS](Screenshot_7.png){ width=70% }

## Настройка firewall и SELinux

![Firewall и SELinux](Screenshot_8.png){ width=70% }

## Скрипт маршрутизации клиента

![Скрипт маршрутизации](Screenshot_9.png){ width=70% }

## Интерфейсы клиента

![Интерфейсы клиента](Screenshot_10.png){ width=70% }

## Анализ DHCP-аренд

![kea-leases4.csv](Screenshot_11.png){ width=70% }

## Генерация TSIG-ключа

![TSIG-ключ](Screenshot_12.png){ width=70% }

## Подключение ключа в named

![Вставка ключа](Screenshot_13.png){ width=70% }

## Настройка политики обновлений прямой зоны

![update-policy FZ](Screenshot_14.png){ width=70% }

## Настройка политики обновлений обратной зоны

![update-policy RZ](Screenshot_15.png){ width=70% }

## Конфигурация tsig-keys.json

![tsig-keys.json](Screenshot_16.png){ width=70% }

## Конфигурация Kea DHCP-DDNS

![kea-dhcp-ddns.conf](Screenshot_17.png){ width=70% }

## Статус Kea DDNS

![Kea DDNS status](Screenshot_18.png){ width=70% }

## Обновления DDNS в DHCP

![dhcp4 DDNS параметры](Screenshot_19.png){ width=70% }

## Проверка DDNS через dig

![dig результат](Screenshot_21.png){ width=70% }

## Завершение настройки

![dhcp.sh](Screenshot_22.png){ width=70% }

# Итоги работы

## Вывод

Настроен DHCP-сервер Kea, интегрированный с Bind9 через TSIG-ключи. Динамические обновления DNS функционируют корректно: клиенты автоматически получают IP-адреса, а соответствующие A- и PTR-записи создаются в DNS-зонах. Инфраструктура полностью автоматизирована и прошла успешное тестирование.

