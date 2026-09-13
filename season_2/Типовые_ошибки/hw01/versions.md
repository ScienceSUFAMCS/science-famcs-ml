---
code: hw01.versions
hw: hw01
title: Не выведены версии окружения
severity: major
detector: rule
---
**Что не так.** В ноутбуке нет вывода версий Python, NumPy, Pandas и scikit-learn.

**Почему это важно.** Это первый пункт задания и полезная привычка: половина
«странных» ошибок в ML объясняется другой версией библиотеки. Зафиксированное
окружение — часть воспроизводимости эксперимента.

**Как надо.**

```python
import sys, numpy as np, pandas as pd, sklearn
print(sys.version)
print("numpy", np.__version__, "| pandas", pd.__version__, "| sklearn", sklearn.__version__)
```

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [Документация Jupyter](https://docs.jupyter.org/en/latest/)
