# String
น้องๆ ก็ได้เรียนไปแล้วถึงประเภทของตัวแปร วันนี้จะมาเรียนรู้ว่าเราจะทำอะไรได้กับตัวแปรแบบ String กันบ้าง

แต่พี่มงต้องอธิบายก่อนนะครับว่า String คืออะไร

String คือ**กลุ่ม**ของตัวอักษร (Character) อย่างน้อย 2 ตัวอักษรเป็นต้นไป (หมายความว่า String จะถูกเรียกว่า Character เมื่ิอมีตัวอักษรเพียงตัวเดียวเท่านั้น)

ตัอย่างเช่น
```python
var1 = "Hello"
var2 = "H"
```

และพี่ก็จะลองถาม Python ดูซิ ว่าเป็นตัวแปรประเภทใด โดยการใช้ฟังก์ชั่น type() นั่นเอง
```python
type(var1)
type(var2)
```

ก็จะได้คำตอบว่า
```python
<class 'str'>
<class 'str'>
```

อ่าวพี่ แล้วมันแตกต่างกันยังไงครับ<br>
น้องๆจะเห็นว่าน้องสามารถเอาตัวอักษร (Character) ไปหั่นเป็นตัวเลขได้ wut wut

เอาเป็นว่า เดี๋ยวพี่จะอธิบายละกันครับ รอดู

## การจัดเก็บตัวแปร String
Python นั้น จะเก็บข้อมูล String ไว้ในแบบ Array หรือว่าลัง(ถ้าจะให้เข้าใจง่ายๆ) โดยลังๆนึง มี character อยู่หนึ่งตัว (นั่นก็คือกล่อง)

และ โกดังคือตัวแปรที่เก็บข้อมูล String ที่มีหน้าที่เก็บลังนั่นเอง<br>
แต่ว่าโกดังนี้มีขนาดไม่จำกัดครับ โดยผู้จัดการขนาดโกดังก็คือตัว Python นั่นเอง ดังนั้นน้องๆเลยไม่ต้องสนใจเรื่องการเปลี่ยนขนาดโกดัง เหมือนหลายๆ ภาษาคอมพิวเตอร์ครับ

ใน Lecture นี้ พี่มงก็จะอธิบาย ว่าน้องๆทำอะไรกับข้อมูลประเภท String ได้บ้างนะครับ

## String Concatenation
Concatenation นั้นหมายถึงการนำ string มาแปะเข้าด้วยกัน [[Reference]](https://en.wikipedia.org/wiki/Concatenation)

น้องสามารถทำการเอา String มาแปะกันได้ โดยการใช้เครื่องหมายบวก (`+`)

ตัวอย่างเช่น
```python
text = "Hello"
text2 = "World"
print(text + text2) # Returns "HelloWorld"
```

หรือน้องๆสามารถใช้เครื่องหมาย , เพื่อทำการเอามาแปะกัน <br>
แต่ว่าจะแตกต่างจาก + นั่นคือ **เอาไปแปะแล้วมี Space ด้วย 1 ตัว**

ตัวอย่างเช่น
```python
text = "Hello"
text2 = "World"
print(text, text2) # Returns "Hello World"
```

แต่ในตัวอย่างนี้
```python
text1 = "Hello"
text2 = "World"
text3 = text1, text2 # Returns ('Hello', 'World')
```

แล้วทำไมมันไม่ได้เหมือน `print(text1, text2)` หล่ะครับ<br>
นั่นก็เพราะว่า เขียนแบบนั้น ก็หมายถึงการให้ตัวแปร `text1` และ `text2` ไปจัดเก็บอยู่ในตัวแปร `text3` นั่นเอง

แต่เอาเป็นว่า มันได้ค่าไม่เท่ากันครับ ไว้ใน lecture หน้าๆจะมาอธิบายครับ

## String และ ตัวเลข
พี่มงบอกเองไม่ใช่เหรอ ว่าเอา String มาทำอะไรกับตัวเลขไม่ได้<br>
แต่ก็ยังมีข้อยกเว้นอยู่นะครับ เมื่อเอา String มายุ่งกับ Integer ตัวอย่างเช่น
```python
text = "Kumamon"
print(text * 5) # Returns "KumamonKumamonKumamonKumamonKumamon"
```

ซึ่งการคูณแบบนี้ Python จะคิดว่าให้ทำการ copy และแปะตัว string นั้น 5 รอบ

::: tip Challenge
น้องลองคิดดูซิ ว่าถ้าพี่เขียนแบบนี้
```python
text = "Kumamon"
print(5 * text)
```
แล้วจะรันผ่าน และได้ผลลัพท์เหมือน `print(text * 5)` หรือเปล่า
:::

แล้วทำไมอันนี้ มันไม่ทำงานหล่ะครับ ???
```python
text = "kuma"
text2 = "mon"
print(text + text2 + 555)
```

มันแสดงข้อความนี้ออกมาอ่ะครับ
```text
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: must be str, not int
```

นั่นก็เพราะว่า Python นึกว่าน้องจะเอาไป Concatinate นั่นเอง ซึ่งเลข 555 นั้นไม่ใช่ String แต่เป็น Integer จึงไม่สามารถทำการ Concat ได้<br>
วิธีการแก้ไขจึงต้องแปลงค่า Integer ไปเป็น String ซะก่อน เลยได้เป็น

```python
text = "kuma"
text2 = "mon"
print(text + text2 + str(555)) # Returns kumamon555
```

### วิธีให้ตัวแปรเก็บค่า String
น้องสามารถใช้ "" เพื่อครอบตัวอักษร เพื่อบอกว่ามันเป็น String ก็ได้<br>
หรือน้องจะใช้ฟังก์ชั่น `str()` เพื่อทำการ Data Type Casting ก็ได้ครับ

ตัวอย่างการให้มันเก็บแบบ string แน่นอน
```python
text1 = "" # ขอบอกไว้ก่อนว่า Python ไม่ต้องทำการจองตัวแปรนะครับ
text2 = "Hello World"
text3 = "Not that much 555"
text4 = "12" # ค่า '12' (string) จะไม่เท่ากับ 12 (integer) นะครับ ต้องระวังให้ดี
```

---
## String array
พี่มงได้เคยอธิบายไว้ว่าตัวอักษรได้ถูกจัดเก็บเหมือนกล่อง<br>
แต่การจัดเรียงกล่องก็เป็นเรื่องสำคัญในการที่จะให้ Python นั้นเก็บข้อมูลได้เรียงตามที่น้องเอาเข้าไปตั้งแต่แรกนั่นเอง

ทำให้แต่ละกล่อง (Character) นั้น ต้องมีการระบุลำดับของตัวมันเองซะก่อน

ภายในตัวอย่างด้านล่าง พี่มงจะใช้ตัวอย่างเป็นคำว่า "@kumamon55" ครับ

ขั้นแรกก็จะต้องแตกออกมาเป็นกล่องที่ใส่ตัวอักษรได้ 1 ตัวอักษรซะก่อน<br>
น้องก็จะได้ประมาณนี้ครับ
```
| Character    | @ | k | u | m | a | m | o | n | 5 | 5 |
|--------------|---|---|---|---|---|---|---|---|---|---|
|              |   |   |   |   |   |   |   |   |   |   |
```

น้องก็จะเห็นว่าตัวอักษร '@' นั้นเป็นตัวแรก และ '5' เป็นตัวสุดท้าย

ปกติแล้ว **คนที่ไม่เก่งเขียนโปรแกรม** เค้าก็จะเรียกตัวแรกว่าตัวที่ 1 เนอะ แต่นี่มันคอมพิวเตอร์นิ ก็ต้องทำให้โลกจำ โดยการสอนคนเขียนโปรแกรมว่า **เรื่มนับ Array ที่เลข 0 ครับ**

![](https://i.redd.it/iwnqgrrbls5z.png)

เพราะอะไรหน่ะเหรอ??? [StackOverflow.com](https://stackoverflow.com/questions/7320686/why-does-the-indexing-start-with-zero-in-c) สิครับ รออะไร<br>(ขอโน้ตไว้ก่อนว่า Python นั้นเขียนมาจากภาษา C นะครับ)

หากเข้าใจแล้ว ก็จะได้ดังนี้ครับ
```
| Character    | @ | k | u | m | a | m | o | n | 5 | 5 |
|--------------|---|---|---|---|---|---|---|---|---|---|
| Array Number | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
```

## เรียกตัวอักษรเดี่ยวๆมาใช้งาน
หากน้องต้องการเอาตัวอักษร '@' มาจาก string ก็สามารถเขียนได้ดังนี้ครับ
```python
text = "@kumamon555"
print(text[0])
```

จุดที่ต้องสังเกตอยู่ที่ `text[0]` ครับ เป็นการบอกว่าจะเอาตัวที่ 0 (`[@]`) มาจากตัวแปร `text` นั่นเอง

แล้วถ้าต้องการเรียกหลายอัน เหมือนเป็นกลุ่มหล่ะ

## การเลือกตัวอักษรมากกว่า 1 ตัว
น้องสามารถเขียนเหมือนอันด้านบนหล่ะครับ แต่น้องเพื่มขั้นตอนขึ้นมาอีกนิดนึง<br>
โดยการเขียนเครื่องหมาย `:` ไปขั้นครับ

วิธีการใช้งานก็คือ [<ตัวอักษรตัวแรก> : <ตัวอักษรหลังตัวสุดท้ายที่เลือก>]

อาจจะยังไม่เก็ท ก็ดูตัวอย่างเอาละกันครับ

ตัวอย่างการใช้งาน
```python
text = "@kumamon555"
print(text[0:8])
```
ก็จะแสดงคำว่า "@kumamon" บนหน้าจอนะครับ<br>
จุดสังเกตนั่นก็คือ พี่ได้เลือกตั้งแต่ตัวที่ 0 นั่นก็คือ @ จนถึงตัวที่ 8 นั่นก็คือ 5 แต่ทำไมมันออกมาเป็น "@kumamon" หล่ะ

เอาเป็นว่ามันเป็นหลักของเค้าอ่ะครับ ระวังด้วยละกัน 😙

แต่หากว่าจะเลือกตั้งแต่ตัวแรกจนถึงตัวที่ 8 อยู่แล้หล่ะ น้องๆก็สามารถละเว้นไว้ได้<br>
ตัวอย่างเช่น
```python
text = "@kumamon555"
print(text[:8])
```
เพราะ Python ถือว่าน้องไม่ยอมบอกเอง ก็จะถึือว่าอยู่ ณ ที่ความเข้าใจเดียวกัน (default) ไปว่าต้องเรื่มจากตัวแรก

## การเลือกข้ามทุกๆ n ตัว
หากน้องต้องการที่จะเลือกเพียงบางตัว เช่นเลือกตัวแรก แล้วก็ข้าม 2 ตัว แล้วก็ค่อยเลือก<br>
น้องก็สามารถทำได้โดยการเพื่ม `:` เข้ามาอีกตัวนึง ก็จะได้เป็น
```python
text = "@kumamon55"
text[::2]
```

```python
<variable>[start:stop:step]

# Start -> ให้เรื่มตั้งแต่ตัวอักษรไหน       (Default: 0)
# Stop  -> ให้หยุดที่ตัวอักษรไหน         ( Required )
# Step  -> ข้ามตัวอักษรเมื่อครบทุกๆ x ตัว  (Default: 1)
```

### หาก Stop เป็นตัวเลขติดลบ
```python
var = "ABCD"
print(var[-1]) # Prints out "D" (D is the first one from the last)
```

### Array จริงน้อยกว่าที่เราต้องการเรียก
```python
var = "ABCD"
print(var[50]) # เกิด error เพราะว่า array ตัวที่ 50 ไม่มีจริง
```

### การ Print ตัวอักษรหลายตัว (แต่ไม่ใช่ทุกตัว)
```python
var = "ABCD"
print(var[0:2]) # Prints out "AB" (โดยเรื่มเอาจากตัวที่ 0 จนถึงตัวที่ 1 (ระวังนะครับ ข้อนี้ผิดกันเยอะมากเลย))
```

### เรื่มต้นและต่อเนื่องไป
```python
var = "My name is Kumamon, and I love eating"
print(var[4:]) # Prints out "name is Kumamon, and I love eating" (Starting from 4th array number)
```

### Start from beginning to stop
```python
var = "My name is Kumamon, and I love eating"
print(var[:7])
# Prints out "My name" (Starting from 0th array number to the 7th)
```

### Skips every
```python
var = "ABABABAB"
print(var[::2])
# Prints out AAAA (Skips after logical number hits every 2, which is B)
```

### Inverse Skips every
```python
var = "ABABABAB"
print(var[::-2])
# Prints out BBBB (Skips after logical number hits every -2, which is A)
```

----------

# Modifying Strings

NOTE: Please go take a look at Week 1. There is a few that you already know
+Python Week 1 by P’ Kumamon (I/O)

Variable Types and how to print like C

| **Use**      | %s     | %d      | %f    | %e                     |
| ------------ | ------ | ------- | ----- | ---------------------- |
| **To print** | String | Integer | Float | Scientific Significant |


### Doing it like C
```python
var = "My name is Kumamon"
print(">> %s <<" %var)
# Prints out ">> My name is Kumamon <<"
```
## String Type Manipulation

| Type      | %10s     | %-10s    | %.10s      | %-.10s     | %10.10s | %-10.-10s |
| --------- | -------- | -------- | ---------- | ---------- | ------- | --------- |
| For       | Aligning | Aligning | Cut String | Cut String | Both    | Both      |
| Alignment | Right    | Left     | Right      | Left       | Right   | Left      |

```python
text = "ABC"

print("%4s" %text)      # Prints out " ABC"
print("%-4s" %text)     # Prints out "ABC "
print("%.2s" %text)     # Prints out "AB"
print("%-.2s" %text)    # Prints out "AB"
print("%5.2s" %text)    # Prints out "   AB"
print("%-5.2s" %text)   # Prints out "AB   "
```

## Integer Type Manipulation

| Type      | %10d     | %-10d    | %.10d      | %-.10d     | %10.10d | %-10.-10d | %0.10d                          |
| --------- | -------- | -------- | ---------- | ---------- | ------- | --------- | ------------------------------- |
| For       | Aligning | Aligning | Cut String | Cut String | Both    | Both      | Aligning                        |
| Alignment | Right    | Left     | Right      | Left       | Right   | Left      | Right
(Add 0 instead of space) |

```python
number = 12345

print("%10d" %number)       # Prints out "     12345"
print("%-10d" %number)      # Prints out "12345     "
print("%.3d" %number)       # Prints out "12345"
print("%-.3d" %number)      # Prints out "12345"
print("%0.10d" %number)     # Prints out 0000012345
```

## Float Type Manipulation

| Type      | %10f     | %-10f    | %.10f      | %-.10f     | %10.10f | %-10.-10f |
| --------- | -------- | -------- | ---------- | ---------- | ------- | --------- |
| For       | Aligning | Aligning | Cut String | Cut String | Both    | Both      |
| Alignment | Right    | Left     | Right      | Left       | Right   | Left      |

```python
number = 123.4567

print("%10f" %number)       # Prints out "123.456700"
print("%-10f" %number)      # Prints out "123.456700"
print("%.2f" %number)       # Prints out "123.46"
print("%-.2f" %number)      # Prints out "123.46"
print("%10.3f" %number)     # Prints out "   123.457"
print("%-10.3f" %number)    # Prints out "123.457   "
```

## Scientific Significant Type Manipulation

```python
number = 123.4567

print("%e" %number) # Prints out '1.234567e+02'
```
----------

# Strings to ASCII
![https://i.stack.imgur.com/X4yts.png](https://i.stack.imgur.com/X4yts.png)


# String to ASCII (Decimal)
```python
print(ord('A'))         # Print out 65
print(ord('B'))         # Print out 66
print(ord('A') + 1)     # Print out 66
```

# ASCII (Decimal) to String
```python
print(chr(65))      # Print out 'A'
print(chr(65+1))    # Print out 'B'
print(chr(65+2))    # Print out 'C'

var = 65
print(chr(var)) # Print out 'A'
```

# Alters String ASCII from character
```python
print(chr(ord('A')+1)) # Print out 'B'
```

# String to change case
Convert character/text to lowercase ->          `.lower()` <br>
Convert character/text to uppercase ->          `.upper()` <br>
Swap character/text case from lower/upper ->    `.swapcase()` <br>

Check character/text is lowercase ->        `.islower()` <br>
Check character/text is uppercase ->        `.isupper()` <br>
Check character/text is a number ->         `.isdigit()` <br>
Check character/text is an alphabet ->      `.isalpha()` <br>

### Using .lower()
```python
return text.lower()
# If text = "KUMAMON", returns "kumamon"
# If text = "KuMaMoN", returns "kumamon"
# If text = "kumamon", returns "kumamon"
```

### Using .upper()
```python
return text.upper()
# If text = "KUMAMON", returns "KUMAMON"
# If text = "KuMaMoN", returns "KUMAMON"
# If text = "kumamon", returns "KUMAMON"
```

### Using .swapcase()
```python
return text.swapcase()
# If text = "KUMAMON", returns "kumamon"
# If text = "KuMaMoN", returns "kUmAmOn"
# If text = "kumamon", returns "KUMAMON"
```

### Using .isupper() & .islower()
```python
<string>.islower()
<string>.isupper()

text = "K"
return text.islower() # Returns false
return text.isupper() # Returns true

text = "k"
return text.islower() # Returns true
return text.isupper() # Returns false
```

### Using .isdigit() & .isalpha()
```python
How to use:
<input variable>.isdigit()
-> Returns True or False

<input variable>.isalpha()
-> Returns True or False

text = "12"
return text.isdigit() # Returns true
return text.isalpha() # Returns false

text = "ABC"
return text.isdigit() # Returns false
return text.isalpha() # Returns true
```

----------
# String with array counts and find
```plain
Finding character in text -> .find()
Count character in text that satisfies search query -> .count()
Finding text in array -> .index()

Count all character in text -> len()
```

### Using .find()
```python
How to use:
<variable name>.find("<character/text you want to find>")
-> Return as the lowest array number

# 1 occurence character
var = "ABCDE"
return var.find("A") # Returns 0

# 2 occurence character
var = "ABCDEAAAAA"
return var.find("A") # Returns 0

# Non occurence character
var = "ABCDE"
return var.find("F") # Returns -1

# Using more than 1 character
var = "Kumamon is happy"
return var.find("Kuma") # Returns 0

# Using more than 1 character + 2 occurrence
var = "Kumamon is happy, Kumamon is happy"
return var.find("Kuma") # Returns 0
```

### Using .count()
```python
How to use:
<variable name>.count("<character/text you want to count>")
-> Returns the amount of character count.

# 1 occurence character
var = "ABCDE"
return var.count("A") # Returns 1

# 2 occurence character
var = "ABCDEAAAAA"
return var.count("A") # Returns 6

# Non occurence character
var = "ABCDE"
return var.count("F") # Returns 0

# Using more than 1 character
var = "Kumamon is happy"
return var.count("Kuma") # Returns 1

# Using more than 1 character + 2 occurrence
var = "Kumamon is happy, Kumamon is happy"
return var.count("Kuma") # Returns 2
```

### Using len()
```python
How to use:
len(<variable you want to count character>)
Returns number of elements/character in array/text

# Using to count strings
return len("Kumamon") # Returns 7

# Using to count strings in variable
var = "Kumamon"
return len(var) # Returns 7

# Using to count elements in array
var = [11,12,13,14,15]
return len(var) # Retuns 5
```
---
# Strings to other base numeric number

### Using bin()
```python
How to use:
bin(<decimal integer>) # Built-in function. Returns the binary number (Base 2)

Example:
print(bin(12345)) # Prints out 0b11000000111001
```

### Using hex()
```python
How to use:
hex(<decimal integer>) # Built-in function. Returns the hexadecimal number (Base 6)

Example:
print(hex(12345)) # Prints out 0x3039
```

### Using oct()
```python
How to use:
oct(<decimal integer>) # Built-in function. Returns the octal number (Base 8)

Example:
print(oct(12345)) # Prints out 0o30071
```

### Convert other base to decimal
```python
number = "11000000111001"
int(number, 2) # Returns 12345 (converts from base 2 (binary) to base 10 (decimal))
```
