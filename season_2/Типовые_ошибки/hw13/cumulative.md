---
code: hw13.cumulative
hw: hw13
title: Нет накопленной доли дисперсии
severity: major
detector: rule
---
**Что не так.** Не построен график накопленной объяснённой дисперсии.

**Почему это важно.** Стандартный способ выбрать число компонент: взять
столько, чтобы покрыть 90–95% дисперсии.

**Как надо.**

```python
plt.plot(np.cumsum(pca.explained_variance_ratio_))
plt.axhline(0.95, ls="--")
```

**Почитать:**
- [sklearn: PCA](https://scikit-learn.org/stable/modules/decomposition.html#pca)
- [Слайды лекции по снижению размерности](materials/pca_slides.pdf)
