# Game Data Analytics

Всем привет!
Этот проект посвящён анализу данных и проведению A/B тестирования для игровой компании.

Проект выполнен на Python с использованием Jupyter Notebook.

## Задачи проекта

### Задача 1: Расчёт Retention игроков

Retention — один из ключевых показателей в компании. Ваша задача — создать функцию для расчёта retention игроков по дням, начиная с даты регистрации. 

**Описание данных**:
- **`reg_data.csv`** — данные о времени регистрации:
  - `reg_ts` — время регистрации
  - `uid` — уникальный идентификатор игрока

- **`auth_data.csv`** — данные о времени захода пользователей в игру:
  - `auth_ts` — время авторизации
  - `uid` — уникальный идентификатор игрока

### Задача 2: Анализ A/B теста рекламных предложений

Результаты A/B теста показали, что ARPU (средняя выручка на пользователя) в тестовой группе выше на 5% по сравнению с контрольной. В контрольной группе 1928 из 202103 пользователей оказались платящими, а в тестовой — 1805 из 202667.

- **Данные**:
  - `user_id` — идентификатор пользователя
  - `revenue` — выручка от пользователя
  - `testgroup` — группа пользователя (контрольная или тестовая)

**Задача**: Определить, какой набор предложений является лучшим. Какие метрики стоит проанализировать для принятия решения и как?

### Задача 3: Анализ результатов события в игре Plants & Gardens

В игре **Plants & Gardens** ежемесячно проходят тематические события, ограниченные по времени. Во время этих событий игроки могут получить уникальные предметы для сада, персонажей, дополнительные монеты и бонусы, выполнив определённые задания. 

**Задача**: Определить метрики для оценки результатов последнего события. Метрики могут включать количество игроков, завершивших задания, среднее количество уровней, пройденных во время события, выручка от участников события и т.д.

## Описание используемых библиотек

- `pandas` — для работы с данными, обработки и фильтрации таблиц
- `numpy` — для математических операций и расчётов
- `seaborn` и `matplotlib.pyplot` — для визуализации данных
- `scipy.stats` — для проведения статистических тестов, таких как тест Манна-Уитни, тест Левена и однофакторный дисперсионный анализ

## Основные функции и методы

- **Анализ retention (удержания) игроков**:
    - Вычисление ежедневного retention игроков, начиная с даты регистрации.
    - Сопоставление дат регистрации и авторизаций для расчёта количества удержанных пользователей по дням.

- **Проведение A/B теста**:
    - **Метрики для анализа**:
        - ARPU (Average Revenue per User) для каждой группы.
        - Конверсия пользователей в платящих.
        - Доля удержания в каждой группе.

- **Анализ события в игре**:
    - Расчёт средней вовлечённости пользователей в событие.
    - Подсчёт уникальных предметов и бонусов, полученных во время события.
    - Оценка выручки от события для анализа эффективности.


# Game Data Analytics

Hello everyone!  
This project is dedicated to data analysis and A/B testing for a gaming company.

The project was implemented in Python using Jupyter Notebook.

## Project Tasks

### Task 1: Calculating Player Retention

Retention is one of the key metrics for the company. Your task is to create a function to calculate daily player retention starting from the registration date.

**Data Description**:
- **`reg_data.csv`** — registration time data:
  - `reg_ts` — registration time
  - `uid` — unique player identifier

- **`auth_data.csv`** — data on users' login times in the game:
  - `auth_ts` — authorization time
  - `uid` — unique player identifier

### Task 2: Analysis of A/B Test for Advertising Offers

The A/B test results showed that ARPU (average revenue per user) in the test group is 5% higher compared to the control group. In the control group, 1928 out of 202,103 users were paying users, while in the test group, there were 1805 paying users out of 202,667.

- **Data**:
  - `user_id` — user identifier
  - `revenue` — revenue from the user
  - `testgroup` — user group (control or test)

**Objective**: Determine which offer set is the best. Which metrics should be analyzed to make a decision, and how?

### Task 3: Event Analysis in the Game *Plants & Gardens*

The game *Plants & Gardens* hosts monthly themed events with a limited timeframe. During these events, players can receive unique garden items, characters, extra coins, and bonuses by completing certain tasks.

**Objective**: Identify metrics to evaluate the results of the latest event. Metrics may include the number of players who completed tasks, the average number of levels completed during the event, revenue from event participants, etc.

## Description of Libraries Used

- `pandas` — for data handling, table processing, and filtering
- `numpy` — for mathematical operations and calculations
- `seaborn` and `matplotlib.pyplot` — for data visualization
- `scipy.stats` — for conducting statistical tests, such as the Mann-Whitney test, Levene's test, and one-way ANOVA

## Key Functions and Methods

- **Player Retention Analysis**:
    - Calculating daily player retention starting from the registration date.
    - Matching registration and authorization dates to calculate the number of retained users per day.

- **Conducting A/B Testing**:
    - **Metrics for Analysis**:
        - ARPU (Average Revenue per User) for each group.
        - Conversion rate of users to paying customers.
        - Retention rate in each group.

- **Game Event Analysis**:
    - Calculating average user engagement in the event.
    - Counting unique items and bonuses obtained during the event.
    - Evaluating event revenue to assess effectiveness.
