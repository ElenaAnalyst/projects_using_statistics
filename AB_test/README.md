## [Оптимизация пользовательского опыта: тестирование форматов фотографий и кнопок в приложении для доставки](https://github.com/ElenaAnalyst/projects_using_statistics/blob/main/AB_test/AB_test.ipynb)
Ознакомиться с файлом решения тут (нажать) ⤴️

### 🛠️ Стек:
<div>
<img src="https://img.shields.io/badge/python-white?logo=python&style=for-the-badge" title="Python" alt="Python" height=35"/>&nbsp;
<img src="https://img.shields.io/badge/pandas-white?logo=pandas&logoColor=blue&style=for-the-badge" title="Pandas" alt="Pandas" height="35"/>&nbsp;
<img src="https://img.shields.io/badge/-scipy.stats-FFF?style=for-the-badge&logo=scipy&logoColor=blue" title="scipy.stats" alt="scipy.stats" height="35"/>&nbsp;
<img src="https://img.shields.io/badge/-Seaborn-FFF?style=for-the-badge&logo=seaborn&logoColor=blue" title="Seaborn" alt="Seaborn" height="35"/>&nbsp;
<img src="https://img.shields.io/badge/-Matplotlib-FFF?style=for-the-badge&logo=matplotlib&logoColor=blue" title="Matplotlib" alt="Matplotlib" height="35"/>&nbsp;
<img src="https://img.shields.io/badge/statsmodels-white?logo=statsmodels&style=for-the-badge" title="statsmodels" alt="statsmodels" height=35"/>&nbsp;
<img src="https://img.shields.io/badge/pingouin-white?style=for-the-badge" title="Pingouin" alt="Pingouin" height=35"/>&nbsp;
</div>


### 📂 Методы и подходы:

- `ANOVA` – для сравнения средних между тремя форматами фотографий;
- `Тест Левена` – для проверки гомогенности дисперсий;
- Проверка нормальности – с помощью тестов и `qq-графиков`;
- `Тест Тьюки` – для определения статистически значимых различий;
- `Многофакторный дисперсионный анализ` (ANOVA) – для анализа влияния факторов на количество событий.


### 📊 В ходе проекта решены следующие задачи:

- Проведен ANOVA для проверки, какой формат фотографий лучше: A, B или C;
- Применен тест Левена, который подтвердил одинаковые дисперсии в группах;
- Проверено распределение данных, все группы показали нормальное распределение;
- Тест Тьюки показал значимые различия между группами A и B, A и C, B и C;
- Рекомендовано использовать квадратные фотографии (группа B);
- Для второго теста использован многофакторный ANOVA для анализа реакции пользователей на новый формат кнопки;
- Выявлены значимые различия между группами по сегментам пользователей, рекомендовано внедрить новый формат кнопки.

<hr>

### Выводы:

- Квадратные фотографии дают лучший результат по числу покупок;
- Новый формат кнопки положительно влияет на поведение пользователей, особенно в высокоактивных сегментах;
- Рекомендуется выкатить обе фичи на всех пользователей.

<hr>

### Описание данных:

[**AB_task_1**](https://github.com/ElenaAnalyst/projects_using_statistics/blob/main/AB_test/AB_task_1.csv) (тест разрешения фотографий блюд в приложении: пользователям показывались либо прямоугольные, либо новые квадратные): 

- `id` – id клиента в эксперименте;
- `group` – в каком разрешении показывались картинки (A – прямоугольные 16:9, B – квадратные, C – прямоугольные 12:4);
- `events` – сколько блюд суммарно было заказано за период.

[**AB_task_2**](https://github.com/ElenaAnalyst/projects_using_statistics/blob/main/AB_test/AB_task_2.csv) (была обновлена кнопка заказа, и часть юзеров видела старый вариант, а часть – новый):

- `id` – id клиента в эксперименте;
- `segment` – сегмент (high/low);
- `group` – вид кнопки (control – старая версия, test – новая версия);
- `events` – сколько блюд суммарно было заказано за период.
