![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/150px-Git-logo.svg.png)

## Initiate Git
การเรื่มใช้งาน Git ในครั้งแรก
* [ดาวน์โหลด Git](Git/Initiate/Install.md)
* [สร้าง Git Directory ใหม่ (Git Init)](Git/Initiate/CreateGit.md)
* [สร้าง Git Repository ใหม่ใน GitHub.com](Git/Initiate/CreateRepo.md)
* [ดาวน์โหลด (Clone) Repository มาจาก GitHub.com (Git Clone)](Git/Initiate/CloneRepo.md)

## Git Flow
การทำงาน หรือ โฟลว์การทำงานของ Git
* [โฟลว์การทำงานหลัก](Git/Flow/)
* [สร้าง Pull Request](Git/Flow/PullRequest/)
* [รีวิว Pull Request ใหม่](Git/Flow/PullRequest/Revision.md)
* [เลือกวิธีการ Merge Pull Request](Git/Flow/PullRequest/Method.md)

## Commiting
การส่ง Version (หรือการทำ Checkpoint) ให้กับไฟล์
* [เพิ่มไฟล์มาทำ Versioning (Git Add)](Git/Commiting/git-add.md)
- [ตั้งให้ไม่สนใจการทำ Versioning (Git Ignore)](Git/Commiting/git-ignore.md)
- [ยกเลิกการทำ Versioning (Git Rm)](Git/Commiting/git-rm.md)
- [สร้าง Commit ใหม่ (Git Commit)](Git/Commiting/git-commit.md)

## Resetting
- [ยกเลิกการแก้ไขไฟล์เดียว (Git Reset HEAD)](Git/)
- [ยกเลิกการแก้ไขไฟล์ทั้งหมด (Git Reset --hard)](Git/)

## Origin Setup
การตั้งค่าปลายทางที่จัดเก็บไฟล์รวม
- [รู้จักความหมายของ Origin](Git/)
- [ตั้งค่า Origin](Git/Origin/Setup.md)
- [เปลี่ยน Origin ใหม่](Git/Origin/Remap.md)
- [เพื่ม commit มาจาก origin อื่น](Git/Origin/MultipleOrigin.md)

## Pushing
การส่ง Version (Commit) ขึ้นปลายทาง
- [Introduction (Git Push)](Git/Pushing/)
- [การ Push โดยที่ปลายทางไม่เคยมี branch นั้นมาก่อน (Git Push --set-origin origin)](Git/)

## Pulling
การอับเดท (การดึง) ไฟล์และเวอร์ชั่นมาจากปลายทาง
- [Introduction (Git Pull)](Git/Pulling/)

## Update Repository
- [(Git Fetch)](Git/)
- [ความแตกต่างระหว่าง Fetch และ Pull](Git/)

## Branching
การดูแลสายการทำงาน
- [ดู branch ที่มีอยู่ในปัจจุบัน (Git Branch)](Git/)
- [สร้าง branch ใหม่ (Git Branch -b)](Git/Branching/CreateBranch.md)
- [รวม branch มาเป็นเส้นเดียวกัน (Git Merge)](Git/Branching/PullBranch.md)
- [ลบ branch ในเครื่อง (Git Branch -D)](Git/)
- [ดูความแตกต่างของแต่ละ branch (Git Branch Diff)](Git/Branching/DiffBranch.md)
- [เปลี่ยนสายให้กับ Commit ด้วย Cherry Picking](Git/Branching/CherryPick.md)

## Handling Conflicts
การแก้ไขการทำงานของ Git
- [Introduction](Git/Conflicts/)
- [Origin ไม่มี branch อยู่]
- [Merge เกิด Conflict]
