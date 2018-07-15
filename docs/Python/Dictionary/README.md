# Dictionary
Dictionary เป็นการเก็บข้อมูลประเภทหนึ่ง ซึ่งจะมีความคล้ายคลึงกับการเก็บตัวแปรหลายๆอันเข้าไปสู่ตัวแปรเดียวกัน

โดย Dictionary จะมีข้อมูลอยู่ 2 ประเภท นั่นคือ

- Key (หากเปรียบเทียบ ก็คือตัวแปร)
- Value (หากเปรียบเทียบ ก็คือค่าที่อยู่ในตัวแปร)

แต่น้องๆก็อย่าลืมว่า Dictionary สามารถเก็บข้อมูลได้หลายๆอัน ทำให้น้องๆสามารถเรียกค่า (Key) เพื่อเอาผลลัพท์ (Value) ได้

## สร้าง dictionary เปล่า
```python
my_dictionary = dict()
```

## สร้าง dictionary โดยการเขียนเอง
```python
my_dictionary = {
"happy" : 20,
"not happy" : 30,
"sad" : False,
}
```

# Accessing the value from key
```python
my_dictionary['happy'] # Returns 20
```

or checking if this key or value exists in dictionary

```python
"happy" in my_dictionary # Return true
20 in my_dictionary # Return true
```

# Adding key and value to the dictionary
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
