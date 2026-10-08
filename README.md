# NYC Taxi Trip Duration Prediction

ML-проект по предсказанию длительности поездок на жёлтом такси в Нью-Йорке.

## 🎯 Задача
Регрессия: предсказать `trip_duration` (в секундах).

## 📊 Данные
- [Kaggle NYC Taxi Trip Duration](https://www.kaggle.com/c/nyc-taxi-trip-duration)
- OSRM (маршруты), погода NYC 2016, праздники США

⚠️ CSV-файлы не включены в репозиторий.

## 🛠 Стек
Python, pandas, numpy, scikit-learn, matplotlib, seaborn, plotly, scipy

## 📈 Результаты

| Модель | RMSLE (valid) |
|---|---|
| LinearRegression | 0.51 |
| DecisionTree (depth=11) | 0.43 |
| RandomForest (200, d=12) | 0.41 |
| **GradientBoosting (100, d=6)** | **0.39** |

**Лучшая модель:** GradientBoostingRegressor, RMSLE = 0.39  
**Топ-3 признака:** `total_distance`, `total_travel_time`, `pickup_hour`

## 💡 Выводы
- OSRM-признаки — самые важные
- Погода слабо влияет на длительность
- Бустинг лучше бэггинга

## 👤 Автор
NikitaNM
