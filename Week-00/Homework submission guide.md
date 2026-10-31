# Homework Submission Guide: คู่มือการส่งงานผ่าน GitHub ด้วยระบบ Pull Request (PR)

ในฐานะที่เป็นนักศึกษาสายเทคโนโลยี การใช้งาน **Git, GitHub และ Generative AI** ให้คล่องแคล่วถือเป็นทักษะพื้นฐานที่สำคัญมาก

ในสัปดาห์ที่1  นักศึกษาได้ทดลองทำกิจกรรม **"ให้ AI ทำการ Audit และประเมินให้คะแนนคำตอบ "** ในธีม **ร้านอาหารป้าจำปีคิทเช่น** กันไปแล้ว เพื่อให้ทุกคนสามารถส่งงานเข้าสู่ระบบคลังข้อมูลกลางของวิชาเราได้ วันนี้เราจะมาเรียนรู้วิธีการส่งงานผ่านระบบ **Pull Request (PR)** กันครับ

## สิ่งที่ต้องเตรียมก่อนเริ่มส่งงาน

1. **Account GitHub** ของตนเอง
2. โปรแกรม **Git** ติดตั้งลงบนเครื่องคอมพิวเตอร์ หรือใช้งานผ่าน Git Web Interface / GitHub Desktop
3. ไฟล์ **`chat.md`** ที่บันทึกบทสนทนาระหว่างนักศึกษากับ AI ตั้งแต่ต้นจนจบ (ห้ามลบประวัติ ห้ามแก้ไขคำตอบ AI ให้สวยงามเกินจริง)

## 5 ขั้นตอนการส่งงานผ่าน GitHub (Pull Request)

ให้นักศึกษาปฏิบัติตามขั้นตอนต่อไปนี้อย่างเคร่งครัด เพื่อให้ระบบและ TA (รวมถึง AI Auditor) สามารถตรวจงานของทุกคนได้โดยไม่ตกหล่น
### ขั้นตอนที่ 1: Fork Repository ของรายวิชา
1. เข้าไปยัง URL GitHub Repository ของรายวิชาวิชาอาชีวอนามัยและความปลอดภัยที่อาจารย์แจ้งไว้
![[Pasted image 20260705115945.png]]

2. มองหาปุ่ม **"Fork"** ที่มุมขวาบนของหน้าจอ กด Fork เพื่อคัดลอกโปรเจกต์ทั้งหมดไปเป็นของตนเอง จากรูป Fork = 68 แสดงว่าทุกคนควรจะ fork ไปแล้ว

![[Pasted image 20260705121354.png]]


### ขั้นตอนที่ 2: Clone และสร้างโฟลเดอร์ส่งงาน

- ให้เตรียมโปรแกรมต่างๆ เกี่ยวกับ git รวมทั้ง editor ที่บนเครื่องให้พร้อม 
	ถ้ายังทำไม่ได้ ให้ดูคำแนะนำตามเครื่องของนักศึกษาได้เลย PC/Lab top/Mac, Tablet/iPad/Smart phone 
- ให้ทำการ Clone Repository ที่ Fork ไปแล้วลงเครื่องคอมพิวเตอร์ หรือจัดการไฟล์บน GitHub ของตนเอง
 
![[Pasted image 20260705121744.png|879]]

1. กดปุ่ม **Code** สีเขียว
2. กดปุ่ม Copy คัดลอก URL

- ในโปรแกรม terminal บนเครื่องส่วนตัว ให้สร้าง Directory ที่จะ clone ไฟล์ทั้งหมดลงมาเก็บ (ภาษา git เรียกว่า working directory)
	![[Pasted image 20260705122002.png]]

	จากรูป เราใช้  `D:\GitHubRepos\__ENGEDU\OHS2569_kosontr>` เป็นพื้นที่ทำงาน (working directory)
- ให้พิมพ์คำสั่ง   `git clone` ตามด้วย url ที่คัดลอกมา
     `git clone https://github.com/kosontr/OHS_2569.git`
 - Terminal จะดึงไฟล์จาก repo มาเก็บไว้ใน working directory  ของเรา
![[Pasted image 20260705122315.png]]

- ลองพิมพ์ `ls` เพื่อดูไฟล์ที่มี หรือพิมพ์ `cd` เพื่อเปลี่ยนเข้าไปใน directory  ย่อย
```
PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr> ls

    Directory: D:\GitHubRepos\__ENGEDU\OHS2569_kosontr

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2026-07-05    12:22                OHS_2569

PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr> cd .\OHS_2569\                                        
PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569> ls

    Directory: D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2026-07-05    12:22                Week-00
d----          2026-07-05    12:22                Week-01
-a---          2026-07-05    12:22             10 .gitignore

PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569> 
```

- ถ้าใช้ visual studio code เราจะเห็นโครงสร้าง folder ที่ clone มา
![[Pasted image 20260705122601.png]]



-  เข้าไปที่โฟลเดอร์ตามสัปดาห์ที่มอบหมาย เช่น `OHS_2569/Week-01/Homework/`
-  **สร้างโฟลเดอร์ใหม่** เป็นรหัสนักศึกษาของตนเอง เช่น `OHS_2569/Week-01/Homework/69012345/` เพื่อป้องกันไฟล์ทับซ้อนกับเพื่อนๆ

![[Pasted image 20260705122643.png]]

### ขั้นตอนที่ 3: วางไฟล์ผลงาน `Homework____chat.md`

1. นำบทสนทนาที่มีโครงสร้าง  (Prompt + คำตอบนักศึกษา + AI Audit & Rubric) และคะแนนที่ AI ประเมิน ใส่ลงในไฟล๋แยกตาม Homework ได้แก่
> Homework 1 Hazard.md --> Homework_1_Hazard_chat.md
> Homework 2 Danger.md --> Homework_2 Danger_chat.md
> Homework 3 Accident.md --> Homework_ 3 Accident_chat.md
> Homework 4 Near Miss.md --> Homework_ 4 Near_Miss_chat.md
> Homework 5 Full OHS Analysis.md --> Homework_ 5_Full_OHS_Analysis_chat.md
> Homework 6 Danger Accident and Near Miss Analysis.md --> Homework_ 6_Danger Accident_and_Near_Miss_Analysis_chat.md

2. นำไฟล์  `xxx_chat.md `ทั้งหมด  มาใส่ไว้ในโฟลเดอร์รหัสนักศึกษาที่สร้างขึ้น เช่น `OHS_2569/Week-01/Homework/69012345/`

![[Pasted image 20260705123244.png]]

3. ตรวจสอบเนื้อหาภายในไฟล์ให้แน่ใจว่าใช้รูปแบบ Markdown ที่ถูกต้อง ปราศจากแท็กแปลกปลอม

### ขั้นตอนที่ 4: Commit และ Push งานขึ้น GitHub ของตนเอง

ทำการบันทึกความเปลี่ยนแปลง (Commit) และส่งไฟล์ขึ้นไปยัง GitHub ส่วนตัวของนักศึกษาด้วยคำสั่ง:

```Bash
git status
git add .
git commit -m "Submit assignment week 01 - [รหัสนักศึกษา]"
git push origin main
```

**ตัวอย่าง**
```bash
PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Week-01/Homework/69012345/

nothing added to commit but untracked files present (use "git add" to track)
PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569> git add . 
PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569> git commit -m "Submit assignment week 01 - [69012345]"  
[main a0c5b58] Submit assignment week 01 - [69012345]
 6 files changed, 12 insertions(+)
 create mode 100644 Week-01/Homework/69012345/Homework_1_Hazard_chat.md
 create mode 100644 Week-01/Homework/69012345/Homework_2_Danger_chat.md
 create mode 100644 Week-01/Homework/69012345/Homework_3_Accident_chat.md
 create mode 100644 Week-01/Homework/69012345/Homework_4_Near_Miss_chat.md
 create mode 100644 Week-01/Homework/69012345/Homework_5_Full_OHS_Analysis_chat.md
 create mode 100644 Week-01/Homework/69012345/Homework_6_Danger_Accident_and_Near_Miss_Analysis_chat.md

PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569> git push origin main
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 32 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (11/11), 1.28 KiB | 437.00 KiB/s, done.
Total 11 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/kosontr/OHS_2569.git
 ! [remote rejected] main -> main (permission denied)
error: failed to push some refs to 'https://github.com/kosontr/OHS_2569.git'

```

**ระวัง!!!** ถ้าขึ้นแบบนี้แสดงว่า push ไม่สำเร็จ อย่าเพิ่งเลิกทำ เพราะงานจะยังไม่ถูกส่งไปยัง repo 
``` bash
 ! [remote rejected] main -> main (permission denied)
error: failed to push some refs to 'https://github.com/kosontr/OHS_2569.git'
```

ให้ไปตั้งค่า `user.name` และ `user.email` ก่อน แล้วรัน `git push origin main` อีกครั้ง

```basg
git push origin main
```

ถ้าขึ้นแบบนี้ แสดงว่าส่งงานขึ้น Github เรียบร้อย แต่งานเรายังไม่จบ เพราะมันไปอยู่แค่ repo ส่วนตัว อาจารย์ยังไม่รู้ หรืออาจจะแกล้งทำไม่เห็น

``` bash
PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569>git push origin main                             
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 32 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (11/11), 1.28 KiB | 656.00 KiB/s, done.
Total 11 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/kosontr/OHS_2569.git
   a1dec70..a0c5b58  main -> main
PS D:\GitHubRepos\__ENGEDU\OHS2569_kosontr\OHS_2569> git status                                                           
On branch main                            
Your branch is up to date with 'origin/main'. <---งานขึ้น github แล้ว

nothing to commit, working tree clean
```
### ขั้นตอนที่ 5: กดสร้าง Pull Request (PR) ส่งงาน
-  กลับมาที่หน้า GitHub Repository ของนักศึกษาเอง จะเห็นข้อความแจ้งเตือนว่ามีความเปลี่ยนแปลงเกิดขึ้น 
	`This branch is 1 commit ahead of koson/OHS_2569:main.`
- ให้กดปุ่ม **"Contribute"** และ **"Open pull request"**
2. ตรวจสอบต้นทางและปลายทาง (Base repository ต้องเป็นคลังวิชาหลัก และ Head repository ต้องเป็นของนักศึกษา)
3. ตั้งชื่อ PR ว่า: `ส่งงานสัปดาห์ที่ 1 - [รหัสนักศึกษา] [ชื่อ-นามสกุล]`
4. กด **"Create pull request"** เป็นอันเสร็จสิ้นกระบวนการ! 
