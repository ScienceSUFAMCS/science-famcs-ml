---
code: hw09.depth_matched
hw: hw09
title: Глубина не задана явно
severity: major
detector: rule
---
**Что не так.** Не указан `max_depth`.

**Почему это важно.** Задание требовало сравнить лес и дерево *одинаковой глубины*. Без явного `max_depth` сравнение некорректно: деревья вырастут разными.

**Почитать:**
- [Задание HW09](rubrics/tasks/hw09.md)
- [Ансамбли в машинном обучении](https://education.yandex.ru/handbook/ml/article/ansambli-v-mashinnom-obuchenii)
