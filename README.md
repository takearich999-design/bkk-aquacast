# 🌊 BKK AquaCast — ศูนย์บัญชาการโทรมาตรแก้มลิงและเฝ้าระวังน้ำท่วม กทม.

ระบบศูนย์บัญชาการข้อมูลโทรมาตรแบบเรียลไทม์เพื่อเฝ้าระวัง บริหารจัดการ และเตือนภัยสถานการณ์น้ำท่วมในพื้นที่กรุงเทพมหานครและปริมณฑล ด้วยเทคโนโลยี Web GIS และ Radar Weather Visualization

🔗 **Live Deployment:** [https://graceful-lamington-947121.netlify.app/](https://graceful-lamington-947121.netlify.app/)

---

## 🚀 ฟังก์ชันหลักของระบบ (Core Features)

1. **🗺️ Cyber Dark Basemap & Interactive Geographic Information System (GIS)**
   - แผนที่ตอบสนองความเร็วสูงด้วย Leaflet 1.9.4 พร้อม Cyber Dark Filter คอนทราสต์สูง
   - รองรับการเปิด-ปิดชั้นข้อมูล (Layer Filters): แก้มลิง, จุดเสี่ยง, รายงานประชาชน, จุดจอดรถฉุกเฉิน
   - Quick Zone Zoom: สลับมุมมองด่วนสู่ 4 โซนสำคัญ (กทม. ชั้นใน, ฝั่งธนบุรี, ลาดกระบัง/KMITL, ท่าอากาศยานสุวรรณภูมิ)

2. **🌧️ เรดาร์ตรวจจับกลุ่มฝนสดและระบบพยากรณ์เมฆฝน (RainViewer Composite Engine)**
   - ดึงข้อมูลเรดาร์ฝนสดระดับประเทศและภูมิภาคแบบเรียลไทม์ผ่าน RainViewer API
   - เครื่องเล่นควบคุมไทม์ไลน์ฝน (Radar HUD Player): เล่นภาพวนลูป (Looping), ปรับความเร็ว, ย้อนหลัง และพยากรณ์ล่วงหน้า
   - แถบเฉดสี dBZ มาตรฐานอุตุนิยมวิทยา (เขียว-เหลือง-ส้ม-แดง-ม่วง)

3. **📊 ดัชนีสมดุล 3 น้ำ (Three-Water Balance Index)**
   - **น้ำเหนือ (Upstream Flow):** อัตราการไหลของน้ำผ่านเขื่อนเจ้าพระยาและสถานีวัดบางไทร (ลบ.ม./วินาที)
   - **น้ำหนุน (Sea Level Surge):** ระดับน้ำทะเลปานกลาง (ม.รทก.) ณ ป้อมพระจุลจอมเกล้า และปากอ่าวไทย
   - **น้ำฝน (Precipitation):** ปริมาณฝนสะสม 24 ชม. ทั่วทุกเขต กทม.

4. **🏞️ โครงข่ายแก้มลิงรองรับน้ำ 16 แห่ง กทม.**
   - ตรวจสอบความจุ ระดับน้ำปัจจุบัน และเปอร์เซ็นต์การกักเก็บน้ำของแก้มลิงสำคัญ (บึงหนองบอน, บึงมักกะสัน, บึงพระราม 9, คลองมหาชัย-สนามชัย ฯลฯ)
   - ข้อมูลอัตราการสูบระบายน้ำออกสู่แม่น้ำเจ้าพระยาและอ่าวไทย

5. **⚠️ 22 จุดเสี่ยงน้ำท่วมและน้ำรอระบายหลัก**
   - เฝ้าระวังจุดลุ่มต่ำตามถนนสายหลัก (วิภาวดีรังสิต, รัชดาภิเษก, สุขุมวิท, แจ้งวัฒนะ, ลาดพร้าว ฯลฯ)
   - แสดงสถานะความเสี่ยง 3 ระดับ: ปกติ (เขียว), เฝ้าระวัง (เหลือง), วิกฤต/ท่วมขัง (แดง)

6. **📸 รายงานเหตุน้ำท่วมจากภาคประชาชน (Citizen Reports)**
   - ประชาชนสามารถส่งพิกัด ภาพถ่าย ระดับความลึกของน้ำท่วมขัง และข้อความรายงานเหตุได้ทันที
   - ระบบจัดเก็บและแสดงผลหมุดแจ้งเหตุบนแผนที่แบบ Real-time พร้อมฟิลเตอร์ตามเขต

7. **🛡️ จุดจอดรถฉุกเฉินและสายด่วนกู้ภัย 24 ชม. (Safe Havens & Emergency SOS)**
   - จุดจอดรถอาคารสูงและพื้นที่ปลอดภัยหนีน้ำท่วม
   - รวมเบอร์สายด่วนรับแจ้งเหตุ (1555, 1784, 199, 1197)
   - ฟังก์ชันทดสอบสัญญาณไซเรนเตือนภัยจำลองผ่าน Web Audio API

---

## 🛠️ โครงสร้างสถาปัตยกรรมและเทคโนโลยี (Tech Stack)

- **Frontend:** Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Styling & UI:** Tailwind CSS (CDN) + Google Fonts (Prompt, JetBrains Mono)
- **Map & GIS:** Leaflet.js 1.9.4 พร้อม Local Assets Fallback
- **Weather & Radar Data:** RainViewer Public API / Local Telemetry Fallback Engine
- **Audio Engine:** Web Audio API (Synthesizer Siren Alarm)
- **Deployment:** Netlify Edge (รองรับ Cloudflare Pages, Vercel, GitHub Pages)

---

## 💻 วิธีการรันในเครื่อง (Local Development)

```bash
# 1. Clone repository
git clone https://github.com/takearich999-design/bkk-aquacast.git
cd bkk-aquacast

# 2. รัน Local Web Server (ตัวอย่างโดยใช้ Node / npx)
npx serve .

# หรือใช้ Python
python3 -m http.server 8080
```

เปิดบราวเซอร์ที่ `http://localhost:8080` เพื่อเข้าใช้งาน

---

## 📄 ลิขสิทธิ์และการพัฒนา (License)
พัฒนาภายใต้สัญญาอนุญาต MIT License โดย takearich999
