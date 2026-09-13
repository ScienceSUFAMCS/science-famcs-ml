---
code: hw07.postpruning
hw: hw07
title: Нет post-pruning через ccp_alpha
severity: major
detector: rule
---
**Что не так.** Не использован `ccp_alpha`.

**Почему это важно.** Post-pruning работает иначе, чем pre-pruning: дерево
строится целиком, а потом обрезаются ветви, дающие слишком малый выигрыш в
чистоте относительно платы за сложность. Это позволяет сохранить полезные
глубокие ветви там, где они действительно нужны.

**Как надо.**

```python
path = DecisionTreeClassifier(random_state=42).cost_complexity_pruning_path(X_train, y_train)
for a in path.ccp_alphas[::5]:
    clf = DecisionTreeClassifier(ccp_alpha=a, random_state=42)
    print(a.round(5), cross_val_score(clf, X_train, y_train, cv=5).mean().round(3))
```

**Почитать:**
- [Решающие деревья](https://education.yandex.ru/handbook/ml/article/reshayushchiye-derevya)
