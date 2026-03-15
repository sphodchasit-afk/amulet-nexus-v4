# 🪬 Amulet Nexus v4

ระบบจัดการพอร์ตพระเครื่องยุคใหม่ — รวดเร็ว เสถียร ด้วยขุมพลัง Supabase Real-time Database

**Live Demo:** [https://a-nx.vercel.app](https://a-nx.vercel.app)

---

## 🌟 มีอะไรใหม่ใน v4?

- ⚡ **Supabase Integration**: เปลี่ยนจาก Google Sheets มาเป็น Database แท้ๆ ทำให้โหลดข้อมูลไวขึ้น 10 เท่า
- 📸 **Direct Image Upload**: อัปโหลดรูปภาพพระเครื่องจากมือถือลง Cloud Storage ได้โดยตรง
- 📱 **PWA Ready**: ติดตั้งเป็นแอปบนมือถือได้ ลื่นไหลเหมือนแอปแท้
- 🎨 **Modern UI**: ปรับปรุงหน้าตาใหม่ในธีม Black & Gold สวยงามและใช้งานง่ายขึ้น

---

## 🚀 ฟีเจอร์หลัก

- 📊 **Dashboard**: สรุปยอดรวมราคาพระเครื่องในพอร์ต
- 📂 **Portfolio**: รายการพระเครื่องพร้อมรูปภาพและรายละเอียดที่มา
- ➕ **Smart Entry**: บันทึกข้อมูลพระเครื่องพร้อมอัปโหลดรูปผ่านกล้องมือถือ
- ☁️ **Cloud Sync**: ข้อมูลไม่หาย เปลี่ยนเครื่องใช้งานได้ทันทีผ่านบัญชี Supabase

---

## 🛠️ Stack (เทคโนโลยีที่ใช้)

- **Frontend**: Vanilla HTML5, CSS3 (Flexbox/Grid), JavaScript (ES6+)
- **Backend**: [Supabase](https://supabase.com/) (Database & Storage)
- **Deployment**: [Vercel](https://vercel.com/)
- **PWA**: Service Workers & Web Manifest

---

## 📂 โครงสร้างไฟล์

```text
ANx/
├── index.html      ← หน้าแอปหลักและระบบเชื่อมต่อ Supabase
├── sw.js           ← ระบบ Offline และ Cache v4
├── manifest.json   ← การตั้งค่าแอป PWA v4
├── vercel.json     ← การตั้งค่าความปลอดภัยของ Vercel
├── icon-192.png    ← ไอคอนแอป (Small)
└── icon-512.png    ← ไอคอนแอป (Large)
