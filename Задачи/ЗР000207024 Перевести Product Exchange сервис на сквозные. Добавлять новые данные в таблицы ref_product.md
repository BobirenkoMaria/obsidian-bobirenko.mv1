### Цель:
Добавить параллельно записи в ref_product_ce запись в ref_product для баз данных orders и useractivity.
### Описание: 
Ранее были добавлены таблицы на основе ref_product_ce: 
- В базе данных orders - таблица ref_product с 4 полями.
- В базе данных useractivity - таблица ref_product с 5 полями.
При создании новых таблиц ref_product на основе ref_product_ce были вырезаны все неиспользуемые поля, а используемые добавлены в новые таблицы.
### Задача:
Необходимо добавить дополнительную запись данных в новую таблицу ref_product на основе существующей записи в ref_product_ce.
Добавление в новые таблицы должно происходить только для указанных ниже полей в соответствующие базы данных.
Для базы данных orders:
- guid
- title
- code
- search_uid
Для базы данных useractivity:
- guid 
- manufacturer_guid 
- spec_guid
- multi_card_guid
- product_type_guid