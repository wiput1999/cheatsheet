# Contribution Guidelines
เรายินดีต้อนรับให้นักพัฒนา หรือเพื่อนๆที่ต้องการช่วยเหลือในการพัฒนา cheatsheet อันนี้ โดยเราก็ได้สร้างกฎเกณฑ์เพื่อให้ผม ([@sagelga](https://github.com/sagelga)) ได้ทำการเช็คและนำเนื้อหาที่ท่านเอาเข้ามาออกสู่สาธารณะ

Welcome all developers to create a Pull Request for new features and more documentation on this repository. I ([@sagelga](https://github.com/sagelga)) created this guidelines to make me check and make a pull request faster.

## Branch Overview
โดย branch ของ repository เราจะมีการจัดการดังนี้

Our branch management on this repository look like this
```
master        
For major (or stable) release

↑

develop             
For development + hotfix release

↑

python  
For Python document development

↑

python/your_username 
This is your branch, that do works on Python document
```

## How to contribute
- ทำการ Fork ตัว repository นี้
- สร้าง branch ใหม่ จากการแตกออกมาจาก branch ภาษาต่างๆ (เช่น Python) โดยตั้งชื่อ branch เป็นชื่อภาษาตามด้วย username ของท่านเอง (ตัวอย่างเช่น หากว่า username คือ sagelga ก็ให้สร้าง branch ใหม่เป็นชื่อ python/sagelga)
- แก้ไข หรือ เพื่มใน branch ใหม่ของท่านเอง และทำการ Pull/Push ปกติ
- หากว่าท่านต้องการส่งการแก้ไขของท่าน ก็ให้สร้าง Pull Request มาโดยตั้ง merge ที่ branch ของภาษานั้นๆ
- รอเพื่อให้งานของท่านนั้่นถูกตรวจสอบ
- หากได้รับการอนุมัติ งานของท่านก็อาจจะไปอยู่ที่ branch เหนือกว่า

## Commit Log
```
{Log Type} {Description}
```

For `{Log Type}`
- Use `+` for additions
- Use `+-` for modifications
- Use `-` for deletions

Example for Commit Log
```
+ Create Python/Dictionary page

+- Edit Python/IO page

- Remove .DS_File from Python/ folder
```