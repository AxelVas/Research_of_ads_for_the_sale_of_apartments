## Исследование объявлений о продаже квартир
![image](https://user-images.githubusercontent.com/76148212/122681626-edb62380-d1fd-11eb-89b3-96ff79ae2893.png)
## Описание проекта
В нашем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Наша задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность. 

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма.
## Краткое описание проведённой работы:
> Проведен исследовательский анализ и предобработка данных для датасета с объявлениями о продаже квартир в Санкт-Петербурге. 
Выявлены, влияние площади, потолков, количества комнат, даты объявления на цены квартир всех представленных населённых пунктов и центра Санкт-Петербурга для построения автоматизированной системы определения цен во избежание мошенничества и аномалий.
На основе данных сервиса Яндекс.Недвижимость определена рыночная стоимость
объектов недвижимости разного типа, типичные параметры квартир, в зависимости от
удаленности от центра. Проведена предобработка данных. Добавлены новые данные.
Построены гистограммы, боксплоты, диаграммы рассеивания.

## Стэк:
`Python`
`Pandas`
`Matplotlib`
`исследовательский анализ данных`
`визуализация данных`
`предобработка данных`
`math`
_____
## Полное содержание проекта:
### Данное исследование разделим на несколько частей.

##### Часть 1. Изучение общей информации 

* <a href='#step_1'>Откроем файл с данными и изучим общую информацию. </a>
* <a href='#step_1.1'>Просмотрим первые и последние 5 строк таблицы с данными</a>
* <a href='#step_1.2'>Познакомимся с данными поближе и просмотрим числовые значения методом describe()</a>
* <a href='#step_1.3'>А так же ознакомимся с типом данных и общей оиформацией по таблице</a>
* <a href='#step_1_end'>Вывод</a>


##### Часть 2. Предобработка данных 

* <a href='#step_2'>Приведём формат вывода даты и времени по столбцу "first_day_exposition"  к удобному для форматирования и обработки</a>

* <a href='#step_2.2'>Произведём подсчёт квартир с нулевым обозначением количества комнат в столбце "rooms"</a>
* <a href='#step_2.3'>Проверим значения колонки "ceiling_height"</a>
* <a href='#step_2.4'>Выполним проверку столбца "floors_total" на отсутствующие значения</a>
* <a href='#step_2.5'>Проверм данные по столбцу "living_area"</a>
* <a href='#step_2.6'>Исследуем столбец "kitchen_area" на предмет корректных значений</a>
* <a href='#step_2.7'>Исследуем колонку "balcony" на предмет отсутствующих значений</a>
* <a href='#step_2.8'>Исследуем столбец "locality_name" на предмет уникальных значений</a>
* <a href='#step_2.9'>Просмотрим значения в столбце "airports_nearest"</a>
* <a href='#step_2.10'>Приведём наименование столбца "cityCenters_nearest" в однотипный формат</a>
* <a href='#step_2.11'>Проверим значения столбца "parks_around" на предмет уникальности</a>
* <a href='#step_2.12'>Исследуем данные в колонке "parks_nearest"</a>
* <a href='#step_2.13'>Исследуем столбец "ponds_around" на предмет отсутствующих и недостоверных данных</a>
* <a href='#step_2.14'>Проведём исследование данных в колонке "ponds_nearest"</a>
* <a href='#step_2.15'>Исследуем данные в колонке "days_exposition"</a>
* <a href='#step_2.16'>Проведём исследование значений столбца "is_apartment"</a> 
* <a href='#step_2_end'>Вывод</a>


##### Часть 3. Посчитаем дополнительные данные и добавим их в таблицу

* <a href='#step_3.1'>Посчитаем и добавим в таблицу  цену квадратного метра</a>
    * <a href='#step_3.1.1'>Вывод </a>
* <a href='#step_3.2'>Посчитаем и добавим в таблицу день недели, месяц и год публикации объявления</a>
    * <a href='#step_3.1.2'>Вывод </a>
* <a href='#step_3_3'>Посчитаем и добавим в таблицу  этаж квартиры; варианты — первый, последний, другой</a>
    * <a href='#step_3.1.3'>Вывод </a>
* <a href='#step_3_4'>Посчитаем и добавим в таблицу  соотношение жилой и общей площади, а также отношение площади кухни к общей</a>
    * <a href='#step_3.1.4'>Вывод </a>
* <a href='#step_3_end'>Вывод </a>   

##### Часть 4. Проведём исследовательский анализ данных
* <a href='#step_4'>Изучим следующие параметры: площадь, цена, число комнат, высота потолков. Построим гистограммы для каждого параметра</a>
    * <a href='#step_4.1.1'>Площадь</a>
    * <a href='#step_4.1.2'>Цена</a>
    * <a href='#step_4.1.3'>Число комнат</a>
    * <a href='#step_4.1.3'>Высота потолков</a>
    * <a href='#step_4.1.end'>Вывод</a>         
* <a href='#step_4.2'>Изучим время продажи квартиры. Построим гистограмму. Посчитаем среднее и медиану.</a>
    * <a href='#step_4.2.end'>Вывод</a>
* <a href='#step_4.3'>Изучим, зависит ли цена от площади, числа комнат, удалённости от центра.</a>
    * <a href='#step_4.3.end'>Вывод</a>
* <a href='#step_4.4'>Изучим зависимость цены от того, на каком этаже расположена квартира: первом, последнем или другом</a>
    * <a href='#step_4.4.end'>Вывод</a>

* <a href='#step_4.5'>Также изучим зависимость цены от даты размещения: дня недели, месяца и года.</a>
    * <a href='#step_4.5.end'>Вывод</a>
* <a href='#step_4.6'>Выберем 10 населённых пунктов с наибольшим числом объявлений.</a>
    * <a href='#step_4.6.end'>Вывод</a>
* <a href='#step_4.7'>Посчитайте среднюю цену квадратного метра в этих населённых пунктах</a>
    * <a href='#step_4.7.end'>Вывод</a>
* <a href='#step_4.8'>Выделим среди них населённые пункты с самой высокой и низкой стоимостью жилья</a>
    * <a href='#step_4.8.end'>Вывод</a>
* <a href='#step_4.8.1'>Изучим предложения квартир: Выделим квартиры в Санкт-Петербурге ('locality_name'). Выясним, какая область входит в центр</a>
    * <a href='#step_4.8.1.end'>Вывод</a>

* <a href='#step_4.9'>Посчитаем среднюю цену для каждого километра</a>
* <a href='#step_4.10'>Выделим сегмент квартир в центре и проанализируем эту территорию</a>
    * <a href='#step_4.10.end'>Вывод</a>
* <a href='#step_4.11'>Выделим факторы, которые влияют на стоимость квартиры </a>


* <a href='#step_4_end'>Вывод</a>

##### Часть 5. Обший вывод по проведённому исследованию 

* <a href='#step_5'>Общий вывод</a>
___
___
