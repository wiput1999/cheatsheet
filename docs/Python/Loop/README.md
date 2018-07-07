# Loops
Loop หรือ Iteration หรือที่ภาษาไทยที่เรียกว่า "วน"<br>
โดยการวนของ Python ก็จะมีอยู่ 2 ประเภทตามที่น้องๆต้องการใข้งาน
- วนเมื่อเงื่อนไขถูกต้อง (Condition-based Loop)
- วนตามจำนวนที่ได้ระบุไว้ (Amount-based Loop)

โดยน้องๆควรเลือกประเภทการวนให้เป็นไปตามที่มันควรจะเป็นนะครับ วิจารณญาณล้วนๆ

## Introduction to While Loop
![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/While-loop-diagram.svg/440px-While-loop-diagram.svg.png)
<br>*Photo from Wikipedia.com*

โดย `while` ก็คือการ **วนเมื่อเงื่อนไขยังคงถูกต้อง** และจะทำการหยุดเมื่อเงื่อนไขไม่เป็นจริงแล้ว หากน้องยังไม่เข้าใจก็ให้อ่านใหม่ครับ แต่ถ้าเข้าใจแล้วก็อ่านเรื่องต่อไปได้เลย

!> **คำแนะนำ**<br>
เนื่องจากว่าอันนี้มันง่ายที่สุด พี่เลยแนะนำว่าให้มาลองเล่นอันนี้ให้่ชำนาญก่อนนะครับ ก่อนที่จะไปหา Loop อีกประเภทนึง

### วิธีการใช้ WHILE loop
```python
while <arguments>:
    # และจะรันโค้ดด้านล่างเมื่อ <argument> ยังเป็นจริง
```

ตัวอย่างเช่น
```python
count = 10
while count > 5:
    print(count)
    count = count - 1

# Results
10
9
8
7
6
```


### Infinite Loop
![](http://3.bp.blogspot.com/_F7vpRIjAvYI/TIU7VpNlbzI/AAAAAAAABoI/s2clJ4LoWO0/s1600/image.png)

น้องอาจจะยังไม่เข้าใจว่า Infinite Loop คืออะไร<br>
1 Infinite Loop เป็นบ้านของ Apple ครับ<br>

หยอกๆ Infinite Loop ก็คือ Loop ที่ัยังไม่จบนั่นเอง<br>
เนื่องจากอะไรนั่นเหรอ ก็เพราะว่าเงื่อนไขยังไม่เป็นจริงซักทียังไงหล่ะ มันก็เลยเกิด

และเมื่อเกิดแล้ว น้องก็จะหยุดมันไม่ได้ครับ ยกเว้นว่าต้องทำการหยุดด้วยการ Terminate โปรแกรม


เอาเป็นว่าไปดูตัวอย่างดีกว่าครับ

```python
kumamon = "cute"
while (kumamon = "cute"):
  print("You are in an infinite loop")

# Returns
You are in an infinite loop
You are in an infinite loop
You are in an infinite loop
You are in an infinite loop
...
...
...
...
# แล้วมันไม่หยุดเลยครับ จริงๆนะ
```
ถ้าสังเกตดีๆ บรรทัดแรกพี่ได้ประกาศตัวแปร kumamon ให้เท่ากับ "cute" มันก็ไม่มีอะไรแปลกประหลาด
บรรทัดที่ 2 พี่ได้เขียนว่า "เมื่อตัวแปร kumamon เท่ากับ "cute" แล้วก็จะให้วน loop" ก็ไม่แปลกอะไร แล้ว loop ก็เรื่มครับ เพราะว่าเป็นจริง

แต่ว่า ไม่มีบรรทัดไหนมีการเปลี่ยนตัวแปร kumamon เลย ทำให้ "เมื่อตัวแปร kumamon เท่ากับ "cute" แล้วก็จะให้วน loop" ยังคงเป็นจริงอยู่ ทำให้วนอยู่แบบนี้แหละครับ ไม่มีใครหยุดมันเลย

## คำสั่งอื่นๆที่เกี่ยวข้อง (Break & Continue)
เนื่องจากว่า น้องต้องการทำ loop แต่ก็อยากที่จะข้าม หรือหยุด loop เมื่อถึงเงื่อนไขที่น้องตั้งเพื่มขึ้นมานั่นเอง<br>
ใน lecture นี้ก็จะสอน keyword ทืี่น้องเอาไว้คุม loop 2 อัน นั่นก็คือ
- Break
- Continue

### Using break
เป็น keyword ที่ว่า เมื่อ loop ถึงบรรทัด break นี้ได้ก็จะทำการออก loop นั้นทันที

!> **ข้อระวัง**<br>ออกแค่ใน loop ที่ตัวเองอยู่ หากว่าอยู่ใน loop ซ้อน loop ก็จะออก loop ที่ตัวเองอยู่ แต่ไม่ได้ออก loop ที่วนอยู่ภายนอก

ตัวอย่างการใช้ `break`
```python
kumamon = "cute"
age = 21

while (kumamon == "cute"):
    print("I am happy")
    age += 1
    
    if (age == 25):
        break
```

ก็จะออกผลมาว่า
```
I am happy
I am happy
I am happy
I am happy
```
เพราะได้วน 4 รอบ แต่ทำไมวนได้ 4 รอบหล่ะ

รอบแรกค่า age = 21 และก็ได้เพื่มในบรรทัดที่ 6 เป็น 22 ครับ และบรรทัดที่ 8 ก็ไม่เป็นจริง เพราะว่า 22 ไม่เท่ากับ 25 ครับ<br>
รอบที่ 2 ก็เช่่นกัน age = 22 และก็ได้เพื่มในบรรทัดที่ 6 เป็น 23 ครับ และบรรทัดที่ 8 ก็ไม่เป็นจริง เพราะว่า 23 ไม่เท่ากับ 25 ครับ

วนไปถึงรอบที่ 4 age = 24 และก็ได้เพื่มในบรรทัดที่ 6 เป็น 25 ครับ และบรรทัดที่ 8 ก็เป็นจริง เพราะว่า 25 เท่ากับ 25 แล้ว จึงถึงบรรทัดที่มี `break` ได้ ทำให้โปรแกรมออกจาก loop มานั่นเอง 

### Using continue
โดยตัว continue นั้นมีความแตกต่างกับ break อยู่นิดเดียว นั่นก็คือ หากถึงบรรทัดนั่นแล้ว ก็จะกลับไปรัน loop ใหม่ โดยทำให้ข้ามบรรทัดที่จะทำงานหลังมันทันที

ถ้ายังไม่เข้าใจก็ไปดูกันครับ
```python
i = 0
while (true):
    i += 1
    if (i == 5):
        continue

    print(i, end=" ")

print("Loop is complete!")
```
ก็จะแสดงผลออกมาดังนี้ครับ
```
"0 1 2 3 4 6 7 8 9 Loop is complete!"
```
น้องก็จะเห็นว่า พอ i = 5 แล้ว ก็จะไม่รันโค้ดด้านล่างเลย (บรรทัดที่ 7 เป็นต้นไป)<br>
แต่เนื่องจากว่าบรรทัดที่ 9 นั้นไม่ได้อยู่ใน loop เลยยังถูกรันอย่างปกติดี

| How to use   | **break**       | **continue**                 |
| ------------ | --------------- | ---------------------------- |
| **Benefits** | Stops the loop  | Reset the loop flow          |
| **For**      | Use as failsafe | Stop program from doing more |

# Introduction to For Loop
![](https://www.programtopia.net/sites/default/files/for_0.png)
```python
How to use:
for <variable> in range(<stop>):
for <variable> in range(<start>,<stop>):

Example
for i in range(10):
    print(i, end=" ")

# Returns 0 1 2 3 4 5 6 7 8 9
```
"for i" is to start a loop. 'i' variable will be number consists of "in range(x,y)".

### For loop without range()
```python
for i in "Kumamon":
    print(i, end=" ")

# Returns "K u m a m o n"
```
This loop will run for every character in "Kumamon". The loop will go for the length of that string

### For loop using text array
```python
text = "Kumamon"
for i in text:
    print(i, end=" ")

# Returns "K u m a m o n"
```
Using range(len()) will help you to make you loop for a length of a string

### For loop using array
```python
text = [1,2,3,4,5]
for i in text:
    print(i, end=" ")

# Returns "1 2 3 4 5"
```

or using the array listings number
```python
text = [1,2,3,4,5]
for i in range(len(text)):
    print(text[i], end=" ")

# Returns "1 2 3 4 5"
```

### Nested For loops
![](http://etutorials.org/shared/images/tutorials/tutorial_23/09inf08.gif)
Program will run the first loop, then encounter the second loop, then encounter the third loop.

This program will run to the total of 2 x 2 x 2 = 8 times.
```python
for i in range(2):
    for j in range(2):
        for k in range(2):
            print(i, j, k)

# Returns
0 0 0
0 0 1
0 1 0
0 1 1
1 0 0
1 0 1
1 1 0
1 1 1
```

### Using For loops to call function
```python
def main():
    for i in range(2):
        for j in range(2):
            kumamon(i, j)

def kumamon(num1, num2):
    print(num1 + num2)

main()

# Returns
0
1
1
2
```

---

## Introduction to variable manipulator
### Using in
`in` keyword is pretty much like equal sign. But it can return true if **some** element does qualify.

```python
How to use:
<text> in <text>

Example
"kumamon" in "kumamon is happy" # Returns True
"kumamoto" in "kumamon is happy" # Returns False
```
in is a tester that find the text within the text. Similarly to .find()

## Use in arrays
```python
Example

shopping_list = ['Apple', 'Banana', 'Peanut', 'Butter', 'Jelly']

"Apple" in shopping_list # Returns true
"Kumamon" in shopping_list # Returns false
```

### Using range()
```python
How to use:
range(<stop>)
range(<start>, <stop>)
range(<start>, <stop>, <step>)

Example
range(10) # Returns 0,1,2,3,4,5,6,7,8,9
range(1,10) # Returns 1,2,3,4,5,6,7,8,9,10
range(1,10,2) # Returns 2,4,6,8,10
```
range is a number array that continues the number as you like

## Loop types comparison
| Loop Type / Sample Environment | **For**      |**While**          |
| ------------------------------ | ------------ | ----------------- |
| Requires to start              | Amount of loops | Argument that still true |
| Loop Control                   | Using in, range() or array | Using break or making argument becomes false |
| Stop when                      | Loop amount is done | When argument is false |
| Made for                       | Exact number of loops | Argument that can become false     |