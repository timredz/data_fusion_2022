# data_fusion_insight
Номинация 2, Insight

## Как добился самого высокого MRR скора на лидерборде в задаче Puzzle
На последний день соревнования у моего решения самый высокий MRR скор, при не самом высоком OCR. 

Это решение не смог имплементировать в main задаче из-за ограничения по времени в 60мин. Можно было частично имплементировать, но этим не занимался

#### Гипотеза
Есть набор MCC и CAT, которые часто встречаются рядом (по времени) в пределах 2х часов. По этим сочетаниям можно угадать пары банк-ртк

#### Что делал?
Взял 15т. пар из трейн. Смержил transactions и clickstream по дате и user_id. Получилось примерно такое:

user_id  | date | mcc_code | cat_id | transaction_time | clickstream_time | delta_time_abs_sec
-------- | -----| -------- |------  |------            |------            |------ 
1051  | 10.07.2021 | 7832  | 552    |  08:05:23        |     09:25:43     | 4820 sec
1051  | 10.07.2021  | 5200 | 170    |  16:05:40        |     23:50:40     | 27900 sec 

Отбираем записи с delta_time_abs_sec < 2 часа и группируем по mcc и cat:

mcc_code|	cat_id|	dist|	count|	clients
-------- | -----| -------- |------  |------
2941 |	7832|	552	|6504|	35|	33
3132|	5200|	170|	6801|	80|	27



![](https://pandao.github.io/editor.md/examples/images/4.jpg)

> Follow your heart.

+ Item A
+ Item B
    + Item B 1
    + Item B 2
    + Item B 3
+ Item C
    * Item C 1
    * Item C 2
    * Item C 3


First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell 
