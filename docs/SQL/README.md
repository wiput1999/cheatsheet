# MySQL

||**เลือกข้อมูลบนตาราง**||
|:-|:-|:-|
|[SELECT](/MySQL/SELECT.md)| **SELECT**<br>`SELECT [column_name]`<br>|**Required command**<br>`FROM`<br><br>**Optional Modifier**<br>`SELECT DISTINCT [column_name]`|
|| **FROM**<br>`FROM [table_name]`|**Required command**<br>`SELECT`|
|[WHERE](/MySQL/WHERE.md)| **WHERE**<br>`WHERE [arguments]`| **Required command**<br>`SELECT` & `FROM`|
|[ORDER](/MySQL/ORDER.md)| **ORDER BY**<br>`ORDER BY [column_name] [ASC / DESC]`| **Required command**<br>`SELECT` & `FROM`|

||Data Manipulation Language (DML)<br>**เพื่ม ลบตาราง + แก้ไข column**||
|-|:-|:-|
|| **CREATE** - สร้างตาราง<br>`CREATE TABLE [table_name]`||
|| **ALTER** - แก้ไขข้อมูลตาราง<br>`ALTER TABLE [table_name]`|**Required Modifier**<br>`[ADD / MODIFY / DROP] [column_name] [column_constraints]`|
|| **DROP** - ลบตารางออก<br>`DROP TABLE [table_name]`|

||จับกลุ่ม||
|-|:-|:-|
||**GROUP**<br>`GROUP BY [column_name]`||
||**HAVING**<br>`HAVING [arguments]`||

|| **เพื่ม ลบ แก้ row ตาราง**||
|-|:-|:-|
|[INSERT](/MySQL/DML/INSERT.md)|**INSERT**<br>`INSERT INTO [table_name]`|**Required command**<br>`VALUES [value_list]`||
|[UPDATE](/MySQL/DML/UPDATE.md)|**UPDATE**<br>`UPDATE [table_name]`|**Required command**<br>`SET [column_name] = [argument] WHERE[argument]`|
|[DELETE](/MySQL/DML/DELETE.md)|**DELETE**<br>`DELETE FROM [table_name]|**Required command**<br>`WHERE [arguments]|

||**รวมตาราง**||
|-|-|-|
|[Natural Join](/MySQL/Join/Inner/Natural-JOIN.md)| **NATURAL JOIN**<br>`NATURAL JOIN [table_name]`| **Required command**<br>`FROM`|
|[INNER Join](/MySQL/Join/Inner/)| **INNER JOIN**<br>`INNER JOIN [table_name]` or <br>`JOIN [table_name]`|**Required modifier**<br>`USING [common_key_name]` or `ON [table1_key] = [table2_key]`|
|[OUTER Join](/MySQL/JOIN/Outer)| **OUTER JOIN**<br>`[LEFT / RIGHT / FULL] OUTER JOIN [table_name]`|**Required modifier**<br>`USING [common_key_name]` or <br>`ON [table1_key] = [table2_key]`|

||จัดการตารางโดยรวม||
|-|-|-|
||**RENAME**<br>`RENAME [table_name] [new_table_name]`||
||**SET INTEGRITY**<br>`SET FOREIGN_KEY_CHECKS =  [true / false]`||

||Transaction Control||
|-|:-|:-|
|[COMMIT](/MySQL/Transaction/COMMIT.md)|**COMMIT**<br>`COMMIT`||
|[ROLLBACK](/MySQL/Transaction/ROLLBACK.md)|**ROLLBACK**<br>`ROLLBACK [checkpoint_name]`||
|[SAVEPOINT](/MySQL/Transaction/SAVEPOINT.md)|**SAVEPOINT**<br>`SAVEPOINT [new_savepoint_name]`||
