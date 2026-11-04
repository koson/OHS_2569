# รูปแบบแนวทางปฏิบัติเพื่อป้องกันอุบัติเหตุ (Accident Prevention Action Patterns)

**วิชา:** OCCUPATIONAL HEALTH AND SAFETY (อาชีวอนามัยและความปลอดภัย)  
**สัปดาห์ที่:** Week 09  
**รหัสนักศึกษา:** 69030091  
**ชื่อ-นามสกุล:** นายทยากร จิตรมาตร  
**ตอนเรียน:** Section 1  

---

## 1. การประสานความร่วมมือระหว่าง Engineer (E) และ Supervisor (S)

```mermaid
graph LR
    subgraph Engineer["วิศวกร (Hardware / System Focus)"]
        E1["ออกแบบ Machine Guarding"]
        E2["คำนวณระบบระบายอากาศ LEV"]
        E3["จัดทำผังกระบวนการ LOTO"]
    end

    subgraph Supervisor["หัวหน้างาน (People / Behavior Focus)"]
        S1["สื่อสาร Toolbox Talk หน้างานทุกเช้า"]
        S2["สังเกตพฤติกรรมความปลอดภัย BBS"]
        S3["ตรวจประเมิน Safety Patrol"]
    end

    Engineer <--> Supervisor
```

---

## 2. ลำดับขั้นการควบคุมอันตราย (Hierarchy of Controls in Practice)

1. **Elimination:** กำจัดขั้นตอนที่มีความเสี่ยงสูงออกจากสายการผลิต
2. **Substitution:** เปลี่ยนสารเคมีไวไฟเป็นสารเคมีไม่ติดไฟ
3. **Engineering Controls:** ติดตั้งม่านแสงนิรภัยและระบบอินเตอร์ล็อก
4. **Administrative Controls:** กำหนดคู่มือ SOP และหมุนเวียนงานลดความล้า
5. **PPE:** อุปกรณ์คุ้มครองความปลอดภัยส่วนบุคคล (เป็นเกราะด่านสุดท้าย)

---

## 3. วงจร PDCA เพื่อการปรับปรุงอย่างต่อเนื่อง

```mermaid
graph TD
    Plan["Plan: ชี้บ่งอันตรายและประเมินความเสี่ยง (JSA / Risk Assessment)"] --> Do["Do: ดำเนินมาตรการวิศวกรรมและอบรม SOP"]
    Do --> Check["Check: ตรวจประเมิน Safety Audit และสถิติ Near-Miss"]
    Check --> Act["Act: ปรับปรุงแก้ไขและยกระดับมาตรฐานความปลอดภัย"]
    Act --> Plan
```

> 📌 **บทสรุป:** อุบัติเหตุในโรงงานจะลดลงจนเป็นศูนย์ (Zero Accident) ได้ ต้องอาศัย **วิศวกรที่ออกแบบระบบให้ผิดพลาดยาก (Safe Hardware)** ร่วมกับ **หัวหน้างานที่สร้างทีมให้ปฏิบัติตามมาตรฐานอย่างมีวินัย (Safe Behavior)**