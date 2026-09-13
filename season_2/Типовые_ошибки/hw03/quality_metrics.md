---
code: hw03.quality_metrics
hw: hw03
title: Нет метрик качества классификации
severity: major
detector: rule
---
**Что не так.** Качество не измерено ни accuracy, ни f1, ни матрицей ошибок.

**Почему это важно.** Без метрики нет результата. При дисбалансе классов
accuracy обманчива, и нужны precision/recall или macro-F1.

**Как надо.**

```python
print(classification_report(y_test, y_pred))
ConfusionMatrixDisplay.from_predictions(y_test, y_pred)
```

**Почитать:**
- [Задание HW03](rubrics/tasks/hw03.md)
- [Метрики классификации и регрессии](https://education.yandex.ru/handbook/ml/article/metriki-klassifikacii-i-regressii)
