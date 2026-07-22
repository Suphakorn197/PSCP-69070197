# บันทึก Reflection การใช้ AI

ใช้ไฟล์นี้เฉพาะเมื่อมีการใช้ AI กับโจทย์ OJ ที่เป็น learning-log-required เท่านั้น

ให้ copy template นี้ แล้วเปลี่ยนชื่อไฟล์เป็น:

```text
ai_reflection.md
```

เขียน reflection นี้ด้วยคำพูดของตนเอง

ห้ามวาง AI conversation ทั้งหมด

ห้ามให้ AI เขียน reflection นี้แทนคุณ

AI อาจช่วยตรวจ grammar, formatting หรือความชัดเจนได้ หลังจากที่คุณเขียน reflection ของตนเองแล้ว

---

## 1. ข้อมูล OJ

| Item | Answer |
|---|---|
| OJ problem number/title | OJ3024 - SurprisingVote |
| OJ submission ID, if submitted |  |
| OJ status | Pass |

---

## 2. เครื่องมือ AI ที่ใช้

เขียนชื่อเครื่องมือ AI ที่ใช้

ตัวอย่าง:

```text
ChatGPT
Claude
Gemini
ChatGPT Codex / OpenAI Codex / Codex CLI
Claude Code
Other: ...
```

My answer:

```text
Gemini
```

---

## 3. การตรวจสอบนโยบายการใช้ AI ของรายวิชา

ตอบหัวข้อนี้อย่างซื่อสัตย์

หัวข้อนี้ยืนยันว่าคุณได้ทำตาม AI workflow ของรายวิชาก่อนและระหว่างใช้ AI

| Statement | Yes / No / Not Applicable | Short note |
|---|---|---|
| I read the relevant workflow before using AI. | Yes |  |
| I used `instructions/COURSE_AI_INSTRUCTIONS.md`, `instructions/AGENTS.md`, or manually followed the course AI instructions if the tool did not support custom instructions. | Yes |  |
| I wrote my own problem understanding before asking AI for help. | Yes |  |
| I wrote my own first plan before asking AI for help. | Yes |  |
| I used AI as a coach, reviewer, debugger, or test-case helper, not as a full-answer generator. | Yes |  |

ถ้าตอบ "No" ในข้อใด ให้อธิบายเหตุผล:

```text

```

---

## 4. ฉันถาม AI ให้ช่วยอะไร

อธิบายสั้น ๆ ว่าถาม AI ให้ช่วยเรื่องอะไร

ห้ามวาง chat log ทั้งหมด

ตัวอย่าง:

- ฉันถาม AI ให้ช่วยอธิบายโจทย์ด้วยภาษาที่เข้าใจง่ายขึ้น
- ฉันถาม AI ให้ช่วย review แผนแรกของฉัน
- ฉันถาม AI ให้ช่วยหา bug ใน code
- ฉันถาม AI ให้ช่วยเสนอ test cases
- ฉันถาม AI ให้อธิบายว่าทำไม output ของฉันต่างจาก expected output

My answer:

```text
ตอนสร้างตัวแปรmin_score ตอนแรกผมเขียนแค่ว่า total_score - score_max โดยที่จริงๆต้องเป็น total_score - score_max - score_max เพราะต้องเอาคะแนนคนกลางมาลบด้วยโดยที่เราจะกำหนดให้คะแนนสูงสุดโดยที่เราจะกำหนดให้คนกลางได้คะแนนสูงสุดเท่าที่จะเป็นไปได้เพื่อหาคะแนนของคนที่ต่ำที่สุดผมจึงให้แชทช่วยอธิบายลอจิกที่ถูกต้องตรงจุดนี้
```

---

## 5. AI ช่วยให้ฉันสังเกตอะไร

เขียนว่า AI ช่วยให้คุณสังเกตอะไร

ตัวอย่าง:

- ความเข้าใจผิดเกี่ยวกับโจทย์
- condition ที่ขาดไป
- bug ในการอ่าน input
- edge case
- ปัญหา syntax ของ Python
- ปัญหา output formatting

My answer:

```text
แชทช่วยให้ผมสังเกตเห็นBu ในการคำนวณครับทำให้รู้ว่าการจะหาคะแนนต่ำสุดได้ต้องหักคะแนนสูงสุดออกไป 2 ครั้ง ไม่ใช่ครั้งเดียวนอกจากนี้แชทยังช่วยชี้ให้เห็นEdge Caseที่สำคัญคือกรณีที่ผลลัพธ์ของการลบเลขออกมาเป็นค่าติดลบ ซึ่งในความเป็นจริงคะแนนโหวตติดลบไม่ได้ผมจึงได้เรียนรู้ว่าต้องใส่เงื่อนไขดักไว้ if min_score < 0เพื่อปรับค่าให้เป็น 0 เสมอ
```

---

## 6. ฉันตรวจสอบหรือแก้อะไรด้วยตนเอง

เขียนว่าหลังจากได้รับความช่วยเหลือจาก AI คุณตรวจสอบ ทดสอบ หรือแก้อะไรด้วยตนเอง

ตัวอย่าง:

- ฉันตรวจ input format ใน OJ problem อีกครั้ง
- ฉันทดสอบ code ใน VS Code
- ฉันเปรียบเทียบ expected output กับ actual output
- ฉันแก้ loop condition ด้วยตนเอง
- ฉันไม่ใช้บางคำแนะนำของ AI เพราะไม่ตรงกับ constraints ของโจทย์
- ฉันปรับคำแนะนำของ AI ให้เป็น code ที่ฉันเข้าใจเอง

My answer:

```text
ผมตรวจสอบเรื่องเงื่อนไขif elif เผื่อในกรณีที่คะแนนจะติดลบแล้วจะปรับให้เท่ากับ0
```

---

## 7. ฉันได้เรียนรู้อะไร

เขียน 2-4 ประโยคเกี่ยวกับสิ่งที่ได้เรียนรู้จากโจทย์นี้และจากกระบวนการใช้ AI ช่วย

ให้เน้นการเรียนรู้ของตนเอง

ห้ามเขียนแค่ว่า "I learned coding" หรือ "AI helped me."

My answer:

```text
ได้เรียนรู้ว่าตอนเขียนลอจิกสมการคณิตศาสตร์ในโปรแกรมเราต้องคำนึงถึงข้อจำกัดในโลกความเป็นจริงด้วย เช่น การคำนวณหาคะแนนต่ำสุดที่ผลลัพธ์อาจออกมาติดลบแต่คะแนนจริงติดลบไม่ได ผมจึงได้เรียนรู้ว่าต้องมีการเขียนเงื่อนไขดักจับข้อผิดพลาดตรงนี้ไว้เสมอ 
```

---

## 8. คำรับรองของนักศึกษา

ตอบอย่างซื่อสัตย์

| Statement | Yes / No |
|---|---|
| I wrote this reflection in my own words. | Yes |
| This reflection describes my real AI use. | Yes |
| I checked AI's suggestions before using them. | Yes |
| I can explain my final code. | Yes |
| I did not ask AI to write this reflection for me. | Yes |
