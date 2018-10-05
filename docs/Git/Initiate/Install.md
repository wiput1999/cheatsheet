# Installing Git

## Installing on Linux
โดยปกติแล้ว ตัว Ubuntu จะมี Git มาให้อยู่แล้ว แต่ก็จะเวอร์ชันเก่าหน่อย<br>
แนะนำว่าให้ทำการ update package ด้วยการใช้
```
sudo apt update
sudo apt upgrade
```

และลองเช็คดูว่ามี Git หรือไม่

### Using apt-get
```
# Update the version first
sudo apt update
sudo apt upgrade

# Then install the real Git
sudo apt-get install git
```

### Using Git Installer (Recommend)
สามารถเข้าไปดาวน์โหลดได้ที่​ [http://git-scm.com/download/linux](http://git-scm.com/download/linux)

---

## Installing on MacOS
### Using Xcode Developer Pack
โดยปกติแล้ว MacOS จะมี Git ติดมาให้ โดยจะดาวน์โหลดมาพร้อมกับ XCode Developer Pack โดยการเรียกใช้
```
sudo xcode-select --install
```

### Using Brew
หรือหากยังลงไม่ได้อีก หรือไม่มี ก็สามารถใช้ตัว package manager [homebrew](https://brew.sh) ได้
```shell
brew tap install git
```

### Using installer
สามารถเข้าไปดาวน์โหลดได้ที่​ [https://git-scm.com/download/mac](https://git-scm.com/download/mac)

---

## Installing on Windows
### Using installer
สามารถเข้าไปดาวน์โหลดได้ที่​ [http://git-scm.com/download/win](http://git-scm.com/download/win)

---
## Check if Git is installed
หากน้องๆมีตัว Git อยู่บน Desktop ก็ถือว่าน้องมีเรียบร้อยแล้ว อิอิ

แต่สำหรับน้องที่ใช้ CLI หรือ package manager ก็สามารถเข้า Window Powershell / Terminal แล้วพิมพ์
```
which git
```

หรือ
```
git --version
```

หากมีคำตอบกลับมาว่าเป็น Git ก็ถือว่ามีเรียบร้อยแล้ว แต่หากว่าตอบกลับมาไม่รู้จัก command นี้ก็ถือว่ายังไม่มีนาจาา

---
## Reference
[Atlassian Git - Install Git](https://www.atlassian.com/git/tutorials/install-git)