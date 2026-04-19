short name : ARM long name : Apartment Room Management command create django - MVT

django-admin startproject arm
cd arm
python manage.py startapp services
python manage.py runserver
if do not work do

'py -m django startproject '
cd
'py manage.py startapp services'
'py manage.py runserver' how to setup go --> services --> view.py (create view)
install SQL

pip install pymysql
python manage.py migrate <-- ใช้ติดตั้ง Table พื้นฐานสำหรับการใช้งาน
ระบบจัดการหอพัก (ARM - Apartment Room Management) ├── 1. หน้าหลัก (Dashboard) │ ├── แสดงภาพรวม (Stats Cards) │ │ ├── จำนวนห้องทั้งหมด │ │ ├── จำนวนห้องว่าง │ │ ├── ยอดค้างชำระ │ │ └── รายการแจ้งซ่อมคงค้าง │ ├── ตารางสถานะห้องพักรายชั้น (Floor Status) │ ├── รายการแจ้งเตือนล่าสุด (Recent Alerts) │ └── ทางลัดการใช้งาน (Quick Actions) │ ├── 2. จัดการห้องพัก (Room Management) - [รองรับข้อ 7] │ ├── ผังห้องพักทั้งหมด (Floor Plan View) │ ├── ข้อมูลประเภทห้องและราคา (Room Types) │ └── สถานะการทำความสะอาด/ความพร้อมของห้อง │ ├── 3. จัดการผู้อาศัย (Tenant Management) - [รองรับข้อ 1] │ ├── ทะเบียนผู้เช่าปัจจุบัน (Active Tenants) │ ├── ระบบทำสัญญาเช่า/ต่อสัญญา (Contract Management) │ ├── ประวัติการย้ายเข้า-ย้ายออก (Tenant History) │ └── เอกสารแนบ (สำเนาบัตรประชาชน/ทะเบียนบ้าน) │ ├── 4. บัญชีและค่าเช่า (Billing & Accounting) - [รองรับข้อ 2, 5, 6] │ ├── บันทึกมิเตอร์น้ำ-ไฟ (Utility Meter Reading) │ ├── การออกใบแจ้งหนี้รายเดือน (Invoicing) │ ├── ระบบรับชำระเงินผ่านธนาคาร/แนบสลิป (Bank Payments) │ ├── ระบบตรวจสอบและยืนยันการชำระเงิน (Payment Verification) │ └── รายงานยอดค้างชำระ (Overdue Reports) │ ├── 5. ระบบแจ้งซ่อม (Maintenance System) - [รองรับข้อ 4] │ ├── รายการแจ้งซ่อมจากผู้เช่า (Maintenance Requests) │ ├── มอบหมายงานและติดตามสถานะ (Task Tracking) │ └── ประวัติการซ่อมบำรุงและค่าใช้จ่าย │ ├── 6. ประชาสัมพันธ์และการแจ้งเตือน (Announcements & Notifications) - [รองรับข้อ 3] │ ├── จัดการประกาศข่าวสาร (Public News) │ ├── ระบบส่งข้อความแจ้งเตือนผู้เช่าเมื่อถึงรอบบิล (Billing Alerts) │ └── แจ้งเตือนสถานะการแจ้งซ่อม (Maintenance Updates) │ └── 7. ตั้งค่าระบบ (System Settings) ├── ข้อมูลหอพัก (Dormitory Profile) ├── จัดการสิทธิ์ผู้ใช้งาน (User Roles/Admin) └── สำรองข้อมูลระบบ (Backup)

Mydatabase Schema (อัปเดตล่าสุดรองรับระบบชำระเงินและแจ้งเตือน)

