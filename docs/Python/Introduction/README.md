# Introduction to Python
สวัสดีครับ พี่ชื่อพี่คุมะมง วันนี้พี่จะมาสอนน้องเขียนโปรแกรมตั้งแต่ลง Python ยันเขียนโปรแกรมสวัสดีชาวโลกเลยนะครับ

## What is Python
น้องอาจจะยังสงสัย ว่ามันคืออะไรอ่ะ Python

Python เป็นภาษาคอมพิวเตอร์ที่ให้น้องสามารถกำหนดว่าให้คอมพิวเตอร์มันทำอะไรบ้าง ซึ่งการเรียนที่คณะ IT และวิชา Problem Solving in IT นี้ เราใช้ Python เพราะว่ามันเข้าใจง่าย และน้องก็ "ไม่ต้องเสียเวลา" เพื่อมาแก้บัคอะไรให้มากมาย เพราะอ่านง่าย อิอิ

และ Python นั้นเป็นภาษาที่รองรับระบบปฎิบัติการเยอะแยะไปหมด ทำให้มันแพร่หลาย และถูกนำไปใช้งานในหลายๆวิธีเลย

## Obtaining Python
เนื่องจากว่า Python นั้นมีหลาย platform มาก ทำให้นักพัฒนาได้เปิดให้น้องๆ ดาวน์โหลด Python ลงเครื่องนะครับ<br>
โดยพี่จะเรียงลำดับจากความยากง่ายให้แล้วกันครับ

**Methods to obtain Python3**<br>
- Download Installer มาจาก Python.org (แนะนำที่สุด)
- Download Installer มาจาก Anaconda.com
- Download โดยการใช้ HomeBrew (สำหรับ macOS)
- Download โดยการใช้ apt-get

### Download Installer มาจาก Python.org
น้องๆสามารถดาวน์โหลดตัว Python + Python IDE (IDLE) ได้ที่เว็บไซต์ของ Python.org ได้เลยครับ<br>
ดาวน์โหลดได้ที่นี่ครับ [https://www.python.org/downloads/](https://www.python.org/downloads/)

โดยให้น้องดาวน์โหลดเวอร์ชันล่าสุด โดยเวอร์ชั่นล่าสุดจะปุ่มสีเหลืองตามภาพก็ให้กดเพื่อดาวน์โหลด Python ลงเครื่องของน้องๆครับ

โดยเราจะใช้เวอร์ชั่นของ Python เป็นเวอร์ชั่น 3 นะครับ (ไม่ใช่ 2)

![](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fopensourceforu.com%2Fwp-content%2Fuploads%2F2016%2F09%2FFigure-1-Python-download-page-from-the-official-portal.jpg&f=1)<br>
ตามภาพ น้องจะเห็นได้ว่าปุ่มดาวน์โหลด Python เป็น version 3.5.2 <br>
**ดังนั้น น้องก็ไปกดปุ่มสีเหลืองเพื่อดาวน์โหลดนะครับ (รู้สึกว่าจะเขียนเป็นเวอร์ชั่น 3.6.2 แล้ว)**

แล้วก็กด install มันครับ และก็กด Next ยาวๆไป

### Download Installer มาจาก Anaconda.com
น้องๆ สามารถดาวน์โหลด Python ได้จากทาง Anaconda ครับ 

ข้อดีอย่างนึงของการทำแบบนี้นั่นคือ Conda (เป็นตัวจัดการ Python ของ Anacoda) จะทำการอับเดทเวอร์ชันให้น้องๆ ให้เป็นเวอร์ชั่นล่าสุดอย่างอัตโนมัติครับ ไม่จำเป็นที่จะต้องไปลงใหม่เหมือนกับวิธีแรก

แต่ข้อเสียจะอยู่ที่ว่ามันไม่มี IDLE ให้อ่ะสิครับ พี่มงเลยแนะนำว่าให้โหลดถ้าน้องๆจะเอาไปใช้กับการเรียน Data Analysis หรือต้องการจะไปเป็น Data Scientist ครับ เพราะว่า tools เค้าพร้อมจริงๆ และใช้งานง่ายด้วย

### Download โดยการใช้ HomeBrew (สำหรับ macOS)
หรือสำหรับน้องๆที่อยากท้าทายตัวเอง และอยากใช้ Python บน command line ก็สามารถใช้ Homebrew ในการจัดการหลายๆอย่างให้น้องครับ ดีงามโคตรๆ


หากน้องยังไม่มี Homebrew บนเครื่อง ก็ให้พิพม์บรรทัดด้านล่างไปด้วยนะครับ
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

และทำการพืิมพ์คำสั่งพวกนี้หลังจากทำการติดตั้ง HomeBrew เรียบร้อยแล้ว
```
brew doctor
brew install python
brew doctor
```

## Is Python in your computer?
สำหรับน้องที่ใช้ MacOS หรือ Linux Distributions ทั้งหลาย น้องสามารถเช็คว่ามี Python ในเครื่องแล้วหรือยัง โดยการพิมพ์
```
python3
```
ผ่านทาง Terminal ครับ

และสำหรับน้องๆที่ใช้ Windows ถ้าเห็น IDLE อยู่บน desktop (หรือที่น้องเก็บมันไว้) ก็ถือว่าดาวน์โหลดเรียบร้อยแล้วครับ โดยปกติแล้วจะมีเขียนเวอร์ขั่นของ Python กำกับที่บน IDLE ด้วยครับ (เช่น IDLE 3.6.2)

## Welcome to IDLE
IDLE คือ IDE (Integrated Development Environment) ของ Python เอง ซึ่งมันก็จะแตกต่างกับตัว Text Editor อื่นๆ (เช่น Atom, Sublime Text, VS Code) นั่นก็คือมันใช้งานง่ายกว่า และก็สามารถกด `F5` (สำหรับน้องๆที่ใช้ Windows) เพื่อทำการรันโปรแกรมได้เลย หรือกดปุ่มบนคีย์บอร์ดเพื่อรันโปรแกรม (script) ที่น้องเขียนได้เลย

โดยเปิดตัว IDLE ขึ้นมาแล้ว น้องๆก็จะเห็นหน้าต่างที่หน้าตาคล้ายๆ command line / shell ของ Python ตามภาพ

![](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fi.stack.imgur.com%2Fbz1qE.jpg&f=1)<br>
หน้าต่าง IDLE

::: warning
สำหรับน้องๆที่โหลด Python โดยการใช้ วิธีอื่นนอกจากวิธีแรก<br>
น้องๆอาจจะไปทำเหมือนวิธีที่ 1 แต่ดาวน์โหลดเพียง IDLE 

หรือลอง Google ดูครับว่ามีวิธีดาวน์โหลดผ่าน `apt-get` หรือไม่
:::

## Welcome to Python Shell
::: warning
สำหรับน้องที่ดาวน์โหลด Python มาโดยการใช้ Homebrew หรือมีบนเครื่องแล้ว
:::

ตัว Python บน Terminal ก็สามารถเรียกได้โดยการพิพม์
```
python3
```
และหน้าจอของน้องๆก็จะเป็นดังภาพ

หรือน้องๆที่ใช้ Windows ก็สามารถเขียนภาษา Python โดยใช้ shell ได้เหมือนกัน โดยการกดเข้าโปรแกรม Python Shell ก็จะได้ผลลัพท์เช่นเดียวกัน

![](https://images.duckduckgo.com/iu/?u=https%3A%2F%2Fraphaelmarques.files.wordpress.com%2F2010%2F03%2Fterminal-python.png&f=1)

## Playing with Python
ใน lecture นี้ พี่มงจะสอนวิธีทั่วๆไปก่อนเนอะ เช่นสวัสดีชาวโลกให้หน่อย อะไรแบบนี้<br>
พี่จะให้น้องสร้างไฟล์ Python (.py) และเอาไฟล์นั้นไปรันนะครับ

ขั้นตอนแรกให้น้องสร้างไฟล์ใหม่ก่อน โดยการกด File -> New File และน้องๆก็จะเห็นหน้าต่างนี้ขึ้นมา

![](https://images.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.w3resource.com%2Fw3r_images%2Fpython-idle-new-window.png&f=1)<br>
ภาพด้านบนเป็นหน้าต่างเขียนโปรแกรม Python น้องสามารถเขียนโปรแกรม Python ในนั้นได้เลยครับ

และก็ให้น้องๆลองพิมพ์ 
``` python
print("Hello World")
```
ในหน้า Text Editor ของ IDLE และน้องก็กดเซฟไฟล์ (Ctrl + S สำหรับ Windows และ Cmd + S สำหรับ MacOS + Linux)

และก็เข้าตรงแท็บที่เขียนว่า "Run" และกด "Run Module" (หรือกด F5 สำหรับน้องๆที่ใช้ Windows) เพื่อรันโปรแกรมนะครับ

น้องก็จะเห็นว่า Python เขียนอะไรกลับมา

::: tip
สำหรับน้องๆที่ยังไม่เข้าใจว่า `print()` คืออะไร มันก็คือวิธีการแสดงผลลัพท์บนหน้าจอให้น้องนั่นเอง
:::

ง่ายใช่มั้ยหล่ะ อิอิ

---
<center>Created by P'Kumamon IT14</center>



