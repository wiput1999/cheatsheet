# Pull from Fork
หากว่าบางครั้ง เราต้องการที่จะดึง commit ของ repository หลักเข้ามาสู่ forked repository ของเรา

ก็สามารถทำได้โดยการเพื่ม [**upstream**]()
```shell
git remote add upstream <original repository>
```

แล้วก็สามารถดึง (fetch) ของ upstream ได้โดยการ
```shell
git fetch upstream
```

ในขณะนี้ ตัว Git ก็ได้รู้ว่ามี upstream ใหม่แล้ว ก็สามารถ pull ปกติได้
```shell
git merge upstream/master master
```

หรือจะทำการ rebase ก็ได้
```shell
git rebase upstream/master
```
