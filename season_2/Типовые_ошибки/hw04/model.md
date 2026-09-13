---
code: hw04.model
hw: hw04
title: Не обучена линейная модель
severity: major
detector: rule
---
**Что не так.** В работе нет ни `LinearRegression`, ни `Ridge`/`Lasso`.

**Почему это важно.** Это тема домашки.

**Как надо.** `LinearRegression().fit(X_train, y_train)` и дальше сравнение
с регуляризованными вариантами.

**Почитать:**
- [Задание HW04](rubrics/tasks/hw04.md)
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
