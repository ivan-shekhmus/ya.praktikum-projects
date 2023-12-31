# Исследование закономерностей успешности продаж игр 
***Ранний проект***

## Данные

- Name — название игры
- Platform — платформа
- Year_of_Release — год выпуска
- Genre — жанр игры
- NA_sales — продажи в Северной Америке (миллионы проданных копий)
- EU_sales — продажи в Европе (миллионы проданных копий)
- JP_sales — продажи в Японии (миллионы проданных копий)
- Other_sales — продажи в других странах (миллионы проданных копий)
- Critic_Score — оценка критиков (максимум 100)
- User_Score — оценка пользователей (максимум 10)
- Rating — рейтинг от организации ESRB (англ. Entertainment Software Rating Board). Эта ассоциация определяет рейтинг компьютерных игр и присваивает им подходящую возрастную категорию.

## Задача

Из открытых источников доступны исторические данные о продажах игр, оценки пользователей и экспертов, жанры и платформы (например, Xbox или PlayStation). <br>
Необходимо выявить определяющие успешность игры закономерности. Это позволит сделать ставку на потенциально популярный продукт и спланировать рекламные кампании.<br>
Также нужно отработать принцип работы с данными, чтобы можно было прогнозировать продажи на будущее.

## Используемые библиотеки

*Pandas* <br>
*NumPy* <br>

 ## Вывод
 В рамках проекта была проведена следующая работа:  
1. **Выполнен общий обзор данных**:  
Аббревиатура "tbd" в столбце *user_score* была заменена на пропуски "nan". С 1993 года до 2010 года наблюдается рост числа релизов игр. Далее идет резкий спад с дальнейшей стагнацией после 2011 года. Большинство критиков оценивает игры от 60 до 85 баллов. Пользователи оценивают игры в основном от 6.5 до 8.7 баллов.  Самые популярные приставки: PS2, DS и PS3. Больше всего игр в жанре action и sports. Самый популярный рейтинг Е - для всех возрастов.
2. **Выполнена подготовка данных**:
Было удалено немногочисленное кол-во строк с пропусками в столбцах *'name'*, *'genre'* и *'year_of_relase'*. Добавлен столбец *'all_sales'* с суммарными продажами во всех регионах.
3. **Исследовательский анализ данных**:
Была выявлена средняя продолжительность жизни игровой платформы, равная 10 годам. Был выбран актуальный период с 2013 года, включительно, в этом году вышли популярные платформы PS4, XOnе. Так же после 2013 снизился общий уровень продаж. Также популярными платформами были выбраны РС и 3DS. В среднем наилучшие показатели продаж имеют платформы: PS3, PS4,, Wii, WiiU, 3DS, X360 и XOne. Выяснили, что хорошая оценка критиков (от 70 и выше) повышает шансы игры на большие продажи, при этом в общем оценка критиков на продажи не влияет. Оценка пользователей вообще не имеют влияния на продажи. Жанр Action является фаворитом среди всех жанров, он имеет как самое большое кол-во игр, так и самые крупные продажи. Самым малочисленным и наименее продаваемым является жанр Puzzle. Самыми стабильно прибыльными жанрами после жанра Shooter являются Sports и Platform.
4. **Портрет пользователя каждого региона**:  
*Популярность платформ по регионам:*  <br>
В Европе платформы PS4, PS3, XOne, X360 и 3DS входят в топ-5 самых популярных;  <br>
В Японии: 3DS, PS3, PSV, PS4, WiiU;  <br>
В Северной Америке: PS4, XOne, X360, PS3, 3DS;  <br>
В остальных странах: PS4, PS3, XOne, X360 и 3DS, аналогично ситуации в Европе.  <br>
Самые платежеспособные регионы это СА и Европа. Япония занимает примерно такую же долю, как и се остальные страны кроме СА и Европы.  
*Популярность жанров по регионам:*  <br>
Топ-5 популярных жанров в регионе Европа: Action, Shooter, Sports, Role-Playing, Pacing и Misc разделяют пятую позицию, однако Pacing немного более продаваемый.  <br>
Топ-5 популярных жанров в регионе Япония: Role-Playing, Action, Misc, Fighting, Shooter.  <br>
Топ-5 популярных жанров в регионе СА: Action, Shooter, Sports, Role-Playing, Misc. <br> 
Топ-5 популярных жанров в регионе остальные страны: Action, Shooter, Sports, Role-Playing, Misc.  <br>
Больше всего рейтинг от ESRB влияет на Европу, Северную Америку и остальные страны. В Японии влияние рейтинга минимально. Чем больше людей попадает в категорию, тем больше продаж. За актуальный период самый популярный рейтинг М - старше 17 лет.
5. **Проверка гипотез**:  
В результате проверки гипотез выяснилось, что:  
средние пользовательские рейтинги платформ XOne и РС могут быть одинаковыми;  
средний пользовательский рейтинг жанра Action и Sports не одинаковые.  