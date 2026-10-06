# 🏢 Database for Dormitory Booking Application

[![XAMPP](https://img.shields.io/badge/Environment-XAMPP-orange.svg)](https://www.apachefriends.org/)
[![Database](https://img.shields.io/badge/Database-MySQL%2FMariaDB-blue.svg)](https://www.mariadb.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

ระบบฐานข้อมูลสำหรับการจองห้องพักหอพัก (Dormitory Booking System) ออกแบบมาเพื่อจัดการข้อมูลผู้ใช้งาน การจองห้องพัก การชำระเงิน และค่าน้ำค่าไฟอย่างเป็นระบบ

---

## 📌 เกี่ยวกับโครงการ (Project Overview)
โครงการนี้เป็นฐานข้อมูลเชิงสัมพันธ์ (Relational Database) ที่ออกแบบมาเพื่อรองรับแอปพลิเคชันจองห้องพักหอพัก ช่วยรองรับกระบวนการทำงานตั้งแต่การค้นหาห้องว่าง การจองห้องพัก การออกบิลชำระเงิน ไปจนถึงการแจ้งซ่อมสิ่งอำนวยความสะดวกภายในห้องพัก

---

## ✨ ฟีเจอร์และขอบเขตระบบ (Features)
- **จัดการผู้ใช้งาน (User Management):** รองรับบทบาทนักศึกษา/ผู้เช่า (Student/Tenant) และผู้ดูแลระบบ (Admin)
- **จัดการห้องพัก (Room Management):** จัดการข้อมูลประเภทห้องพัก (แอร์/พัดลม), ราคา, สิ่งอำนวยความสะดวก และสถานะห้องว่าง
- **ระบบการจองห้องพัก (Booking System):** ตรวจสอบห้องว่าง การทำรายการจอง เช็กอิน/เช็กเอาต์ และประวัติการจอง
- **ระบบชำระเงินและบิล (Payment & Billing):** ออกบิลค่าน้ำ ค่าไฟ ค่าเช่ารายเดือน และบันทึกหลักฐานการชำระเงิน
- **ระบบแจ้งซ่อม (Maintenance System):** แจ้งเรื่องร้องเรียน/แจ้งซ่อมอุปกรณ์ชำรุดภายในห้อง

---

## 📊 ER Diagram (Entity-Relationship Diagram)
*(แปะรูปภาพ ER Diagram ของคุณที่นี่)*

![ER Diagram](./docs/er-diagram.png)

---

## 🗄️ โครงสร้างตารางข้อมูลหลัก (Database Schema)

| ตาราง (Table Name) | คำอธิบาย (Description) |
| :--- | :--- |
| `users` | เก็บข้อมูลผู้ใช้งาน (นักศึกษา/ผู้เช่า และ Admin) |
| `dormitories` | เก็บข้อมูลอาคาร/หอพัก |
| `room_types` | เก็บรายละเอียดประเภทห้องพัก (เช่น ห้องแอร์เตียงคู่, ห้องพัดลมเตียงเดี่ยว) |
| `rooms` | เก็บข้อมูลห้องพักแต่ละห้อง เลขห้อง ชั้น และสถานะห้อง (`available`, `booked`, `occupied`) |
| `bookings` | เก็บประวัติและรายละเอียดการจองห้องพัก |
| `payments` | เก็บข้อมูลการชำระเงิน บิลค่าน้ำ/ไฟ และสถานะการชำระเงิน (`pending`, `approved`, `rejected`) |
| `maintenance_requests` | เก็บรายการแจ้งซ่อมอุปกรณ์ภายในห้อง |

---

## 🛠️ เทคโนโลยีและเครื่องมือ (Tech Stack)
- **Local Server Environment:** XAMPP
- **Database Engine:** MySQL / MariaDB
- **Database Management Tool:** phpMyAdmin
- **Language:** SQL (DDL, DML)

---

## 🚀 วิธีติดตั้งและใช้งานด้วย XAMPP (Getting Started with XAMPP)

### 1. เตรียมความพร้อมระบบ
1. ดาวน์โหลดและติดตั้ง [XAMPP](https://www.apachefriends.org/)
2. เปิด **XAMPP Control Panel** และกด **Start** ที่บริการ **MySQL** (และ Apache หากต้องการใช้งาน phpMyAdmin)

### 2. Clone Repository
```bash
git clone [https://github.com/taksornc/database-for-dormitory-booking-application.git](https://github.com/taksornc/database-for-dormitory-booking-application.git)
cd database-for-dormitory-booking-application
