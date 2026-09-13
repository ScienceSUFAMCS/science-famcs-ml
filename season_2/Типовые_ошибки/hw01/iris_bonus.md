---
code: hw01.iris_bonus
hw: hw01
title: Не сделана бонусная часть с Iris
severity: minor
detector: rule
---
**Что не так.** Не выполнена бонусная часть: загрузить `load_iris`, собрать
DataFrame, обучить простую модель и посчитать accuracy.

**Почему это важно.** Это первый полный ML-пайплайн в миниатюре: данные → модель
→ метрика. Дальше весь курс — надстройки над этой схемой.

**Как надо.**

```python
from sklearn.datasets import load_iris
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

data = load_iris(as_frame=True)
X_train, X_test, y_train, y_test = train_test_split(
    data.data, data.target, test_size=0.2, random_state=42, stratify=data.target)
clf = LogisticRegression(max_iter=1000).fit(X_train, y_train)
print(accuracy_score(y_test, clf.predict(X_test)))
```

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
