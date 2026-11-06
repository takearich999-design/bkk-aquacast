# 🌐 AquaCast Global & TH — ศูนย์บัญชาการโทรมาตร สภาพอากาศ และเรดาร์ตรวจจับฝนทั่วประเทศ & ทั่วโลก

ระบบศูนย์บัญชาการข้อมูลโทรมาตรแบบเรียลไทม์ ยกระดับการเฝ้าระวัง บริหารจัดการ และเตือนภัยสภาพอากาศ/น้ำท่วม จากระดับกรุงเทพฯ สู่ **ทั่วประเทศไทยและทั่วโลก (Nationwide & Worldwide)** ด้วยเทคโนโลยี Web GIS และ RainViewer Global Weather Radar Engine

🔗 **GitHub Repository:** [https://github.com/takearich999-design/bkk-aquacast](https://github.com/takearich999-design/bkk-aquacast)  
🔗 **Live Deployment:** [https://graceful-lamington-947121.netlify.app/](https://graceful-lamington-947121.netlify.app/)

---

## 🚀 ฟังก์ชันหลักที่ได้รับการอัปเกรด (Major Upgrades)

### 1. 🌏 เรดาร์ตรวจจับกลุ่มฝนและพายุทั่วโลก (Global Weather Radar)
- เชื่อมต่อสัญญาณเรดาร์สดจากเครือข่ายกว่า 1,000+ สถานีทั่วโลกผ่าน **RainViewer Global Composite API**
- ซูมดูได้ตั้งแต่ระดับโลก (World View: พายุไต้ฝุ่น, พายุหมุนเขตร้อน, แนวปะทะอากาศ) ไปจนถึงระดับอำเภอและตำบลในประเทศไทย
- **Radar HUD Player:** ควบคุมการเล่น Time-lapse กลุ่มเมฆฝน, ปรับความเร็ว 0.5x / 1x / 2x และโหมดพยากรณ์ล่วงหน้า (Nowcasting)

### 2. 🔍 ระบบค้นหาพิกัดและเมืองทั่วโลก (Global Location Search & FlyTo)
- ช่องค้นหาอัจฉริยะรองรับชื่อจังหวัด อำเภอ และเมืองทั่วโลก (เช่น เชียงใหม่, หาดใหญ่, Tokyo, London, Singapore, New York)
- เชื่อมต่อ OpenStreetMap Nominatim Geocoding API บินสู่พิกัดทันที (Smooth flyTo) พร้อมปักหมุดชั่วคราว
- แถบทางลัดบินด่วน (Quick Jump Chips) บนแผนที่

### 3. 🌐 สวิตช์เลือกขอบเขตมุมมองด่วน (Scope Selector)
- 🇹🇭 **ทั่วไทย (Thailand Nationwide):** ภาพรวม 77 จังหวัด
- 🌏 **ทั่วโลก (Global / Worldwide):** ติดตามแนวพายุระดับทวีป
- 🏙️ **กรุงเทพฯ & ปริมณฑล (BKK Hub):** ซูมเจาะลึกพื้นที่เมืองหลวง
- 🧭 **ภูมิภาคหลักในไทย:** ภาคเหนือ, ภาคอีสาน, ภาคกลาง, ภาคใต้, ภาคตะวันออก
- 🗺️ **ภูมิภาคสากล:** อาเซียน (ASEAN), เอเชียตะวันออก (Japan/Korea/Taiwan)

### 4. 🏞️ โครงข่ายเขื่อนหลัก 25 แห่งทั่วไทย & แก้มลิง กทม. 16 แห่ง (41 แห่ง)
- **เขื่อนยุทธศาสตร์ 25 แห่ง:** ภูมิพล, สิริกิติ์, แควน้อย, ป่าสักชลสิทธิ์, ศรีนครินทร์, วชิราลงกรณ, อุบลรัตน์, ลำปาว, สิรินธร, จุฬาภรณ์, ขุนด่านปราการชล, รัชชประภา, บางลาง ฯลฯ
- **แก้มลิง กทม. 16 แห่ง:** บึงหนองบอน, บึงมักกะสัน, บึงพระราม 9, คลองมหาชัย-สนามชัย ฯลฯ
- แสดงความจุกักเก็บ (ล้าน ลบ.ม.), เปอร์เซ็นต์ปริมาณน้ำปัจจุบัน, และอัตราการระบายน้ำ

### 5. ⚠️ จุดเสี่ยงน้ำท่วมและน้ำป่าหลาก 36 จุดสำคัญ
- **ต่างจังหวัด (14 จุด):** แม่สาย (เชียงราย), ริมน้ำปิง (เชียงใหม่), ริมน้ำยม (สุโขทัย), ริมน้ำน่าน, วารินชำราบ (อุบลฯ ริมน้ำมูล), ชุมชนริมน้ำชี, บางบาล-เสนา (อยุธยา), พุนพิน (สุราษฎร์ฯ), หาดใหญ่ (สงขลา), เมืองเก่าภูเก็ต ฯลฯ
- **กรุงเทพฯ (22 จุดเสี่ยงหลัก):** ถ.วิภาวดี, รัชดา, แจ้งวัฒนะ, รามคำแหง, ลาดพร้าว, สุขุมวิท, ศรีนครินทร์ ฯลฯ

### 6. 📡 สถานีเรดาร์และศูนย์อุตุนิยมวิทยา 24 แห่ง
- **เรดาร์กรมอุตุนิยมวิทยา (TMD) 16 สถานี:** อมก๋อย, ลำปาง, พิษณุโลก, ขอนแก่น, สกลนคร, อุบลราชธานี, ตาคลี, สัตหีบ, หัวหิน, สุราษฎร์ธานี, ภูเก็ต, สงขลา, สุวรรณภูมิ, หนองจอก, หนองแขม
- **ศูนย์อุตุนิยมวิทยาชั้นนำของโลก 8 แห่ง:** JMA (Tokyo), KMA (Seoul), HKO (Hong Kong), BoM (Sydney), NOAA (USA), Met Office (UK), DWD (Germany), ECMWF

### 7. 📊 โทรมาตรน้ำและสภาพอากาศโลก (Hydro & Global Climate)
- ตรวจสอบอัตราน้ำเหนือไหลผ่านแม่น้ำเจ้าพระยา (C.2 นครสวรรค์, C.13 เขื่อนเจ้าพระยา, C.29A บางไทร)
- ดัชนีมรสุม (ITCZ) และดัชนี ENSO (La Niña / El Niño)
- ดัชนีสมดุล 3 น้ำ กทม.

---

## 🛠️ โครงสร้างสถาปัตยกรรม (Tech Stack)

- **Frontend:** Vanilla HTML5, CSS3, JavaScript (ES6+ Modular)
- **Styling:** Tailwind CSS (CDN) + Custom Cyber Glass Theme
- **Map Engine:** Leaflet.js 1.9.4 with World Copy Jump & Cyber Dark Tiles
- **Weather & Radar:** RainViewer Global Composite API
- **Geocoding:** OpenStreetMap Nominatim API + Built-in Fast Coordinates
- **Audio:** Web Audio API (Multi-tone Siren Synthesizer)

---

## 💻 วิธีการรันในเครื่อง (Local Development)

```bash
git clone https://github.com/takearich999-design/bkk-aquacast.git
cd bkk-aquacast
npx serve .
# หรือ
python3 -m http.server 8080
```

---

## 📄 License
MIT License — takearich999
