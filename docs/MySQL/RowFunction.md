# Group Function

ต้องการการ GROUP ก่อนที่จะใช้ได้

## AVG

หาค่าเฉลี่ยของ column ที่ระบุไว้

    SELECT AVG(department_id)
    FROM employees
## SUM
    SELECT SUM(department_id)
    FROM employees
## MIN MAX
    SELECT MIN(salary), MAX(salary)
    FROM employees;

สามาารถใช้สำหรับ เวลา ตัวเลข ตัวอักษร

## COUNT
    SELECT COUNT(department_id)
    FROM employees

โดยจะไม่มีการนับแถวที่เป็นค่า NULL เมื่อ department_id ในแถวนั้นเป็น NULL


## Including Null Value to count
    SELECT AVG(IFNULL(commission_pct,0))
    FROM employees;
