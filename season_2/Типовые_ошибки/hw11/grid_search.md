---
code: hw11.grid_search
hw: hw11
title: Нет Grid Search
severity: major
detector: rule
---
**Что не так.** Не использован `GridSearchCV`.

**Почему это важно.** Полный перебор по сетке — базовый метод: он гарантированно найдёт лучшую комбинацию из заданных, но число вариантов растёт как произведение размеров сетки.

**Почитать:**
- [Подбор гиперпараметров](https://education.yandex.ru/handbook/ml/article/podbor-giperparametrov)
