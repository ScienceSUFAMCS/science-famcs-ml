---
code: hw03.baselines
hw: hw03
title: Нет сравнения с базовыми моделями
severity: major
detector: rule
---
**Что не так.** Обучен только KNN, сравнить его не с чем.

**Почему это важно.** Это самая частая недоработка в этой домашке на потоке.
Метрика сама по себе ничего не значит: accuracy 0.85 звучит хорошо, пока
не выяснится, что константное предсказание самого частого класса даёт 0.84.
Без бейзлайна нельзя утверждать, что модель вообще чему-то научилась, — а
задание прямо просило понять, когда KNN хорош, а когда уступает.

**Как надо.** Минимум — константный бейзлайн, дальше пара обычных моделей:

```python
from sklearn.dummy import DummyClassifier
models = {
    "most_frequent": DummyClassifier(strategy="most_frequent"),
    "logreg": LogisticRegression(max_iter=1000),
    "tree": DecisionTreeClassifier(random_state=42),
    "knn": KNeighborsClassifier(n_neighbors=best_k),
}
for name, m in models.items():
    print(name, cross_val_score(m, X_train_s, y_train, cv=5).mean().round(3))
```

**Почитать:**
- [Задание HW03](rubrics/tasks/hw03.md)
- [Метрические методы](https://education.yandex.ru/handbook/ml/article/metricheskiye-metody)
- [Метрики классификации и регрессии](https://education.yandex.ru/handbook/ml/article/metriki-klassifikacii-i-regressii)
