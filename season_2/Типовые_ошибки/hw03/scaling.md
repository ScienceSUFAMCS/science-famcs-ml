---
code: hw03.scaling
hw: hw03
title: Нет масштабирования признаков
severity: major
detector: rule
---
**Что не так.** Признаки не приведены к одному масштабу.

**Почему это важно.** Для KNN это не мелочь, а определяющий фактор. Метод
считает расстояния, и признак с диапазоном 0–100000 (пробег) полностью
заглушит признак с диапазоном 0–1. Фактически модель будет смотреть только на
самый «крупный» столбец.

**Как надо.**

```python
scaler = StandardScaler()
X_train_s = scaler.fit_transform(X_train)
X_test_s  = scaler.transform(X_test)
```

Обязательно покажите метрики до и после масштабирования — разница
обычно впечатляет.

**Почитать:**
- [Задание HW03](rubrics/tasks/hw03.md)
- [Метрические методы](https://education.yandex.ru/handbook/ml/article/metricheskiye-metody)
