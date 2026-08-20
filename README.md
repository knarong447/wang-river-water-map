# Wang River Water-Level WebGIS

แผนที่ออนไลน์สำหรับติดตามระดับน้ำและอัตราการไหลของสถานี 14 แห่งในลุ่มน้ำวัง พัฒนาด้วย Leaflet, OpenStreetMap และ JavaScript แบบ static เพื่อเผยแพร่ผ่าน GitHub Pages

## เปิดใช้งาน GitHub Pages

1. สร้าง repository ชื่อ `wang-river-water-map`
2. อัปโหลดไฟล์และโฟลเดอร์ทั้งหมดในแพ็กเกจนี้
3. เปิด **Settings → Pages**
4. ที่ **Source** เลือก **GitHub Actions**
5. รอ workflow ชื่อ **Deploy static site to Pages** ทำงานสำเร็จ
6. เว็บไซต์จะอยู่ที่ `https://USERNAME.github.io/wang-river-water-map/`

## ทดสอบในเครื่อง

เปิดด้วย local web server เช่น VS Code Live Server หรือ:

```bash
python -m http.server 8000
```

แล้วเปิด `http://localhost:8000`

## แหล่งข้อมูล

- ระดับน้ำและอัตราการไหล: ศูนย์อุทกวิทยาชลประทานภาคเหนือตอนบน กรมชลประทาน
- แผนที่ฐาน: OpenStreetMap
- พิกัดสถานี: ชุดข้อมูลที่ผู้ใช้ยืนยันเมื่อ 20 สิงหาคม 2569

## ข้อจำกัด

- เว็บไซต์เรียกข้อมูล JSONP จากระบบต้นทาง หากระบบต้นทางไม่ตอบสนอง จะแสดง “ไม่มีข้อมูล”
- เกณฑ์เตือนภัยใช้ค่า `level_limit` ที่แหล่งข้อมูลส่งกลับ
- ระบบนี้ใช้สนับสนุนการติดตามสถานการณ์ ไม่ใช่ประกาศเตือนภัยอย่างเป็นทางการ
