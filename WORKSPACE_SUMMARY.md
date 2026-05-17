# สรุป Workspace: CTF

เอกสารนี้สรุปไฟล์ทั้งหมดใน workspace `CTF` เพื่อใช้เป็นข้อมูลประกอบการดูแลเว็บ static บน GitHub Pages

## ภาพรวมโปรเจกต์

- ประเภทโปรเจกต์: Static website แบบ HTML ล้วน
- ภาษาเนื้อหา: ไทยเป็นหลัก พร้อมคำศัพท์ด้าน Network / CTF เป็นภาษาอังกฤษ
- โครงสร้างไฟล์: ทุกหน้าอยู่ที่ root ของ repository
- Entry point สำหรับ GitHub Pages: `index.html`
- Assets ภายนอก: Google Fonts และลิงก์อ้างอิงเครื่องมือ CTF ภายนอก
- Assets ภายใน: ไม่พบไฟล์ CSS, JavaScript, รูปภาพ หรือ asset แยกจาก HTML

## รายการไฟล์ทั้งหมด

| ไฟล์ | บทบาท | สถานะบนเว็บ |
| --- | --- | --- |
| `index.html` | หน้าแรก / สารบัญหลักของเว็บ | ใช้เป็นหน้าแรกของ GitHub Pages |
| `packets-and-frames-th.html` | บทเรียน Network Fundamentals เรื่อง Packets & Frames | เปิดจากหน้าแรกได้ |
| `dns-in-detail-th.html` | บทเรียนเรื่อง DNS in Detail | เปิดจากหน้าแรกได้ |
| `extending-your-network-th.html` | บทเรียนเรื่อง Extending Your Network | เปิดจากหน้าแรกได้ |
| `ctf-vol1.html` | คู่มือ CTF Collection Vol 1 และเตรียมสอบ CTF | เปิดจากหน้าแรกได้ |

## โครงสร้างการนำทาง

หน้า `index.html` ทำหน้าที่เป็น hub กลางและลิงก์ไปยังทุกหน้า HTML ใน workspace ด้วย relative path:

- `packets-and-frames-th.html`
- `dns-in-detail-th.html`
- `extending-your-network-th.html`
- `ctf-vol1.html`

ทุกหน้า HTML มี header/menu สำหรับข้ามไฟล์หลักใน workspace แล้ว จึงสามารถกดไปกลับระหว่างบทเรียนและคู่มือ CTF ได้โดยไม่ต้องกลับผ่าน browser back button

ลิงก์แบบ relative path เหมาะกับ GitHub Pages project site ที่เปิดผ่าน `https://panuwatsopwork.github.io/CTF/` เพราะ browser จะ resolve ไฟล์จาก root ของ project site เดียวกัน

## รายละเอียดไฟล์

### `index.html`

หน้าแรกของเว็บและเป็นสารบัญหลักสำหรับ GitHub Pages

- Title: `Network Fundamentals - สารบัญบทเรียน CTF`
- Theme: dark navy gradient, orange accent, card layout, ฟอนต์ Sarabun และ Fira Code
- Layout ปัจจุบัน:
  - Sticky navigation ด้านบนสำหรับไปยัง section และหน้า HTML สำคัญ
  - Hero header สีส้มเดิมของเว็บ
  - Intro อธิบายเส้นทางการเรียน
  - เมนูลัดไปยังทุกหน้า
  - กลุ่มบทเรียน Network Fundamentals
  - กลุ่ม CTF Collection และเตรียมสอบ
  - Note สำหรับ GitHub Pages
- ข้อสำคัญ: หน้าแรกใช้ relative links ทั้งหมด จึงเหมาะกับ GitHub Pages ที่ใช้ `index.html` เป็น entry point
- Mobile: เมนูและ card layout ปรับลงจอเล็ก โดยเมนูเลื่อนแนวนอนได้เมื่อพื้นที่ไม่พอ

### `packets-and-frames-th.html`

บทเรียนพื้นฐานเรื่องการส่งข้อมูลผ่านเครือข่าย

- Title: `Packets & Frames - สื่อการสอน Network Fundamentals`
- Theme: dark navy และ orange accent ใกล้เคียงกับ `index.html`
- เนื้อหาหลัก:
  - Packets และ Frames
  - TCP/IP และ Three-Way Handshake
  - Practical เรื่อง Handshake
  - UDP/IP
  - Ports 101
  - สรุปภาพรวมและการนำไปใช้
- โครงสร้างภายใน:
  - มี table of contents แบบ anchor link
  - ใช้ section id `task1` ถึง `task5` และ `summary`
  - มีตาราง, กล่องคำอธิบาย, diagram แบบ inline SVG
- External dependency:
  - Google Fonts
  - ลิงก์อ้างอิง TryHackMe room
- Mobile: เพิ่ม header menu ข้ามไฟล์, ลด padding, ปรับหัวข้อ, table และ diagram ให้เลื่อนแนวนอนได้เมื่อจอแคบ

### `dns-in-detail-th.html`

บทเรียนเรื่อง Domain Name System

- Title: `DNS in Detail - สื่อการสอน Network Fundamentals`
- Theme: dark navy และ orange accent
- เนื้อหาหลัก:
  - What is DNS?
  - Domain Hierarchy
  - Record Types
  - Making A Request
  - Practical การ query DNS
  - สรุปภาพรวมและการนำไปใช้
- โครงสร้างภายใน:
  - ใช้ section id `t1` ถึง `t5` และ `summary`
  - มี table of contents, diagram, table, info box, warn box และ success box
- External dependency:
  - Google Fonts
- Mobile: เพิ่ม header menu ข้ามไฟล์, ปรับ task card, table, diagram และ flow step ให้ไม่ล้นจอ

### `extending-your-network-th.html`

บทเรียนเรื่องการขยายเครือข่ายและการควบคุม traffic

- Title: `Extending Your Network - สื่อการสอน Network Fundamentals`
- Theme: dark navy และ orange accent
- เนื้อหาหลัก:
  - Introduction to Port Forwarding
  - Firewalls 101
  - Practical - Firewall
  - VPN Basics
  - LAN Networking Devices: Router & Switch
  - Practical - Network Simulator
  - สรุปภาพรวมและการนำไปใช้
- โครงสร้างภายใน:
  - ใช้ section id `t1` ถึง `t6` และ `summary`
  - มี table of contents, diagram, flow step, table และกล่องคำอธิบาย
- External dependency:
  - Google Fonts
- Mobile: เพิ่ม header menu ข้ามไฟล์, ปรับ task card, table, diagram และ flow step ให้ไม่ล้นจอ

### `ctf-vol1.html`

คู่มือ CTF ขนาดใหญ่แบบ single-page

- Title: `CTF Collection Vol 1 - สรุปการแก้โจทย์และเทคนิค`
- Theme: dark palette แยกจากชุด Network โดยใช้ mint, pink และ yellow accent
- ฟอนต์:
  - Space Grotesk
  - IBM Plex Mono
  - Sarabun
- เนื้อหาหลัก:
  - Mindset และเครื่องมือพื้นฐาน
  - Walkthrough / เทคนิคสำหรับโจทย์ CTF 20 หัวข้อ
  - ภาคเตรียมสอบ CTF แบบ Jeopardy
  - ตารางเครื่องมือ CTF สำหรับห้องสอบ
  - หมวดสอบ 8 ด้าน: Web, Cryptography, Digital Forensic, Network Security, Reverse Engineering, Pwnable, Miscellaneous / OSINT และ Programming / Scripting
  - สรุปและเส้นทางต่อยอด
- โครงสร้างภายใน:
  - ใช้ section id `mindset`, `q1` ถึง `q20`, `exam-prep`, `exam-tools`, `exam-h1` ถึง `exam-h8` และ `summary`
  - มี sticky top bar, sidebar, mobile menu และ scroll-spy
- JavaScript:
  - ควบคุม sidebar บน mobile
  - ปิด sidebar เมื่อกด overlay
  - ใช้ IntersectionObserver เพื่อ highlight menu ตาม section ที่อ่านอยู่
- External dependency:
  - Google Fonts
  - ลิงก์เครื่องมือ CTF ภายนอก เช่น CyberChef, dCode, Aperi'Solve และแหล่งฝึกอื่น ๆ
- Mobile: topbar มีเมนูข้ามไฟล์แบบเลื่อนแนวนอน, sidebar เป็น overlay ผ่านปุ่มลอย, code block/table เลื่อนแนวนอนได้ และ exam/example cards ถูกจัดเรียงเป็นแนวตั้งบนจอเล็ก

## GitHub Pages Checklist

- มี `index.html` ที่ root ของ repository แล้ว
- ทุกหน้าเป็น static HTML ไม่ต้องมี build step
- ลิงก์จากหน้าแรกไปหน้าอื่นใช้ relative path
- ทุกหน้า HTML มีเมนูข้ามไฟล์ด้วย relative path
- ไม่มี asset ภายในที่ต้องอัปโหลดเพิ่มนอกจากไฟล์ HTML และ Markdown
- ควร commit และ push `ctf-vol1.html` เพราะเป็นไฟล์ใหม่ที่ต้องอยู่บน remote ก่อน GitHub Pages จะเปิดได้
- หลัง push แล้วให้ตรวจ URL หลัก: `https://panuwatsopwork.github.io/CTF/`

## ข้อเสนอแนะสำหรับการดูแลต่อ

- หากบทเรียนเพิ่มขึ้น ควรเพิ่ม card และ quick link ใน `index.html`
- หาก `ctf-vol1.html` โตขึ้นมาก ควรพิจารณาแยกเป็นหลายหน้าในอนาคตเพื่อให้โหลดเร็วขึ้น
- หากต้องการ UX แบบไปกลับครบทุกหน้า อาจเพิ่มลิงก์กลับหน้าแรกใน footer ของบทเรียนแต่ละหน้า
