Сервис, обеспечивающий работу с базой данных.

![[Pasted image 20231029223434.png]]

# Docs

### BlockUnit

\<\<enumiration\>\>

**Attributes:**
- id: Идентификационный номер блокировки
- block_mode: Режим блокировки
- relation: Отношение(я), на которое(ые) направлена блокировка
- block_time: Время создания блокировки

### DataBase

\<\<singleton\>\>

**Attributes:**
- cursor: Курсор БД
- is_connected: Маркер, показывающий, подключен ли сервис к БД
- blocks_list: Список активных блокировок

**Methods:**

- \_\_init\_\_
	Params:
	- \*\*kwargs: Параметры для инициализации БД

- open_connection
	Params:
	- None
	Return:
	- is_connected: Маркер, показывающий, подключен ли сервис к БД

- close_connection
	Params:
	- None
	Return:
	- is_connected: Маркер, показывающий, подключен ли сервис к БД

- block
	Params:
	- id: Идентификационный номер блокировки
	- block_mode: Режим блокировки
	- relation: Отношение(я), на которое(ые) направлена блокировка
	- block_time: Время создания блокировки
	Return:
	- None

- unblock
	Params:
	- BlockUnit: Блокировка
	Return:
	- is_unblocked: Маркер, показывающий, отменена ли блокировка

- get_blocks
	Params:
	- None
	Return:
	- blocks_list: Список блокировок

**Множество геттеров (по необходимости список расширять!!!)**

- get_users
	Params:
	- None
	Return:
	- users_list: Список пользователей
