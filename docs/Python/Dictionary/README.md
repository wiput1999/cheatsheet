# Dictionary
Dictionary เป็นการเก็บข้อมูลประเภทหนึ่ง ซึ่งจะมีความคล้ายคลึงกับการเก็บตัวแปรหลายๆอันเข้าไปสู่ตัวแปรเดียวกัน

โดย Dictionary จะมีข้อมูลอยู่ 2 ประเภท นั่นคือ

- Key (หากเปรียบเทียบ ก็คือตัวแปร)
- Value (หากเปรียบเทียบ ก็คือค่าที่อยู่ในตัวแปร)

แต่น้องๆก็อย่าลืมว่า Dictionary สามารถเก็บข้อมูลได้หลายๆอัน ทำให้น้องๆสามารถเรียกค่า (Key) เพื่อเอาผลลัพท์ (Value) ได้

## สร้าง dictionary
### สร้าง Dictionary เปล่าๆ
โดยการใช้ฟังก์ชั่น `dict()` เพื่อเปลี่ยนตัวแปรให้เก็บข้อมูลแบบ Dictionary
```python
my_dictionary = dict()
```

### สร้าง dictionary โดยการเขียนเอง
โดยฝั่งซ้ายจะเป็นค่า key และฝั่งขวาจะเป็นค่า value
```python
my_dictionary = {
"happy" : 20,
"not happy" : 30,
"sad" : False,
}
```

## เอาข้อมูลออกมาจาก Dictionary
```python
my_dictionary['happy'] # Returns 20
```

หรือน้องๆอาจจะเช็คก่อนว่ามี key นั้นๆอยู่หรือเปล่าโดยการใช้ keyword `ìn`
```python
"happy" in my_dictionary # Return true
20 in my_dictionary # Return true
```

# เพื่มค่าเข้าใปใน Dictionary
You can add it like list.
```python
alphabet = input()
my_dictionary = dict()

for i in alphabet:
    if not i in my_dictionary:
      my_dictionary[i] = 1
    else:
      my_dictionary += 1

```
