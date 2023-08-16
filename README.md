# Домашнее задание к занятию «Индексы» Фадеев Михаил

### Задание 1

Напишите запрос к учебной базе данных, который вернёт процентное отношение общего размера всех индексов к общему размеру всех таблиц.

![image](https://github.com/FadMikhail/Indexes/assets/132131230/c9e2d583-f42c-49c5-8b1a-d91b3da4542c)

### Задание 2

Выполните explain analyze следующего запроса:
```sql
select distinct concat(c.last_name, ' ', c.first_name), sum(p.amount) over (partition by c.customer_id, f.title)
from payment p, rental r, customer c, inventory i, film f
where date(p.payment_date) = '2005-07-30' and p.payment_date = r.rental_date and r.customer_id = c.customer_id and i.inventory_id = r.inventory_id
```
- перечислите узкие места;
#### Таблицы inventory, rental и film

- оптимизируйте запрос: внесите корректировки по использованию операторов, при необходимости добавьте индексы.
![image](https://github.com/FadMikhail/Indexes/assets/132131230/22ec789f-74fc-4abc-93e7-60611fcf6170)
![image](https://github.com/FadMikhail/Indexes/assets/132131230/e7cf9ab4-5001-4df2-a624-9a5dc58a487a)





