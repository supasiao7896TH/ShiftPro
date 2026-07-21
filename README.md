# OmniShift-Ledger (ShiftPro Tracker)

แอปบันทึกกะการทำงาน คำนวณ OT / เบี้ยกะ / รายได้รายเดือน-รายปี
ทำงานเป็น **Single-file HTML** เก็บข้อมูลในเครื่องด้วย `localStorage` — เปิดไฟล์ `index.html` ในเบราว์เซอร์ได้เลย ไม่ต้องติดตั้งอะไร

## ฟีเจอร์
- บันทึกกะ (M/N), OT 1.5 / 2.0 / 3.0, เหตุผล และรายละเอียดรายวัน
- สรุปรายได้รายเดือน + กราฟ (Income breakdown / OT รายเดือน)
- Annual Dashboard สรุปรายปี (รายได้รวม, OT, วันลาพักร้อน/ลาป่วย)
- จัดการรายการเหตุผล (เพิ่ม/ลบ) เอง
- Backup / Restore เป็นไฟล์ JSON
- Dark / Light mode
- Responsive: เดสก์ท็อปเป็นตาราง, มือถือเป็นการ์ด (ออกแบบสำหรับ Samsung S26 Ultra)
- **PWA**: ติดตั้งเป็นแอปบนมือถือ/เดสก์ท็อปได้ ใช้งาน offline ได้ (service worker แคชไฟล์ทั้งหมด)

## ติดตั้งเป็นแอป (PWA)
เปิดลิงก์ผ่าน Chrome/Samsung Internet/Edge แล้ว:
- **มือถือ:** เมนู ⋮ → "เพิ่มลงในหน้าจอหลัก" (Add to Home screen) หรือกดไอคอน ⬇️ ในแอป
- **เดสก์ท็อป:** กดไอคอนติดตั้งบนแถบ address bar
ติดตั้งแล้วเปิดได้เต็มจอแบบไม่มีแถบเบราว์เซอร์ และทำงาน offline ได้

## วิธีใช้
1. เปิด `index.html` ด้วยเบราว์เซอร์ หรือ deploy ขึ้น GitHub Pages
2. ตั้งค่าเงินเดือน/เรตกะ ที่ Advanced Settings
3. กรอกข้อมูลรายวัน — ระบบ **autosave** ให้อัตโนมัติ (หรือกด 💾 / Ctrl+S)

## Deploy บน GitHub Pages
Settings → Pages → Branch: `main` / `(root)` → Save
จากนั้นเปิดที่ `https://supasiao7896th.github.io/OmniShift-Ledger/`

## หมายเหตุ
- วันหยุดราชการแยกเป็น `FIXED_HOLIDAYS` (วันที่ตายตัว ใช้ทุกปีอัตโนมัติ) และ `VARIABLE_HOLIDAYS` (จันทรคติ/ชดเชย เก็บแยกตามปี: 2025–2027 ตรวจสอบแล้ว) ปีถัดไปเพิ่มได้ที่ `VARIABLE_HOLIDAYS` เมื่อมีประกาศ ครม.

---
Developed by Supasit A.@1981 TH & AI Partner · V11.0
