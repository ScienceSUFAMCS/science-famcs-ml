---
code: common.absolute_path
hw: common
title: Абсолютный путь к данным
severity: major
detector: rule
kind: hygiene
---
**Что не так.** Датасет загружается по абсолютному пути — `/train.csv`,
`C:\Users\...\data.csv` или `/content/...` из Google Colab.

**Почему это важно.** У проверяющего такого пути нет, и ноутбук падает на
первой же ячейке с `FileNotFoundError`. Воспроизводимость — часть работы:
результат, который не запускается ни у кого, кроме автора, ценности не имеет.

**Как надо.** Класть данные рядом с ноутбуком и обращаться относительным путём,
а лучше — скачивать кодом, чтобы файл вообще не нужно было коммитить:

```python
df = pd.read_csv("data/train.csv")          # файл лежит в репозитории рядом

# или через kagglehub — тогда данные не нужно хранить в git
import kagglehub
path = kagglehub.dataset_download("shwetabh123/mall-customers")
df = pd.read_csv(f"{path}/Mall_Customers.csv")
```

**Почитать:**
- [Как сдаются домашки на курсе](rubrics/tasks/hw01.md)
- [Документация Jupyter](https://docs.jupyter.org/en/latest/)
