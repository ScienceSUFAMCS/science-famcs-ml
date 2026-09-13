---
code: hw04.split
hw: hw04
title: Нет разделения выборки
severity: major
detector: rule
---
**Что не так.** Нет ни `train_test_split`, ни кросс-валидации.

**Почему это важно.** R² на обучающей выборке всегда оптимистичен и растёт от
добавления любого признака, даже случайного. Оценивать качество можно только
на данных, которых модель не видела.

**Почитать:**
- [Задание HW04](rubrics/tasks/hw04.md)
- [Кросс-валидация](https://education.yandex.ru/handbook/ml/article/kross-validaciya)
