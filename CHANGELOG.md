# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

> ไฟล์นี้สร้างจากประวัติ git เพราะโปรเจกต์ยังไม่มี changelog มาก่อน และไม่มี git tag ตามเวอร์ชัน
> วันที่ของ `2.0.0`–`2.0.3` จึงเป็นการประมาณจาก commit ที่เริ่มใช้เวอร์ชันนั้น
> เวอร์ชันที่แสดงในแอป (`appConfig.appVersion`) อาจต่างจากเวอร์ชัน build (`latestVersion` / `app.config.js`)

## [Unreleased]

### Removed

- ลบไฟล์ CI เก่า (GitLab CI, Docker local build) และไฟล์ config สำรอง หลัง sync จาก sitdev

## [2.0.4] - 2026-08-23

เวอร์ชัน build ปัจจุบัน (`app.config.js` / `runtimeVersion` = `2.0.4`)
แสดงในแอปเป็น `2.0.2`

### Added

- ช่องหมายเหตุคิว (Queue Remark) และแสดงในหน้าสรุป ([Jira-3459], [Jira-3466])
- Autofill สำนักงานที่ดินในฟอร์มคิว ([Jira-3463])
- ผู้ให้ / ผู้รับ / เจ้าของ ในคิว ตามการตั้งค่า BF ([Jira-3460])
- รองรับสำนักงานที่ดินภายนอกในคิว ([Jira-3389], [Jira-3390], [Jira-3440])
- ปฏิทินรังวัดแสดงเฉพาะวันที่ว่าง ([Jira-3467])
- เปรียบเทียบเวอร์ชันกับสโตร์แบบ semver พร้อม unit test
- Expo config plugin สำหรับ CodePush keys และ Android network security
- สคริปต์ `restoreAndroidAssets` สำหรับ prebuild Android

### Changed

- อัปเดตเวอร์ชันแอปจาก `2.0.3` เป็น `2.0.4` และเวอร์ชันที่แสดงจาก `2.0.1` เป็น `2.0.2`
- ปรับ dialog ประกาศ, hook คิวรังวัด, และหน้าสรุปค่าธรรมเนียม/ภาษี (RCAL)
- ไม่บังคับอัปเดตเวอร์ชันจากสโตร์ในบางกรณี

### Fixed

- เลขโฉนดซ้ำในคิว ([Jira-3485])
- ไม่สามารถเปลี่ยนประเภทจดทะเบียนได้ และ dropdown เลขโฉนดซ้อนกัน ([Jira-3385], [Jira-3455])
- ข้อความ error วันที่รังวัด ([Jira-3452])
- แก้คิวสำนักงานที่ดินภายนอก ([Jira-3389])
- Modal แก้ไขโปรไฟล์ไม่เลื่อนตามคีย์บอร์ด ([Jira-3457])
- RCAL ([Jira-3495])
- แก้หลาย issue พร้อมกัน: [DEQ-3358], [DEQ-3178], [DEQ-3378], [DEQ-3383], [DEQ-3389], [DEQ-3436], [DEQ-3435], [DEQ-3437]
- Build Android และ native lock ของ vector icons บน iOS

## [2.0.3] - 2026-06-08

เวอร์ชันที่ `appConfig.latestVersion` เป็น `2.0.3` (แสดงในแอปเป็น `2.0.1`)
รวมงาน Electronic Queue / โปรไฟล์ / native ที่ sync เข้ามาช่วงต้นปี–กลางปี 2026

### Added

- UI new-design สำหรับคิวอิเล็กทรอนิกส์ทั้ง 3 ประเภท (จดทะเบียน, รังวัด, จดทะเบียนต่างสำนักงาน)
- จัดการตัวแทน (manage agent) แบบ new-design
- คู่มือในแอป และหน้าประวัติคิว / รายละเอียดคำขอ
- CodePush (Revopush) สำหรับ Android และ iOS
- Splash screen และไอคอนแอปชุดใหม่

### Changed

- ปรับฟอร์มคำขอ, นิติกรรม, เอกสาร, ปฏิทินนัดหมาย ของทุกประเภทคิว
- ปรับ forgot password / OTP / แก้ไขโปรไฟล์ / ข้อกำหนดและเงื่อนไข
- ปรับหน้าแรก, รายการคิว, และการแจ้งเตือน

### Fixed

- ปัญหาการรันแอปบน Android / local API ในช่วง setup native

## [2.0.0] - 2025-08-01

เริ่มโมดูลคิวอิเล็กทรอนิกส์และแอปหลัก e-QLands Plus (นอกเหนือจาก RCAL)

### Added

- Electronic Queue: คำขอจดทะเบียน, คำขอรังวัด, จดทะเบียนต่างสำนักงาน
- Tab navigator: หน้าหลัก, คิว, ยื่นคำขอ, การแจ้งเตือน, โปรไฟล์
- สมัครสมาชิกบุคคลธรรมดาและนิติบุคคล, OTP, ข้อกำหนดและเงื่อนไข
- ลืมรหัสผ่าน / รีเซ็ตรหัสผ่าน
- จัดการตัวแทน (นิติบุคคล)
- การแจ้งเตือนในแอป
- เอกสารคู่มือภาษาไทย (`README.th.md`)

## [1.0.0] - 2025-04-03

แปลงโปรเจกต์เป็น TypeScript และพัฒนา RCAL (คำนวณค่าธรรมเนียม) จนครบ flow หลัก

### Added

- โครงสร้าง Expo Router + TypeScript
- RCAL: ที่ดิน, สิ่งปลูกสร้าง, ห้องชุด / คอนโด
- ประเภทธุรกรรม: ขาย, จำนอง, ให้, มรดก, เช่า, กรรมสิทธิ์ร่วม
- หน้าประมาณราคา, โฉนด, สรุปค่าธรรมเนียม/ภาษี, ลดหย่อนภาษี
- ดาวน์โหลด PDF สรุป (ที่ดิน, ห้องชุด, เช่า, จำนอง)
- Login / guest (anonymous token)
- สมัครสมาชิก, OTP, ข้อกำหนดและเงื่อนไข ([DEQ-636], [DEQ-681])
- สรุปจำนวนผู้ใช้ทั้งหมดและรายเดือนบนหน้า login RCAL ([DEQ-519])
- ระบบ i18n ไทย/อังกฤษ
- Network debugger
- Unit test (Jest)
- CI/CD: GitLab, EAS Build, Jenkins

### Changed

- ปรับ validation, formatter ตัวเลข, และ UX ช่องกรอกทั้ง flow
- แยก flow บุคคลธรรมดา / นิติบุคคล สำหรับขายและจำนอง ([DEQ-315])
- ซ่อนหน้าให้และมรดกสำหรับนิติบุคคล ([DEQ-682], [DEQ-683])
- จัดโครงสร้างตาม feature / Clean Architecture

### Fixed

- Validation โฉนด, พื้นที่, ราคาประเมิน, และ acquisition หลายประเภท
- Navigation ย้อนกลับและวนฟอร์มเมื่อมีหลายแปลง/หลายอาคาร
- แสดงผลบน Android (line height, checkbox, foldable)
- ปฏิทินพุทธศักราชในฟอร์ม RCAL
- Build / Expo Doctor / plugin ของ EAS

## [0.1.0] - 2025-03-30

### Added

- Initial commit ของโปรเจกต์ EQLand Mobile

[Unreleased]: https://dc2-gitlab.dol.go.th/root/eqlandsmobile/-/compare/202ea0a8d9af5b083e9d9fcb9b1f6268c9afa02d...HEAD
[2.0.4]: https://dc2-gitlab.dol.go.th/root/eqlandsmobile/-/compare/ad49e1ae03bb92f95b7522f9d32f65b9f01b9339...202ea0a8d9af5b083e9d9fcb9b1f6268c9afa02d
[2.0.3]: https://dc2-gitlab.dol.go.th/root/eqlandsmobile/-/compare/05d87b73971d94547b63fb464e5a6044aa5efd0d...ad49e1ae03bb92f95b7522f9d32f65b9f01b9339
[2.0.0]: https://dc2-gitlab.dol.go.th/root/eqlandsmobile/-/compare/7825152804ebe2ae5a96b700610a3b19c6fb6442...05d87b73971d94547b63fb464e5a6044aa5efd0d
[1.0.0]: https://dc2-gitlab.dol.go.th/root/eqlandsmobile/-/compare/166e9d2ac8c8bd34de80efaea0d760f247207538...7825152804ebe2ae5a96b700610a3b19c6fb6442
[0.1.0]: https://dc2-gitlab.dol.go.th/root/eqlandsmobile/-/commits/166e9d2ac8c8bd34de80efaea0d760f247207538
