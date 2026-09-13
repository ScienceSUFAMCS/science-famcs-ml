---
code: hw09.importances
hw: hw09
title: Не показана важность признаков
severity: minor
detector: rule
---
**Что не так.** Не выведен `feature_importances_`.

**Почему это важно.** Это почти бесплатный побочный продукт леса и хороший
способ проверить себя. Стоит помнить об искажении: встроенная важность
завышает вклад признаков с большим числом уникальных значений, поэтому
надёжнее permutation importance.

**Почитать:**
- [Задание HW09](rubrics/tasks/hw09.md)
- [Ансамбли в машинном обучении](https://education.yandex.ru/handbook/ml/article/ansambli-v-mashinnom-obuchenii)
