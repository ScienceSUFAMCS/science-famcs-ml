---
code: hw06.compare_sklearn
hw: hw06
title: Нет сравнения с GaussianNB из sklearn
severity: major
detector: rule
---
**Что не так.** Не обучен `GaussianNB`.

**Почему это важно.** Совпадение метрик — доказательство того, что ваша реализация верна. Расхождение указывает на ошибку в формулах.

**Почитать:**
- [Генеративный подход к классификации](https://education.yandex.ru/handbook/ml/article/generativnyj-podhod-k-klassifikacii)
- [Как оценивать вероятности](https://education.yandex.ru/handbook/ml/article/kak-ocenivat-veroyatnosti)
