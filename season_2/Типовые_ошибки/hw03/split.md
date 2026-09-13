---
code: hw03.split
hw: hw03
title: Нет разделения на train и test
severity: major
detector: rule
---
**Что не так.** Не вызван `train_test_split` или иной способ отложить тест.

**Почему это важно.** Без отложенной выборки нельзя сказать ничего о качестве:
KNN на обучающей выборке при `k=1` даёт идеальную точность просто потому, что
ближайший сосед любого объекта — он сам.

**Как надо.**

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y)
```

`stratify=y` сохраняет доли классов — важно при дисбалансе.

**Почитать:**
- [Задание HW03](rubrics/tasks/hw03.md)
- [Кросс-валидация](https://education.yandex.ru/handbook/ml/article/kross-validaciya)
