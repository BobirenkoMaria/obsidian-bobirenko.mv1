
# TODO
``` dataview
TASK FROM "TODO" 
WHERE !completed AND !checked
```
---
# Сделано сегодня
```dataview
TASK FROM "TODO"
WHERE date(split(completion, " ")[0]) = date(today)
```
---
# Последние изменения
```dataview
TABLE WITHOUT ID 
	file.link AS "Задача", 
	file.cday AS "Создано",
	date-end AS "Выполнена",
	file.mday AS "Изменено"
FROM "Задачи" or "Заявки" or "Документация" or "README" or "Self Review"
SORT file.mday DESC, date-end DESC, file.cday DESC
LIMIT 5
```


