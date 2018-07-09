# Runtime on Python
หลังจากน้องๆได้เรียนวิธีการเขียน Python แบบหลักการไปแล้ว><br>
ใน lecture นี้ก็จะมาดูกันว่า Python และภาษาโปรแกรมหลายๆอันเค้่าทำอะไร เมื่อโปรแกรมถูกทำงานแล้ว

เราก็ต้องมาดูกันก่อนครับ ว่ากว่าโค้ดของน้องๆจะรันได้ Python ต้องทำอะไรบ้าง
1. **Compile**
2.
3. **Interpret** แปลง

## เกิด Error
ก็ปกติอ่ะเนอะ ที่โปรแกรมจะเจอปัญหา แต่เราก็สามารถแยกปัญหาออกมาเป็น 2 ประเภทได้ นั่นคือ
- Compile Error
- Runtime Error

โดยทั้ง 2 อันนี้จะแตกต่างกันด้วยว่า อันนึงเกิดก่อนที่โปรแกรมจะรันจริงๆ กับอีกอันคือเกิดเมื่อรันไปแล้วนั่นเอง

หากน้องๆยังไม่รู้ว่ามันต่างกันอย่างไร ก็ไปดูกันครับ
```python
var == 21
print(var)
```

พอรันแล้ว ก็จะแจ้งเตือนแบบนี้ครับ 
```
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'var' is not defined
```
ตัว Python ได้แจ้งบอกถึง `NameError` ครับ เพราะว่าน้องๆยังไม่ได้บอกตัวแปร `var` ในบรรทัดที่ 1 เลย ทำให้มันพังตั้งแต่บรรทัดที่ 1 แล้วครับ

แต่คำว่าพัง ก็ไม่ได้หมายความว่า Python มันจะรันไปแล้วนะครับ มันยังไม่ได้รัน เพราะมันยังไม่เข้าใจว่าตัวแปร `var` คืออะไร ทำให้มันบอกน้องๆก่อนว่ามันไม่เข้าใจนั่นเอง และหยุดการทำงานของ Compiler ทันที

กับอีกแบบนึงครับ
```python
# File RTErrorExample1.py
first_name = input()
first_name = int(first_name)
```
อันนี้โปรแกรมก็จะทำงานได้อย่างปกติดีครับ เพราะว่าน้องๆเขียนโค้ดได้อย่างถูกต้อง<br>
แต่หากว่าน้องๆเอา string เข้าไป เช่น "kumamon" ก็จะเกิดแบบนี้ขึ้นครับ

```
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '"kumamon"'
```


--- 
Reference
[softwareengineering.stackexchange.com/questions/313254/how-does-the-python-runtime-actually-work](https://softwareengineering.stackexchange.com/questions/313254/how-does-the-python-runtime-actually-work)