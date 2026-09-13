---
code: common.show_without_call
hw: common
title: plt.show написан без скобок
severity: major
detector: rule
kind: hygiene
---
**Что не так.** В коде стоит `plt.show` вместо `plt.show()`.

**Почему это важно.** Без скобок это не вызов функции, а ссылка на неё: в вывод
ячейки падает строка вида `<function matplotlib.pyplot.show>`. В Jupyter график
всё равно рисуется — но только благодаря inline-бэкенду, который выводит фигуры
сам. В обычном скрипте или при другом бэкенде окно не откроется, и вы этого не
заметите, потому что ошибки нет.

**Как надо.**

```python
plt.show()
```

**Почитать:**
- [Как сдаются домашки на курсе](rubrics/tasks/hw01.md)
- [matplotlib: быстрый старт](https://matplotlib.org/stable/users/explain/quick_start.html)
