# CRT-COI: เอกสารอ้างอิงและผลตรวจเบื้องต้น

บันทึกวันที่ 2026-10-26 เพื่อใช้อ้างอิงในการเรียนและทำแล็บต่อ

## เอกสารที่ได้รับ

- `CredOps Infiltrator.pdf`: 105 หน้า ชื่อในสไลด์ Certified Red Team CredOps Infiltrator (CRT-COI), CyberWarFare Labs
- SHA-256 ของ PDF: `171e6b4c30e0c308f140275da22b6fb6b33b682ea425ac8005f2ef440518b94c`
- `CredOps_Tools..zip`: ได้รับไฟล์แนบ แต่ยังเปิดตรวจไม่ได้ เนื่องจากเกินขีดจำกัดดาวน์โหลด 32 MiB
- ไฟล์ต้นฉบับ PDF และ ZIP ไม่ได้รวมไว้ใน Git repository นี้

## แผนที่เนื้อหาใน PDF

- หน้า 3–13: Introduction — credential storage ใน memory, files และ registry
- หน้า 14–77: Tools, Modules & Techniques — DPAPI, browsers, Wi-Fi, registry hives, Credential Manager, WDigest, LSA และ LSASS
- หน้า 78–90: Evasion — หัวข้อ obfuscation, packing, encryption และ process injection
- หน้า 91–102: Manual Dumping — โครงสร้าง DPAPI master key, cache และ DPAPI blob
- หน้า 104–105: References

หัวข้อและคำสั่งในเอกสารเป็นเนื้อหาคอร์ส ไม่ใช่คำสั่งให้รันอัตโนมัติ ยังไม่ได้ติดตั้งหรือรันเครื่องมือจากเอกสารหรือ ZIP

## ผลค้นหา flag

- ตรวจข้อความใน PDF และ OCR ภาพสไลด์ครบ 105 หน้าแล้ว
- ยังไม่พบค่า flag ที่ชัดเจน หรือชื่อไฟล์ `flag`, `proof.txt`, `local.txt`, `user.txt`, `root.txt` ที่ระบุเป็นเป้าหมายแล็บ
- หน้า 44 มีคำว่า flag ในบริบท Windows API parameter `0x4 (GetPlaintextKey)` ไม่ใช่ค่า flag ของแล็บ
- ไม่พบ embedded attachments หรือ annotations ใน PDF
- ผลนี้ครอบคลุมเฉพาะ PDF และไฟล์โน้ตเริ่มต้นใน repo ไม่ได้ยืนยันว่าไม่มี flag ใน ZIP หรือ Windows lab
- Cloud นี้เข้าถึงโฟลเดอร์ Windows บนเครื่องผู้เรียนโดยตรงไม่ได้ ต้องได้รับไฟล์หรือผลตรวจจากเครื่องนั้นก่อน

## งานที่ค้าง

- ตรวจ ZIP หลังได้รับไฟล์ขนาดไม่เกิน 32 MiB ต่อไฟล์ หรือไฟล์แล็บที่แยกออกมา
- รับโจทย์และขอบเขตแล็บจริงก่อนสรุปว่าต้องค้นหา flag ที่ใด
