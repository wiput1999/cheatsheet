# Installing Git
หากว่ามี Git อยู่แล้ว ก็ไม่ต้องดาวน์โหลดอีกเพื่อที่จะ update git version โดยสามารถเช็คได้[ด้วยคำสั่ง]()

## Installing on Linux
```shell
# ใช้ apt ในการดาวน์โหลด
sudo apt-get install git-all
# หรือใช้ dnf ในการดาวน์โหลด
sudo dnf install git-all
```

หรือหากยังไม่ได้อีก ให้ลองไปดู​ http://git-scm.com/download/linux

## Installing on Mac
โดยปกติแล้ว MacOS จะมี Git ติดมาให้อยู่แล้ว ไม่จำเป็นที่จะต้องดาวน์โหลดเหมือน Linux

โดยจะดาวน์โหลดพร้อมกับ Developer Pack ที่ตัว XCode ดาวน์โหลดให้เมื่อมีการพิมพ์ `git`

หรือหากยังลงไม่ได้อีก หรือไม่มี ก็สามารถใช้ตัว package manager `brew` ได้
```shell
brew tap install git
```

## Installing on Windows
Windows สามารถ download git ได้ทีี่ http://git-scm.com/download/win

## GUI-based Versioning Tool
หากว่าไม่อยากพิมพ์ command ของ Git เอง ก็สามารถดาวน์โหลดได้จากหลายที่ เช่น
- [GitHub Desktop]() (แต่ละรองรับแค่การ push Git repository ที่อยู่บน GitHub.com เท่านั้น)
- [GitKraken](https://www.gitkraken.com)
- [SourceTree](https://www.sourcetreeapp.com)

## Checking the Git version
```shell
git --version
```

# Initiate Git
โดยหากว่า project folder ใดต้องการทำการ Versioning โดยการใช้ Git ก็สามารถทำได้โดยการพิมพ์

```shell
git init
```

โดยทำแล้ว จะมีโฟล์เดอร์ `.git` ขึ้นมาเพื่อจัดการ versioning โดยใน folder นั้นจะเก็บข้อมูลเกี่ยวกับการ commit เก่าๆ และปลายทาง ว่า remote อยู่ที่ไหน และอื่นๆที่เกียวข้องกับระบบ Git

และเมื่อทำการ init แล้วก็สามารถเรื่มทำงานและเพื่มไฟล์ได้เลย
