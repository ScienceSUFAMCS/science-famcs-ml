---
code: hw01.seed
hw: hw01
title: Не зафиксирован seed в бонусной части
severity: minor
detector: rule
---
**Что не так.** Случайная генерация без `seed`.

**Почему это важно.** При каждом запуске получаются другие числа, и текст
выводов перестаёт соответствовать таблицам в ноутбуке.

**Как надо.** `rng = np.random.default_rng(42)` и дальше только через `rng`.

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [Яндекс.Хендбук — первые шаги](https://education.yandex.ru/handbook/ml/article/pervie-shagi)
