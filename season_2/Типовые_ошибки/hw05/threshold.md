---
code: hw05.threshold
hw: hw05
title: Нет эксперимента с порогом классификации
severity: major
detector: rule
---
**Что не так.** Не показано, как меняются метрики при пороге 0.3 / 0.5 / 0.7.

**Почему это важно.** Порог 0.5 — произвольное соглашение, а не свойство модели.
Понижая порог, вы ловите больше положительных объектов (растёт recall) ценой
ложных срабатываний (падает precision). В реальных задачах порог выбирают
из цены ошибки, а не по умолчанию.

**Как надо.**

```python
for thr in [0.3, 0.5, 0.7]:
    pred = (proba >= thr).astype(int)
    print(thr, precision_score(y_test, pred).round(3), recall_score(y_test, pred).round(3))
```

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Метрики классификации и регрессии](https://education.yandex.ru/handbook/ml/article/metriki-klassifikacii-i-regressii)
