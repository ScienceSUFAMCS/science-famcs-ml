---
code: hw11.random_search
hw: hw11
title: Нет Random Search
severity: major
detector: rule
---
**Что не так.** Не использован `RandomizedSearchCV`.

**Почему это важно.** Задание сравнивало стратегии. Случайный поиск при том же
бюджете обычно выигрывает у сетки: если из пяти гиперпараметров реально важны
два, сетка тратит попытки на перебор незначимых, а случайный поиск покрывает
важные оси гораздо плотнее.

**Почитать:**
- [Подбор гиперпараметров](https://education.yandex.ru/handbook/ml/article/podbor-giperparametrov)
