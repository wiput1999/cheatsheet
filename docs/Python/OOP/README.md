# Class and Object
เราต้องมาเข้าใจหลักการณ์ของ Class และ Object กันก่อน

โดย Class นั่นก็คือเหมือนกล่อง โดยทุกอย่าง (Object) ที่อยู่ในกล่องนั้น จะมีคุณสมบัติเหมือนกัน และสามารถทำการปรับแต่งด้วยการใช้วิธีที่เหมือนกัน

และสำหรับ Object ก็คือสี่งของทั่วๆไปที่อาจจะเก็บข้อมูลแบบต่างๆ

ตัวอย่าง Object ก็เช่น String ครับ มันก็คือ Object ที่เก็บข้อมูล แต่เราก็เรียกว่าข้อมูลประเภท String

โดยเราอาจจะต้องสร้าง Object โดยการบอกให้ตัวแปรนี้มีค่าเท่ากับ class นี้ เพื่อให้มันทำการจัดการและมีคุณสมบัติเหมือน class ที่สร้างมันขึ้นมา

## การสร้าง class
การสร้าง Class นั้นมีอยู่ 2 ส่วน นั่นก็คือตัว constructor และตัว method
- โดย constructor จะถูกรันเมื่ิอมีตัวแปรเข้ามาอยู่ใน class เพื่อเป็นการบอกคุณลักษณะ หรือ/และ ข้อมูล
- Method เป็นขั้นตอน (เหมือนเป็น Function) เพื่อให้ Object นั้นๆทำการเปลี่ยนแปลงค่า หรือทำการเปลี่ยนแปลงภายในได้

ตัวอย่างของ class
```python
class Kumamon: # Class needs AT LEAST 1 self (which equals to class name itself.)
    def __init__(self, name): # This function is __init__ WHICH IS REQUIRED BY CLASS. It defines all other variable name
        self.name = name + " desu" # Defining variable name to be equal to itself + desu
        
    def rename(self, new_name):
        self.name = new_name
        return
```

## Calling a class variables
```python
happy = Kumamon("Uvuvwevwevwe onyetenyevwe ugwemubwem ossas")
return happy.name # Returns "Uvuvwevwevwe onyetenyevwe ugwemubwem ossas desu"

```

## Example of function defining
```python
class Mango:
    def func(self):
        a, b = 8, 9
        return a+b

    def func2(self, x,y):
        c = self.func()
        z = x + y + c
        return z

a = Mango()
a.func2(1,1)
print(a)
```
