# Git
Git เป็นระบบจัดการเวอร์ชั่นของไฟล์ (Version Control) 
นั่นก็คือการจัดการดูเวอร์ชั่นว่าไฟล์ถูกแก้ไขหรือไม่ และถูกแก้ไขจากอะไรมาเป็นอะไร
ทำให้น้องๆที่ต้องการทำงานกันหลายๆคน หรือทำงานแล้วอาจจะต้องกลับไปดูการแก้ไขเวอร์ชันที่แล้วนั่นเอง

โดย Version Control นั้นมีหลายยี่ห้อ หรือ หลายวิธีเหลือเกิน แต่ Git นั้นได้รับความนิยมสูงสุดก็เพราะการจัดการภายในที่ดีนั่นเอง

> Git is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development, but it can be used to keep track of changes in any set of files. As a distributed revision control system it is aimed at speed, data integrity, and support for distributed, non-linear workflows. - [Wikipedia](https://en.wikipedia.org/wiki/Git_(software))

ใน Cheatsheet นี้ก็จะเป็นการสอนการใช้งาน Git โดยการใช้ GitCLI (Command Line Interface) และก็จะใช้ Github.com มาเป็น remote หรือว่าที่จัดเก็บเวอร์ชันตรงกลางครับ

น้องๆสามารถเอาความรู้ที่ได้จากการเรียน Cheatsheet นี้ไปใช้งาน Git จากการใช้ tool หรือ server อื่นๆได้ พี่ก็จะขอแนะนำพวกนั้นไว้ [ที่นี่]() นะครับ

# Reference
- [Atlassian Git]()


## ขั้นตอนการทำงานของ Git
1. ไฟล์ถูกเพื่ม (Untracked)
2. ไฟล์เคยมีอยู่ในระบบแล้ว (Unstaged)
3. ไฟล์ถูกจดจำ (Staged)
4. ไฟล์ถูกจัดเก็บเป็นเวอร์ชั่น (Locally Commited)
5. ไฟล์ถูกจักเก็บเป็นเวอร์ชั่น และ อับโหลดขื้นส่วนกลางแล้ว (Remotely Commited)

และหลังจากนั้น ผู้ใช้งานคนอื่นๆ ก็สามารถเข้ามาทำการแก้ไขไฟล์ของเราได้อย่างปกติ โดยการ
1. ดึงจากส่วนกลางลงมาใช้งาน (Pull)
2. ทำการแก้ไข โดยเรื่มจากระดับ Unstaged
3. ทำการ Commit ขึ้นไปหา Remote

พี่มงก็จะแนะนำให้ไปอ่านตามการใช้งานตามลำดับนี้นะครับ จะได้เข้าใจการทำงานได้ดีขึ้น