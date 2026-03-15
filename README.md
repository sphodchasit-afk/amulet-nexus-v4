# 🪬 Amulet Nexus v3

ติดตามพอร์ตพระเครื่อง · กำไร/ขาดทุน · Google Sheets & Drive

**Live:** https://a-nx.vercel.app

---

## Features

- 📊 Dashboard — ภาพรวมพอร์ต กำไร/ขาดทุน Win Rate
- 🗂 Portfolio — รายการทั้งหมด ค้นหา กรอง
- ➕ บันทึก — เพิ่มรายการพร้อมรูปภาพ
- 📈 วิเคราะห์ — Win Rate ช่องทางที่ดีที่สุด
- ☁️ Cloud — Google Sheets sync + Drive รูปภาพ
- 📄 Export CSV / JSON Backup
- 📱 PWA — ติดตั้งบนมือถือได้

---

## Stack

- Vanilla HTML / CSS / JS (ไม่มี framework)
- Google Sheets API v4
- Google Drive API v3
- Google OAuth 2.0 (GSI)
- Vercel (static hosting)
- PWA (Service Worker + Web Manifest)

---

## Files

```
ANx/
├── index.html      ← แอปทั้งหมด
├── sw.js           ← Service Worker (PWA + offline)
├── manifest.json   ← PWA manifest
├── vercel.json     ← Vercel headers + rewrites
├── icon-192.png    ← App icon (ใส่เอง)
├── icon-512.png    ← App icon (ใส่เอง)
└── .gitignore
```

---

## Config (แก้ใน index.html)

| ค่า | ตำแหน่ง |
|---|---|
| `GOOGLE_CLIENT_ID` | บรรทัด config ใน `<script>` |
| `SPREADSHEET_ID` | บรรทัด config ใน `<script>` |
| `SHEET_NAME` | บรรทัด config ใน `<script>` |

---

## Deploy

1. Push ขึ้น GitHub
2. Import repo ใน [vercel.com](https://vercel.com)
3. Deploy — ไม่ต้องตั้งค่าอะไรเพิ่ม

---

## Workflow แก้โค้ด

```
แก้กับ Claude → ดาวน์โหลด → Acode → paste index.html → commit → Vercel auto-deploy ~30s
```

---

*v3 — ตัด Flo Finance ออกชั่วคราว เพิ่มกลับใน v4*
