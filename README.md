# Специалист по Data Science

## Разработка модели ML для предсказания продолжения деятельности стартапа

## Стоящая задача

- Разработать модель машинного обучения для предсказания продолжения деятельности стартапа.
- Провести полноценный разведочный анализ и сформировать рекомендации будущим создателям стартапов (какие факторы влияют на успешность стартапа).

## инструменты и библиотеки, которые использовали в проекте

В проекте использовались следующие инструменты и библиотеки Python обеспечивают широкий спектр функциональности для работы с данными, от предварительной обработки до построения и оценки моделей машинного обучения. :

- os: Библиотека для взаимодействия с операционной системой, включая работу с файловой системой.
- matplotlib.pyplot & seaborn: Библиотеки для визуализации данных, позволяющие создавать статистические графики.
- missingno: Инструмент для визуализации отсутствующих данных в датафреймах.
- pandas: Мощная библиотека для анализа и манипуляции данными.
- numpy: Основная библиотека для научных вычислений в Python.
- shap: Библиотека для объяснения прогнозов моделей машинного обучения.
- phik: Библиотека для вычисления корреляции между переменными.
- Из sklearn (Scikit-learn) использовались:
  - Pipeline & ColumnTransformer: Классы для создания конвейеров обработки данных.
  - OneHotEncoder, StandardScaler, MinMaxScaler: Инструменты для предварительной обработки данных, такие как кодирование категорий и масштабирование.
  - train_test_split & RandomizedSearchCV: Функции для разделения данных на обучающие и тестовые наборы и для оптимизации гиперпараметров моделей.
  - LogisticRegression & DecisionTreeClassifier: Модели для классификации данных.
  - f1_score & confusion_matrix: Метрики для оценки качества моделей.
  - GradientBoostingClassifier & HistGradientBoostingClassifier: Ансамблевые модели для повышения точности прогнозирования.
  - DummyClassifier: Простая модель для сравнения производительности.
  - CatBoostClassifier: Модель градиентного бустинга, оптимизированная для категориальных данных.

**Выводы**
Была проведена работа по разработке модели для предсказания деятености стратапа, выбрана лучшая модель по метрике **F1**, лучшей моделью оказалсь модель `CatBoostClassifier`, ее лучшие параметры модели:

- `preprocessor__num: MinMaxScaler()`,
- `models__learning_rate: 0.3`,
- `models__iterations: 100`,
- `models__depth: 5`;

Метрика лучшей модели на тренировочной выборке: **0.988**

Даны рекомендации бизнесу
