---
code: hw10.categorical
hw: hw10
title: Нет поддержки категориальных признаков
severity: minor
detector: rule
---
**Что не так.** Не добавлена нативная работа с категориями.

**Почему это важно.** Необязательный пункт. Полезно понимать, как это решает CatBoost: упорядоченным target statistics, который считает среднее таргета по категории только на «прошлых» объектах и потому не протекает.

**Почитать:**
- [Задание HW10](rubrics/tasks/hw10.md)
- [Градиентный бустинг](https://education.yandex.ru/handbook/ml/article/gradientnyj-busting)
