---
code: hw10.importances
hw: hw10
title: Нет свойства feature_importances_
severity: major
detector: rule
---
**Что не так.** Не реализовано свойство `feature_importances_`.

**Почему это важно.** Пункт задания, и он проще, чем кажется: внутри уже
используются `DecisionTreeRegressor`, у каждого из них важности есть — надо
усреднить их по всем деревьям ансамбля с учётом learning rate.

**Почитать:**
- [Задание HW10](rubrics/tasks/hw10.md)
- [Градиентный бустинг](https://education.yandex.ru/handbook/ml/article/gradientnyj-busting)
