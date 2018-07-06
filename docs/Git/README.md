# Git
Git เป็นระบบจัดการเวอร์ชั่นของไฟล์ (Version Control) โดยมีการจัดระเบียบข้อมูลด้วยการใช้ Git

ตัว Git เป็น Open Source ของ GitHub

> Git is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development, but it can be used to keep track of changes in any set of files. As a distributed revision control system it is aimed at speed, data integrity, and support for distributed, non-linear workflows. - [Wikipedia](https://en.wikipedia.org/wiki/Git_(software))

## ขั้นตอนการทำงานของ Git
1. ไฟล์ถูกเพื่ม (Untracked)
2. ไฟล์เคยมีอยู่ในระบบแล้ว (Unstaged)
3. ไฟล์ถูกจดจำ (Staged)
4. ไฟล์ถูกจัดเก็บเป็นเวอร์ชั่น (Locally Commited)
5. ไฟล์ถูกจักเก็บเป็นเวอร์ชั่น และ อับโหลดขื้นส่วนกลางแล้ว (Remotely Commited)
6. ดึงจากส่วนกลางลงมาใช้งาน (Pull)

ซึ่งแต่ละขั้นตอนมีหลักการแตกต่างกัน เพราะทำหน้าที่แยกกัน

โดยทุกอย่างเรื่มต้นจากการ [ดาวน์โหลด Git](Initiate/install.md) และทำการ[สร้าง Git Repository](Initiate/git-init.md)

## Commiting
- [Git Add](Commiting/git-add.md)
- [Git Ignore](Commiting/git-ignore.md)
- [Git Remove](Commiting/git-rm.md)
- [Git Commit](Commiting/git-commit.md)
## Pushing
- [Introduction](Pushing/)
## Pulling
- [Introduction](Pulling/)
## Branching
- [Create branch](Branching/CreateBranch.md)
- [Pull branch](Branching/PullBranch.md)
- [Check branch difference](Branching/DiffBranch.md)

## Merging branch
- [Introduction](Branching/MergeBase/)
- [Pull Request](Branching/MergeBase/PullRequest.md)
- [Merge Request](Branching/MergeBase/MergeRequest.md)
- [Squash and Rebase](Branching/MergeBase/RebaseRequest.md)

## Handling Conflicts
- [Introduction](Conflicts/)
