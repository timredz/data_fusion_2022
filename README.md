# data_fusion_insight
Номинация 2, Insight

## Как добился самого высокого MRR скора на лидерборде в задаче Puzzle
На последний день соревнования у моего решения самый высокий MRR скор, при не самом высоком OCR. 

Это решение не смог имплементировать в main задаче из-за ограничения по времени в 60мин. Можно было частично имплементировать, но этим не занимался

#### Гипотеза
Есть набор MCC и CAT, которые часто встречаются рядом (по времени) в пределах 2х часов. По этим сочетаниям можно угадать пары банк-ртк

#### Что делал?
Взял 15т. пар из трейн. Смержил transactions и clickstream по дате и user_id. Получилось примерно такое:

user_id  | date | mcc_code | cat_id | transaction_time | clickstream_time | delta_time_absolute_value
-------- | -----| -------- |------ |------ |------ |------ 
1051  | 10.07.2021 |  |   |   |   |  
1051  | 10.07.2021  |  |   |   |   |  



mcc_code	cat_id	dist	count	clients
2941	7832	552	6504	35	33
3132	5200	170	6801	80	27
3211	4784	794	6888	40	27
3305	5999	606	6999	25	23
3580	5815	763	7325	40	22



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
