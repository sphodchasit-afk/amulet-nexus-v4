# 🪬 Amulet Nexus v4

ติดตามพอร์ตพระเครื่อง · กำไร/ขาดทุน · Supabase Cloud

**Live:** https://a-nxv3.vercel.app

---

## Features

- 📊 Dashboard — ภาพรวมพอร์ต กำไร/ขาดทุน Win Rate
- 🗂 Portfolio — รายการทั้งหมด ค้นหา กรอง
- ➕ บันทึก — เพิ่มรายการพร้อมรูปภาพ (Supabase Storage)
- 📈 วิเคราะห์ — Win Rate ช่องทางที่ดีที่สุด
- ☁️ Cloud — Supabase real-time database
- 📄 Export CSV / JSON Backup / Import JSON (รองรับ v3)
- 📱 PWA — ติดตั้งบนมือถือได้

---

## Stack

- Vanilla HTML / CSS / JS (ไม่มี framework)
- Supabase (PostgreSQL + Storage)
- @supabase/supabase-js v2 (CDN)
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
├── icon-192.png    ← App icon
├── icon-512.png    ← App icon
└── README.md
```

---

## Supabase Setup

### 1. สร้างตาราง (SQL Editor)

```sql
create table amulets (
  id uuid primary key default gen_random_uuid(),
  name text not null,
  type text,
  channel text,
  trust text,
  buy_price numeric default 0,
  buy_date date,
  status text default 'held',
  sell_price numeric,
  sell_date date,
  sell_channel text,
  pressure text,
  note text,
  photos jsonb default '[]',
  created_at timestamptz default now()
);

alter table amulets enable row level security;
create policy "allow all" on amulets for all using (true);
```

### 2. สร้าง Storage Bucket

- ไปที่ **Storage → New bucket**
- ชื่อ: `amulet-images`
- ติ๊ก **Public bucket**

---

## Config (แก้ใน index.html)

| ค่า | ตำแหน่ง |
|---|---|
| `SUPABASE_URL` | บรรทัด config ใน `<script>` |
| `SUPABASE_KEY` | บรรทัด config ใน `<script>` (anon public key) |

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

## Migration จาก v3

ใช้ฟีเจอร์ **Import JSON** ในหน้า Cloud  
รองรับทั้ง format v3 (camelCase) และ v4 (snake_case) อัตโนมัติ

---

*v4 — เปลี่ยน backend จาก Google Sheets/Drive เป็น Supabase*
