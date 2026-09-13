---
code: hw06.priors
hw: hw06
title: Не реализована оценка априорных вероятностей
severity: major
detector: rule
---
**Что не так.** Нет функции `compute_priors`.

**Почему это важно.** Априорная вероятность класса P(y) — половина формулы Байеса.
При сильном дисбалансе именно она определяет предсказание, когда правдоподобия
близки.

**Как надо.** `priors[c] = (y == c).sum() / len(y)`.

**Почитать:**
- [Генеративный подход к классификации](https://education.yandex.ru/handbook/ml/article/generativnyj-podhod-k-klassifikacii)
- [Как оценивать вероятности](https://education.yandex.ru/handbook/ml/article/kak-ocenivat-veroyatnosti)
