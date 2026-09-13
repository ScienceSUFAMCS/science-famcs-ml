---
code: hw10.libraries
hw: hw10
title: Сравнены не все три библиотеки
severity: major
detector: rule
---
**Что не так.** Использованы не все из XGBoost, LightGBM и CatBoost.

**Почему это важно.** Задание про различия реализаций: LightGBM растит деревья по листьям и быстрее на больших данных, CatBoost умеет категории «из коробки» и устойчивее к переобучению на малых выборках, XGBoost — классика с самой предсказуемой настройкой.

**Почитать:**
- [Задание HW10](rubrics/tasks/hw10.md)
- [Градиентный бустинг](https://education.yandex.ru/handbook/ml/article/gradientnyj-busting)
