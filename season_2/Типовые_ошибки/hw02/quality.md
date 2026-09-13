---
code: hw02.quality
hw: hw02
title: Нет проверки пропусков и дубликатов
severity: major
detector: rule
---
**Что не так.** Не посчитаны пропуски и/или полные дубликаты строк.

**Почему это важно.** Дубликаты завышают качество модели: одна и та же строка
может попасть и в train, и в test. Пропуски ломают обучение моделей, которые их
не поддерживают.

**Как надо.**

```python
df.isnull().sum().sort_values(ascending=False)
df.duplicated().sum()
df = df.drop_duplicates()
```

**Почитать:**
- [Задание HW02 (чек-лист EDA)](rubrics/tasks/hw02.md)
- [ODS: первичный анализ данных с Pandas](https://habr.com/ru/companies/ods/articles/322626/)
- [pandas за 10 минут](https://pandas.pydata.org/docs/user_guide/10min.html)
