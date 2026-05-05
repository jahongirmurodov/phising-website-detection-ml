# Phishing Website Detection (Machine Learning)

## Overview
This project focuses on building a machine learning model to detect phishing websites. The model classifies web pages as either phishing (1) or legitimate (0) based on URL structure, domain reputation, and page behavior features.

## Business Context
Phishing attacks are widely used to steal user credentials and financial data. This solution can be applied in:
- Browser security extensions  
- Anti-phishing systems  
- корпоративные системы кибербезопасности  

## Objectives
- Perform data preprocessing and EDA  
- Train and compare multiple ML models  
- Optimize model performance  
- Minimize false negatives (focus on Recall)  

## Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- XGBoost / LightGBM (optional)  

## Data Description
The dataset includes features describing:

### URL Structure
- URL length, hostname length  
- number of dots, slashes, hyphens  
- presence of IP, '@', shortening services  

### Domain Reputation
- domain age, registration length  
- DNS record, Google index  
- page rank, web traffic  

### Page Behavior (HTML/JS)
- iframe, popup, onmouseover  
- login forms, external favicon  
- disabled right-click, email submission  

### Link Structure
- number of links  
- ratio of internal/external links  
- redirections  

### Target
- 1 — phishing  
- 0 — legitimate  

## Methodology

### 1. Data Preprocessing
- Checked missing values and duplicates  
- Analyzed class distribution  
- Encoded categorical features  
- Applied feature scaling (if required)  

### 2. Exploratory Data Analysis
- Class balance analysis  
- Feature distributions  
- Correlation heatmap  
- Feature importance exploration  

### 3. Model Training
Trained and compared:
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting (XGBoost / LightGBM)  

### 4. Model Evaluation
Metrics used:
- Accuracy  
- Precision  
- Recall (primary focus)  
- F1-score  
- ROC-AUC  

Additional evaluation:
- Confusion Matrix  
- ROC Curve  

### 5. Handling Class Imbalance
- class_weight  
- SMOTE / undersampling (if needed)  

### 6. Hyperparameter Tuning
- GridSearchCV / RandomizedSearchCV  

### 7. Final Model
- Selected best-performing model  
- Trained on full dataset  
- Saved model using pickle / joblib  

## Results
- Built a robust classification model  
- Achieved strong Recall for phishing detection  
- Identified key features influencing predictions  
- Reduced risk of missing phishing websites  

## Key Takeaways
- Recall is critical in security-related ML tasks  
- URL and domain features are strong predictors  
- Ensemble models outperform simple models  
- Feature engineering improves performance  

## Possible Improvements
- Deploy model as API  
- Integrate into browser extension  
- Use deep learning for advanced detection  
- Real-time data pipeline  

---

# Обнаружение фишинговых сайтов (Machine Learning)

## Обзор проекта
Проект направлен на разработку модели машинного обучения для классификации веб-страниц на фишинговые и безопасные.

## Бизнес-контекст
Фишинговые сайты используются для кражи данных пользователей. Решение может применяться в системах безопасности и браузерах.

## Цели проекта
- Предобработка данных и EDA  
- Обучение и сравнение моделей  
- Оптимизация качества модели  
- Минимизация пропуска фишинга (Recall)  

## Используемые технологии
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- XGBoost / LightGBM  

## Описание данных
Признаки описывают:
- структуру URL  
- репутацию домена  
- поведение страницы  
- ссылочную структуру  

Целевая переменная:
- 1 — фишинг  
- 0 — безопасный сайт  

## Методология
- Очистка данных  
- EDA  
- Обучение моделей (LR, Tree, RF, Boosting)  
- Оценка (Accuracy, Precision, Recall, F1, ROC-AUC)  
- Работа с дисбалансом  
- Подбор гиперпараметров  
- Выбор и сохранение модели  

## Результаты
- Построена модель классификации  
- Повышен Recall для обнаружения фишинга  
- Выявлены важные признаки  

## Выводы
- ML эффективно решает задачу обнаружения фишинга  
- Ошибки пропуска критичнее ложных срабатываний  
- Ансамбли дают лучший результат  

## Возможные улучшения
- Деплой модели  
- Интеграция в реальные системы  
- Работа с потоковыми данными
