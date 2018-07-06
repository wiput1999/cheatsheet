# Full Outer Join
![Select all from Table A and B](https://static1.squarespace.com/static/5732253c8a65e244fd589e4c/t/5744be65c6fc08b3af1b0fbd/1464122985024/?format=300w)

เนื่องจากคำสั่งของ MySQL ไม่มี Full Outer Join อย่างแท้จริง เลยต้องคำนวณด้วยการนำ Left Outer Join มารวม (Union) กับ Right Outer Join เพื่อให้ได้ผลลัพท์เหมือนกับ Full Outer Join

```sql
SELECT *
FROM order
LEFT OUTER JOIN employees
USING (P_Code)

UNION

SELECT *
FROM order
RIGHT OUTER JOIN employees
USING (P_Code);
```

ตาราง Full Outer Join เป็นประเภทที่ว่า หากอีกฝั่งไม่มีข้อมูลก็จะได้ค่า NULL กลับมาทั้งสองฝั่ง<br>
นั่นหมายความว่า ตารางก็จะแสดงข้อมูลทั้งหมดของทั้งตารางซ้าย และตารางขวา โดยรวมอยู่ในตารางเดียวกัน
