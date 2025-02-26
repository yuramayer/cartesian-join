# Left Join

**Left Join** - возвращает все строки из первой таблицы и соответствующие им из второй. Если соответствующих нет, возвращается `null`


### Без null, без повторений

#### Код

```sql
with tab_A as (
	select generate_series(1, 3) as col_A
	),
tab_B as (
	select generate_series(2, 4) as col_B
	)
select *
from tab_A
	left join
	tab_B
	on tab_A.col_A = tab_B.col_B
;
```

#### Вывод
![Вывод SQL кода](img/code_1.png)

#### Теория

![Фрейм таблицы](img/tab_1.png)

