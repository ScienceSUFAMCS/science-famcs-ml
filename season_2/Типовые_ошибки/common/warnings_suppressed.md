---
code: common.warnings_suppressed
hw: common
title: Предупреждения отключены глобально
severity: minor
detector: rule
kind: hygiene
---
**Что не так.** В начале ноутбука стоит `warnings.filterwarnings('ignore')`.

**Почему это важно.** Заглушаются не только косметические `FutureWarning`, но и
сообщения, которые прямо указывают на ошибку: цепочечное присваивание в pandas
(изменения молча теряются), несходимость модели (`ConvergenceWarning` у
логистической регрессии — сигнал, что не хватило итераций или нет
масштабирования), деление на ноль в numpy.

**Как надо.** Прочитать предупреждения и починить причину. Если какое-то
действительно мешает и разобрано — глушить точечно:

```python
warnings.filterwarnings("ignore", category=FutureWarning, module="seaborn")
```

**Почитать:**
- [Как сдаются домашки на курсе](rubrics/tasks/hw01.md)
- [pandas за 10 минут](https://pandas.pydata.org/docs/user_guide/10min.html)
