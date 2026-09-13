# Типовые ошибки

*Второй сезон · весна 2026*

Разборы, собранные по итогам проверки **929 работ**: что именно пошло не так,
почему это важно и как надо. Общие ошибки не привязаны к теме и встречаются
в любой работе; остальные — по темам.

## Общие

- [plt.show написан без скобок](common/show_without_call.md)
- [Абсолютный путь к данным](common/absolute_path.md)
- [В ноутбуке нет заполненного кода](common/nothing_done.md)
- [В репозитории лежит ключ доступа](common/secret_in_repo.md)
- [Весь текст в работе — из шаблона](common/no_own_conclusions.md)
- [Выводы написаны комментариями в ячейке кода](common/conclusions_in_code_comments.md)
- [Выводы расходятся с результатами в ноутбуке](common/text_contradicts_output.md)
- [Вызов не меняет данные и результат не сохраняется](common/no_effect_call.md)
- [Не зафиксирован seed](common/no_seed.md)
- [Нет текстовых выводов](common/no_conclusions.md)
- [Ноутбук не выполняется сверху вниз](common/execution_out_of_order.md)
- [Ноутбук не запустится с нуля: имя нигде не определено](common/undefined_name.md)
- [Ноутбук не открывается](common/notebook_unreadable.md)
- [Ноутбук падает с ошибкой](common/error_output.md)
- [Ноутбук сохранён без запуска](common/not_executed.md)
- [Остались незаполненные ячейки задания](common/blank_template_cells.md)
- [Попытка обмануть автоматическую проверку](common/prompt_injection_attempt.md)
- [Предупреждения отключены глобально](common/warnings_suppressed.md)
- [Преобразование обучено до разделения выборки](common/fit_before_split.md)
- [Преобразование обучено на тестовой выборке](common/fit_on_test.md)
- [Разбиение выборки не зафиксировано](common/split_without_seed.md)
- [Часть ячеек не выполнена](common/partially_executed.md)

## hw01

- [Не выведены версии окружения](hw01/versions.md)
- [Не зафиксирован seed в бонусной части](hw01/seed.md)
- [Не сделана бонусная часть с Iris](hw01/iris_bonus.md)
- [Нет DataFrame с базовым обзором](hw01/dataframe.md)
- [Нет векторизованного умножения](hw01/vectorization.md)
- [Нет гистограммы или тепловой карты корреляций](hw01/plots.md)
- [Нет осмысленных операций pandas](hw01/pandas_ops.md)
- [Нет случайной матрицы и статистик по осям](hw01/numpy_matrix.md)

## hw02

- [Выбор заполнения пропусков не обоснован](hw02/justified_imputation.md)
- [Использованы не все три библиотеки визуализации](hw02/three_libs.md)
- [Мало итоговых выводов](hw02/conclusions.md)
- [Не посчитаны перцентили](hw02/quantiles.md)
- [Не созданы новые признаки](hw02/feature_engineering.md)
- [Не хватает обязательных типов графиков](hw02/plot_kinds.md)
- [Нет describe для строковых колонок](hw02/describe_object.md)
- [Нет блока про использование AI](hw02/ai_block.md)
- [Нет быстрого обзора данных](hw02/overview.md)
- [Нет гипотез и наблюдений](hw02/hypotheses.md)
- [Нет дисперсии, асимметрии и эксцесса](hw02/skew_kurt.md)
- [Нет кодирования категориальных признаков](hw02/encoding.md)
- [Нет проверки пропусков и дубликатов](hw02/quality.md)
- [Нет ссылки на датасет](hw02/dataset_link.md)
- [Показана только одна стратегия работы с пропусками](hw02/missing_strategies.md)
- [Пропуски в категориях не заполнены модой](hw02/mode_fill.md)

## hw03

- [Не видно загрузки датасета для классификации](hw03/dataset_classification.md)
- [Не сравнивались метрики расстояния](hw03/metrics_compare.md)
- [Нет вывода о влиянии масштабирования](hw03/scaling_conclusion.md)
- [Нет вывода, когда KNN хорош, а когда уступает](hw03/when_knn_good.md)
- [Нет масштабирования признаков](hw03/scaling.md)
- [Нет метрик качества классификации](hw03/quality_metrics.md)
- [Нет подбора числа соседей](hw03/k_search.md)
- [Нет разделения на train и test](hw03/split.md)
- [Нет сравнения с базовыми моделями](hw03/baselines.md)

## hw04

- [Выбор метрик не обоснован](hw04/metric_choice_justified.md)
- [Не обучена линейная модель](hw04/model.md)
- [Не хватает метрик регрессии](hw04/metrics.md)
- [Нет базового решения для сравнения](hw04/baseline.md)
- [Нет предварительного анализа данных](hw04/eda.md)
- [Нет работы с признаками](hw04/feature_engineering.md)
- [Нет разделения выборки](hw04/split.md)
- [Нет регуляризации](hw04/regularization.md)
- [Признаки не масштабированы](hw04/scaling.md)
- [Работа не читается как исследование](hw04/reads_as_research.md)

## hw05

- [Модель не собрана в класс](hw05/model_class.md)
- [Не реализован log-loss](hw05/log_loss.md)
- [Не реализован шаг градиентного спуска](hw05/gradient_step.md)
- [Не реализована сигмоида](hw05/sigmoid.md)
- [Не сделан шаг 1: разделение и стандартизация](hw05/split_scale.md)
- [Нет confusion matrix или ROC-кривой](hw05/roc.md)
- [Нет метрик качества своей модели](hw05/metrics.md)
- [Нет ответов на финальные вопросы](hw05/final_questions.md)
- [Нет сравнения со scikit-learn](hw05/compare_sklearn.md)
- [Нет эксперимента с порогом классификации](hw05/threshold.md)
- [Реализация численно неустойчива](hw05/numerically_stable.md)

## hw06

- [Вычисления не в логарифмах](hw06/log_space.md)
- [Классификатор не собран в класс](hw06/model_class.md)
- [Не оценены параметры распределений по классам](hw06/params.md)
- [Не проверено допущение о независимости признаков](hw06/independence.md)
- [Не реализован log-likelihood](hw06/loglik.md)
- [Не реализована оценка априорных вероятностей](hw06/priors.md)
- [Нет метрик и матрицы ошибок](hw06/metrics.md)
- [Нет ответов на финальные вопросы](hw06/final_questions.md)
- [Нет разделения данных](hw06/split.md)
- [Нет сравнения с GaussianNB из sklearn](hw06/compare_sklearn.md)

## hw07

- [Не обучено дерево решений](hw07/base_tree.md)
- [Не показана неустойчивость дерева](hw07/instability.md)
- [Нет post-pruning через ccp_alpha](hw07/postpruning.md)
- [Нет pre-pruning](hw07/prepruning.md)
- [Нет интерпретации структуры дерева](hw07/interpretation.md)
- [Нет поиска по сетке гиперпараметров](hw07/grid.md)
- [Нет работы с пропусками](hw07/missing.md)
- [Структура дерева не визуализирована](hw07/visualize.md)

## hw08

- [Масштабирование не через Pipeline](hw08/pipeline.md)
- [Не подобраны C и gamma](hw08/grid.md)
- [Не показан SVM без масштабирования](hw08/no_scaling_demo.md)
- [Не построена граница решений](hw08/boundary.md)
- [Нет confusion matrix](hw08/confusion.md)
- [Нет анализа ошибок](hw08/error_analysis.md)
- [Нет ответов на финальные вопросы](hw08/final_questions.md)
- [Нет разделения данных](hw08/split.md)
- [Нет сравнения линейного ядра и RBF](hw08/linear_vs_rbf.md)

## hw09

- [Глубина не задана явно](hw09/depth_matched.md)
- [Не обучен случайный лес](hw09/forest.md)
- [Не показана важность признаков](hw09/importances.md)
- [Не показана подготовка данных](hw09/preprocessing.md)
- [Не сравнивалась скорость обучения](hw09/speed.md)
- [Не хватает метрик регрессии](hw09/metrics.md)
- [Нет вывода о сравнении моделей](hw09/comparison_conclusion.md)
- [Нет кросс-валидации](hw09/cv.md)
- [Нет одиночного дерева для сравнения](hw09/single_tree.md)
- [Нет ответов про разбиение выборки](hw09/split_questions.md)

## hw10

- [Не добавлен параметр colsample_bytree](hw10/colsample.md)
- [Не добавлен параметр subsample](hw10/subsample.md)
- [Нет поддержки категориальных признаков](hw10/categorical.md)
- [Нет свойства feature_importances_](hw10/importances.md)
- [Нет собственной реализации бустинга](hw10/own_boosting.md)
- [Своя реализация заметно хуже библиотечной](hw10/quality_gap.md)
- [Своя реализация не сравнена с библиотечной](hw10/comparison.md)
- [Сравнены не все три библиотеки](hw10/libraries.md)

## hw11

- [Важности показаны, но не прочитаны](hw11/reads_importances.md)
- [Гиперпараметры подобраны по тесту](hw11/cv_correct.md)
- [Не сделан бонус с Optuna](hw11/optuna.md)
- [Нет Grid Search](hw11/grid_search.md)
- [Нет PDP и ICE-кривых](hw11/pdp.md)
- [Нет Permutation Importance](hw11/permutation.md)
- [Нет Random Search](hw11/random_search.md)
- [Нет SHAP](hw11/shap.md)
- [Нет базовых моделей без тюнинга](hw11/baselines.md)
- [Нет диагностики подозрительных признаков](hw11/leak_diagnostics.md)
- [Нет сводной таблицы и итогов](hw11/summary.md)

## hw12

- [DBSCAN не применён](hw12/dbscan.md)
- [Не разобрана работа с шумом](hw12/noise.md)
- [Не разобрано влияние eps и min_samples](hw12/params.md)
- [Нет масштабирования перед кластеризацией](hw12/scaling.md)
- [Нет ответов на вопросы для размышления](hw12/reflection_answers.md)
- [Нет подбора eps через k-distance plot](hw12/k_distance.md)
- [Нет силуэта](hw12/silhouette.md)
- [Нет сравнения с K-Means](hw12/kmeans_compare.md)

## hw13

- [PCA не использован как препроцессинг](hw13/downstream.md)
- [PCA не применён](hw13/pca.md)
- [Не применён UMAP](hw13/umap.md)
- [Не применён t-SNE](hw13/tsne.md)
- [Нет выводов о структуре данных в проекциях](hw13/conclusions.md)
- [Нет интерпретации компонент](hw13/loadings.md)
- [Нет накопленной доли дисперсии](hw13/cumulative.md)
- [Нет объяснённой дисперсии](hw13/explained_variance.md)
- [Нет стандартизации перед PCA](hw13/scaling.md)
