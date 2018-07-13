# Lists
Like a string, a list is a sequence of values. In string, the value are characters; in a list, they can be any type. The values in a list are called **elements** or sometimes **items**.

There are several ways to create a new list; the simplest is enclose the elements in square brackets ([ and ])

### สร้าง List ขึ้นมาใหม่
ในภาษา Python น้องๆไม่จำเป็นที่จะต้องประกาศตัวแปรการจัดเก็บนะครับสามารถบอกค่าให้มันได้เลย

หากน้องๆอยากที่จะสร้าง List เปล่าขึ้นมา 1 อัน ก็สามารถเขียนได้ว่า
```python
var1 = list()
```
หรือ
```python
var2 = []
```
แต่ถ้าน้องต้องการระบุขนาดไว้ล่วงหน้า ก็สามารถใส่ค่าว่างเข้าไปได้ครับ ดังนี้
```python
var3 = [None, None, None]
```
หรือถ้าน้องต้องการใส่ข้อมูลเข้าไปเองเลย ก็สามารถทำได้ดังนี้ครับ
```python
kumamon = ['Kumamon', 'is', 'so', 'cute']
numbers = [1, 2, 3, 4]
```

## เข้าถึงข้อมูลใน List
น้องๆสามารถเข้าถึงข้อมูลได้โดยการใช้ [] เหมือน String เลย

ตัวอย่างเช่น
```python
kumamon = ['Kumamon', 'is', 'so', 'cute']
var1 = kumamon[0]

print(var1) # ก็จะได้ผลลัพท์เป็น 'Kumamon'
type(var1) # ก็จะเป็นประเภท String
```

หรืออาจจะเลือกหลายๆอันเหมือน String เช่น
```python
kumamon = ['Kumamon', 'is', 'so', 'cute']
var1 = kumamon[0:2]

print(var1) # ก็จะได้ผลลัพท์เป็น ['Kumamon', 'is', 'so']
type(var1) # ก็จะออกมาเป็น <class 'list'> (ตัวแปรประเภท list)
```


## การนับลำดับของ List
หลักการของการนับลำดับข้อมูลใน List ก็เหมือนกับ String นะครับ
โดยให้ตัวแรกมีค่าเท่ากับ 0 และนับไปเรื่อยๆครับ
| **Value**          | Kumamon | is | so | cute |
| ------------------ | ------- | -- | -- | ---- |
| **Array Number**   | 0       | 1  | 2  | 3    |
| **Logical Number** | 1       | 2  | 3  | 4    |


then looked at numbers

| **Value**          | 1 | 2 | 3 | 4 |
| ------------------ | - | - | - | - |
| **Array Number**   | 0 | 1 | 2 | 3 |
| **Logical Number** | 1 | 2 | 3 | 4 |

## เพื่มข้อมูลไปใน List
### ด้วยการใช้ method `.append()`
```Python
kumamon = [1,2,3,4]
kumamon.append(5)

# kumamon now equals to
[1, 2, 3, 4, 5]
```
น้องๆจะเห็นว่าข้อมูลที่ถุก append จะไปอยู่ลำดับสุดท้ายเลย

### โดยการบวกจาก List อื่น
```python
text1 = ["Happy"]
text2 = ["Kumamon"]
text1 += text2

# ทำให้ตัวแปร `text1` มีค่าเท่ากับ
["Happy", "Kumamon"]
```

## การแปลงระหว่าง String และ List
### แปลง String -> List ด้วย `.split()`

ตัวอย่างการใช้งาน
```Python
text = "I am a happy Kumamon"
text = text.split() 
# ตัวแปร text มีค่าเป็น ['I', 'am', 'a', 'happy', 'Kumamon']

text = "I,am,a,happy,Kumamon"
text = text.split(",") 
# ตัวแปร text มีค่าเป็น ['I', 'am', 'a', 'happy', 'Kumamon']
```

### Using .join()
```Python
"""
How to use:
<separator you want to use>.join(<array variable>)
-> Return the new text that have been joined
"""

text = ['I', 'am', 'a', 'happy', 'Kumamon']
print(" ".join(text)) # Prints out "I am a happy Kumamon"
```

## แก้ไขข้อมูลใน List
### ใช้ method `.sort()`
```python
my_list = [1, 3, 4, 2, 5]
my_list.sort()

# my_list now equals to
[1, 2, 3, 4, 5]
```

### ใช้ function `sorted()`
```python
my_list = [1, 3, 4, 2, 5]
sorted(my_list)

# my_list now equals to
[1, 2, 3, 4, 5]
```

แต่หากว่าน้องๆต้องการที่จะ sort จากหลังมาหน้า<br>
ก็ให้ใส่ Parameter `reverse` และให้มันเป็น True ครับ

ตัวอย่างเช่น
```Python
my_list = [1, 3, 4, 2, 5]
my_list.sort(reverse = True)

# my_list now equals to
[5, 4, 3, 2, 1]
```

เช่นเดียวกันกับการใช้ `sorted()`

### ข้อสังเกตของการใช้ sort
การ sort นี้จะทำการเลือกจากตัวข้อมูลที่มีค่า ASCII ต่ำที่สุดก่อน ทำให้การ sort ตัวอักษรเป็นแบบนี้
```Python
my_list = ['a', 'A', 'z', 'Z']
my_list = my_list.sort()

# my_list now equals to

```

Again, sorting use the comparing techniques, so integer cannot be sorted with strings
```Python
my_list = [9, 1, 'a', 'A']
my_list = my_list.sort()

# Return ValueError because integer cannot be compared with character
```

## หาข้อมูลใน List
### หาว่าข้อมูลอยู่ที่ลำดับใดด้วย .index()
ตัวอย่างการใช้งาน
```
<list_variable>.list(<key>)
```

วิธีการใช้งาน
```
my_list = ["Happy", "Funny", "Fat"]
index_number = my_list.index("Happy")

print(index_number)
```
ก็จะแสดงค่าออกมาเป็น 0 เพราะคำว่า "Happy" อยู่ที่ลำดับที่ 0


# ลบข้อมูลใน List
### นำข้อมูลออกไปและไปแทนในตัวแปรด้วย .pop()
.pop() หากถูกเรียกใช้แล้ว ก็จะคืนค่าเข้าไปอยู่ใตัวแปรที่เรียก และทำการลบข้อมูลนั้นออกจาก List เลย<br>
ให้คิดว่ามันคือการย้ายข้อมูลเข้าไปในตัวแปรนั่นเอง

วิธีการใช้งาน
```
How to use:
<variable name>.pop("<character/text/array number you want to use>")
-> Returns the selected item, and removing them from array
```

ตัวอย่างการใช้งาน
```Python
my_list = ["Happy", "Funny", "Fat"]
print(my_list.pop(1))

# Returns "Funny"
# and my_list = ["Happy", "Fat"]
```

### นำข้อมูลออกจาก List ด้วย .remove()
.remove() จะทำการลบข้อมูลที่น้องเลือกออกจากตั list เลย

!> และหลังจากการทำ `.remove()` ตัว List จะทำการคำนวณลำดับใน list ใหม่

ตัวอย่างการใช้งาน
```
<variable name>.remove("<character/text/array number you want to remove>")
-> Variable will update as you wish
```

วิธีก่รใช้งาน
```python
my_list = ["Happy", "Funny", "Fat"]
my_list.remove("Funny")

# my_list is now equals to ["Happy", "Fat"]
```

### แทนค่าใน List ด้วย .replace()
```Python
"""
How to use:
<variable name>.replace(<text that you like to change>,<text that you like to change to>)
-> Returns the text that have been modified
"""

text = "Hello, my name is Kumamon"
return text.replace("Kumamon", "Rillakuma")
# Returns "Hello, my name is Rillakuma"
```