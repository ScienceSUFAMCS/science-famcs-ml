---
code: hw05.roc
hw: hw05
title: Нет confusion matrix или ROC-кривой
severity: major
detector: rule
---
**Что не так.** Отсутствует матрица ошибок и/или ROC-кривая с AUC.

**Почему это важно.** Матрица ошибок показывает, какие именно ошибки делает
модель — путает ли она классы симметрично. ROC-AUC оценивает качество
ранжирования и не зависит от выбора порога, поэтому им удобно сравнивать модели.

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Метрики классификации и регрессии](https://education.yandex.ru/handbook/ml/article/metriki-klassifikacii-i-regressii)
