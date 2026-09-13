---
code: common.no_effect_call
hw: common
title: Вызов не меняет данные и результат не сохраняется
severity: major
detector: rule
kind: hygiene
---
**Что не так.** Строка вида `df.dropna(subset=[...])` или
`df.drop_duplicates()` стоит сама по себе: результат никуда не присваивается,
а `inplace` не указан.

**Почему это важно.** Методы pandas по умолчанию возвращают **новый**
датафрейм, а исходный не трогают. Такая строка выполняется, ничего не ломает и
не делает ровно ничего — а дальше по ноутбуку вы работаете с неочищенными
данными, будучи уверены, что очистили их.

**Как надо.** Присваивать результат:

```python
df = df.dropna(subset=["age", "sex"])
df = df.drop_duplicates()
```

`inplace=True` формально тоже работает, но его не рекомендуют: он мешает
цепочкам и в новых версиях pandas ведёт себя непоследовательно.

**Почитать:**
- [Как сдаются домашки на курсе](rubrics/tasks/hw01.md)
- [pandas: почему inplace не нужен](https://pandas.pydata.org/docs/whatsnew/v2.0.0.html#copy-on-write-improvements)
