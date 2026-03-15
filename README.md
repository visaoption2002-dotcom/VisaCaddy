# VisaCaddy Web

เว็บไซต์บริการกด Username & Password สำหรับ Work and Holiday Visas ไทย-ออสเตรเลีย (WAH) และ Working Holiday Scheme ไทย-นิวซีแลนด์ (WHS)

## 📁 โครงสร้างโปรเจกต์

```
VisaCaddy/
├── index.html          # หน้าแรก (Landing Page)
├── about_wah.html      # เกี่ยวกับ Work and Holiday Visas ไทย-ออสเตรเลีย (WAH)
├── faq.html            # คำถามที่พบบ่อย
├── resite_photo.html   # เครื่องมือปรับขนาดภาพ
└── assets/             # ไฟล์ภาพและ assets
    ├── images/         # รูปภาพหลักของเว็บไซต์
    └── favicon/        # favicon + manifest
```

## 🎨 เทคโนโลยีที่ใช้

- **HTML5** + **CSS3** (Vanilla)
- **JavaScript** (Vanilla)
- **Google Fonts**: Inter, Space Grotesk, Playfair Display, Lato
- **Cropper.js** (สำหรับหน้า resite_photo)

## ✅ To-Do List (Updated: 2026-03-07)

### ✅ ทำแล้ว (Completed)
- [x] ตั้งค่า favicon และ manifest ครบทุกหน้า (`index.html`, `about_wah.html`, `faq.html`, `resite_photo.html`)
- [x] เพิ่ม Open Graph + Twitter meta tags ครบทุกหน้า
- [x] สร้างหน้า `faq.html` พร้อมหมวดหมู่คำถามและระบบค้นหา
- [x] สร้างหน้า `resite_photo.html` พร้อมเครื่องมือปรับขนาดภาพ
- [x] **[NEW]** ปรับปรุงภาษาในหน้า `faq.html` ทั้งหมดให้เป็นภาษาเขียนที่สุภาพ เป็นทางการ และเป็นระเบียบ (เปลี่ยนคำสรรพนาม, เปลี่ยนคำลงท้ายเป็น "ครับ")
- [x] **[NEW]** ออกแบบโลโก้ใหม่และปรับใช้ Brand Identity ล่าสุด (Icon Size: 176px, Gap: 0px)
- [x] **[NEW]** สร้างชุดไฟล์สคริปต์สำหรับการ Export โลโก้คุณภาพสูง (`export_logo_locked.py` และ `Mainlogo.html` สำหรับใช้ในห้องแล็บ)

### 🔥 ต้องทำต่อ (Priority)
- [ ] ติดตั้งโลโก้ใหม่เข้าระบบ (นำโลโก้ที่เพิ่ง Export มาแทนที่โลโก้เดิมใน Navbar และ Footer ของทุกหน้า)
- [ ] อัปเดตเนื้อหา `about_wah.html` ให้เป็นข้อมูล WAH 2026 ทั้งหมด (ปัจจุบันยังมีข้อความปี 2025)
- [ ] ตรวจความถูกต้องข้อมูล WAH ไทย-ออสเตรเลีย / WHS ไทย-นิวซีแลนด์ ในหน้า `about_wah.html` อีกครั้งเทียบประกาศล่าสุด
- [ ] ทดสอบ responsive บนอุปกรณ์จริง (mobile/tablet/desktop) โดยเน้นที่ Navbar ที่ใส่โลโก้ใหม่

### 🔧 Technical
- [ ] Optimize รูปภาพใหม่ๆ ใน `assets/images/` เป็น WebP/AVIF เพื่อลดขนาดไฟล์
- [ ] นำไฟล์สคริปต์ Python สำหรับ Export โลโก้ ไปรวมหรือลบออกหากใช้งานเสร็จแล้ว เพื่อความสะอาดของโปรเจกต์
- [ ] ทดสอบ flow ของ `resite_photo.html` แบบ end-to-end (อัปโหลด -> ครอป -> ดาวน์โหลด) อีกครั้ง

### 🚀 Deployment
- [ ] เปิดใช้งาน Cloudflare หรือบริการอื่นๆ เพื่อจัดการเรื่อง Cache และ Security
- [ ] Deploy production และตรวจ sanity check หลัง deploy (ตรวจเช็ค SSL Certificate)

### 🎯 Optional
- [ ] เพิ่ม Google Analytics / Plausible
- [ ] เชื่อมต่อปุ่ม LINE Official ให้ทำงานครอบคลุมทุกจุดในหน้าเว็บไซต์

## 📝 Changelog

### 2026-03-07
- ✅ ปรับปรุงหน้า `faq.html` : เปลี่ยนภาษาพูดเป็นภาษาเขียนแบบเป็นทางการ และปรับสรรพนามให้สม่ำเสมอทั้งหน้า
- ✅ พัฒนา **Logo Generator Lab** : และทำการ Export โลโก้วางโครงสร้างขนาด Icon, Wordmark, Subtitle เสร็จสมบูรณ์
- ✅ ลบไฟล์แล็บชั่วคราว (`Mainlogo.html`, `visacaddy-brand.html`) ออกจาก Workflow หลักแล้ว

### 2026-02-12
- ✅ อัปเดตรูป `about_wah.html` (hero + feature) และย้ายไฟล์ไป `assets/images/` พร้อมตั้งชื่อใหม่
- ✅ ล้าง path รูปเก่าที่ไม่ใช้งาน (`old_vertion/...`) ออกจากหน้า `about_wah.html`

### 2026-02-01
- ✅ ลบโฟลเดอร์ `reserve/` และ `main/` (ไฟล์เวอร์ชันเก่าที่ไม่ใช้แล้ว)
- ✅ ทำความสะอาดไฟล์ขยะเรียบร้อย
- ✅ สร้างโครงสร้าง `assets/` พร้อมหมวดหมู่

## 🚀 วิธีใช้งาน

1. เปิด `index.html` ในเบราว์เซอร์
2. หรือ deploy ขึ้น web server

---

© 2026 VisaCaddy. All rights reserved.




Cancel25022026.
