#wildberies
![[Pasted image 20250309125510.png]]
#### Решение
```sql
-- первый способ
select name where id not in (select id from employee where parent_id is null) from employee

-- второй способ 
select name from employee e left join employee e2 on e.id == e2.parent_id where e2.id is null
```
---
#ozon
