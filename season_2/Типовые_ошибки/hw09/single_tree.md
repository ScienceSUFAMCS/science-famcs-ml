---
code: hw09.single_tree
hw: hw09
title: Нет одиночного дерева для сравнения
severity: major
detector: rule
---
**Что не так.** Не обучено отдельное дерево той же глубины.

**Почему это важно.** Это ядро задания. Сравнение показывает, что даёт именно
ансамблирование: одиночное глубокое дерево имеет низкое смещение и высокую
дисперсию, а усреднение множества декоррелированных деревьев дисперсию гасит,
почти не трогая смещение.

**Почитать:**
- [Задание HW09](rubrics/tasks/hw09.md)
- [Ансамбли в машинном обучении](https://education.yandex.ru/handbook/ml/article/ansambli-v-mashinnom-obuchenii)
- [Bias-variance decomposition](https://education.yandex.ru/handbook/ml/article/bias-variance-decomposition)
