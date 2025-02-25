# ใบงานการทดลอง HTML

## การทดลองที่ 4: การสร้างลิงก์และการแทรกรูปภาพ

### การเตรียมโครงสร้างโฟลเดอร์และไฟล์
1. สร้างโครงสร้างโฟลเดอร์:
   ```
   html-workshop/
   ├── index.html
   ├── pages/
   │   ├── about.html
   │   └── contact.html
   ├── images/
   │   ├── logo.jpg
   │   └── products/
   │       ├── product1.jpg
   │       └── product2.jpg
   └── files/
       └── document.pdf
   ```

2. ขั้นตอนการสร้างโครงสร้าง:
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "pages"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "images"
   - ในโฟลเดอร์ images > New Folder > สร้าง "products"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "files"

3. สร้างไฟล์ HTML:
   - ในโฟลเดอร์หลัก: สร้าง index.html (ใช้ไฟล์เดิมที่มีได้)
   - ในโฟลเดอร์ pages: สร้าง about.html และ contact.html

4. จัดเตรียมไฟล์:
   - นำรูปภาพที่ต้องการใช้ไปไว้ในโฟลเดอร์ images
   - นำรูปภาพสินค้าไปไว้ในโฟลเดอร์ products
   - นำไฟล์เอกสารไปไว้ในโฟลเดอร์ files

### ขั้นตอนการทดลอง

#### ส่วนที่ 1: การสร้างลิงก์
1. เปิดไฟล์ index.html และใส่โครงสร้างพื้นฐาน:
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>หน้าหลัก</title>
</head>
<body>
    <!-- ส่วนของเนื้อหา -->
</body>
</html>
```

2. สร้างเมนูนำทางพื้นฐาน:
```html
<nav>
    <!-- ลิงก์ภายใน - ไปยังหน้าในเว็บไซต์เดียวกัน -->
    <a href="index.html">หน้าหลัก</a>
    <a href="pages/about.html">เกี่ยวกับเรา</a>
    <a href="pages/contact.html">ติดต่อเรา</a>
    
    <!-- ลิงก์ภายนอก - เปิดในแท็บใหม่ -->
    <a href="https://www.google.com" target="_blank">
        ไปยัง Google
    </a>
</nav>
```
คำอธิบาย:
- `href="..."` - กำหนดเส้นทางของลิงก์
- `target="_blank"` - เปิดลิงก์ในแท็บใหม่

3. สร้างลิงก์ภายในหน้าเดียวกัน:
```html
<!-- สร้างจุดเชื่อมโยง -->
<section id="top">
    <h1>เนื้อหาส่วนบน</h1>
</section>

<section id="products">
    <h2>สินค้าของเรา</h2>
</section>

<!-- ลิงก์ไปยังจุดเชื่อมโยง -->
<a href="#top">กลับด้านบน</a>
<a href="#products">ไปยังสินค้า</a>
```
คำอธิบาย:
- `id="..."` - กำหนดจุดเชื่อมโยง
- `href="#..."` - ลิงก์ไปยัง id ที่กำหนด

4. สร้างลิงก์พิเศษ:
```html
<!-- ลิงก์อีเมล -->
<a href="mailto:contact@example.com">ส่งอีเมลหาเรา</a>

<!-- ลิงก์โทรศัพท์ -->
<a href="tel:+66812345678">โทร 081-234-5678</a>

<!-- ลิงก์ดาวน์โหลด -->
<a href="files/document.pdf" download>
    ดาวน์โหลดเอกสาร
</a>
```
คำอธิบาย:
- `mailto:` - เปิดโปรแกรมอีเมล
- `tel:` - เปิดโปรแกรมโทรศัพท์
- `download` - ดาวน์โหลดไฟล์แทนการเปิด

#### ส่วนที่ 2: การแทรกรูปภาพ
1. แทรกรูปภาพพื้นฐาน:
```html
<!-- รูปภาพในโฟลเดอร์ images -->
<img src="images/logo.jpg" 
     alt="โลโก้บริษัท"
     width="200">

<!-- รูปภาพในโฟลเดอร์ย่อย products -->
<img src="images/products/product1.jpg" 
     alt="สินค้าชิ้นที่ 1"
     width="300"
     height="200">
```
คำอธิบาย:
- `src="..."` - ระบุตำแหน่งของรูปภาพ
- `alt="..."` - ข้อความทดแทนเมื่อไม่สามารถแสดงรูปได้
- `width="..."` - กำหนดความกว้าง
- `height="..."` - กำหนดความสูง

2. ใช้ figure และ figcaption:
```html
<figure>
    <img src="images/products/product2.jpg" 
         alt="สินค้าชิ้นที่ 2">
    <figcaption>
        รายละเอียดสินค้าชิ้นที่ 2
    </figcaption>
</figure>
```
คำอธิบาย:
- `<figure>` - จัดกลุ่มรูปภาพและคำอธิบาย
- `<figcaption>` - คำอธิบายประกอบรูปภาพ

3. สร้างรูปภาพที่คลิกได้:
```html
<a href="images/products/product1.jpg">
    <img src="images/products/product1.jpg" 
         alt="คลิกเพื่อดูรูปขนาดใหญ่"
         width="200">
</a>
```

### หมายเหตุ
- ตรวจสอบการสะกดชื่อไฟล์และโฟลเดอร์ให้ถูกต้อง
- path ของรูปภาพต้องถูกต้องตามโครงสร้างโฟลเดอร์
- ทดสอบการทำงานของลิงก์ทุกจุด

### แบบฝึกหัด
1. สร้างแกลเลอรีสินค้า:
   - สร้างโฟลเดอร์ images/gallery
   - ใส่รูปภาพอย่างน้อย 4 รูป
   - แต่ละรูปต้องคลิกดูขนาดใหญ่ได้
   - มีคำอธิบายใต้รูป
   - มีปุ่มกลับด้านบน

### บันทึกผลการทดลอง
- รหัสเอกสาร HTML ที่เขียน:
```html
[<!DOCTYPE html>
<html lang="en">
<head>
    <title>PRODUCTS OF POKÉMON CARDS</title>
    <!-- นำเข้า Google Fonts -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Montserrat:wght@400;700&display=swap">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
        }
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Montserrat', sans-serif;
        }
        nav, section, figure, figcaption {
            margin-bottom: 20px;
        }
        nav img {
            vertical-align: middle;
        }
        nav a {
            margin-right: 10px;
            text-decoration: none;
            color: #333;
            font-weight: 700;
        }
        figure {
            text-align: center;
        }
        hr {
            margin: 20px 0;
        }
    </style>
</head>
<body>
    
    <nav>
        <!-- ลิงก์ภายใน - ไปยังหน้าในเว็บไซต์เดียวกัน -->
       
        <!-- รูปภาพในโฟลเดอร์ images -->
            <img src="images/products/logop.png" 
            alt="โลโก้บริษัท"
            height="100"
            width="400">
            <a href="index.html">หน้าหลัก</a>
        <a href="test.html">กลับ</a>
        
        <!-- ลิงก์ภายนอก - เปิดในแท็บใหม่ -->
        <a href="https://www.google.com" target="_blank">
            ไปยัง Google
        </a>
    </nav>
    <!-- สร้างจุดเชื่อมโยง -->
<section id="top">
    <h1>การ์ดโปเกม่อนจาก Pokémon</h1>
</section>

<section id="products">
    <h2>สินค้าของทางร้านเรา</h2>
</section>

<!-- กล่องใส่สินค้า -->
<figure>
    <!-- รูปภาพที่กดเพื่อดูขนาดใหญ่ -->
    <a href="images/products/1.jpg">
        <img src="images/products/1.jpg" 
             alt="Charizard Pokémon Card"
             width="300"
             height="400">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Charizard Pokémon Card</strong>
        คุณสมบัติ: ความหายากสูง, พลังโจมตีระดับสูง, การ์ดสวยงาม
        จุดเด่น:
        การ์ดสะสมที่มีคุณค่าทางจิตใจ
        ออกแบบอย่างละเอียดและสวยงาม
        เหมาะสำหรับการสะสมและการเล่นการแข่งขัน</figcaption>
</figure>
<hr>

<figure>
    <a href="images/products/2.jpg">
        <img src="images/products/2.jpg" 
             alt="Pikachu Pokémon Card"
             width="300"
             height="400">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Pikachu Pokémon Card</strong>
        คุณสมบัติ: ความหายากระดับกลาง, พลังโจมตีไฟฟ้า, การ์ดน่ารัก
        จุดเด่น:
        การ์ดที่ได้รับความนิยมสูง
        ตัวละครที่เป็นสัญลักษณ์ของโปเกม่อน
        เหมาะสำหรับนักสะสมและผู้เริ่มต้น</figcaption>
</figure>

<figure>
<hr>
    <a href="images/products/3.png">
    <img src="images/products/3.png" 
         alt="Meowth Pokémon Card"
         width="300"
         height="400">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Meowth Pokémon Card</strong>
        คุณสมบัติ: การ์ดรางวัลพิเศษ, พลังโจมตีแบบธรรมดา, การ์ดที่ได้รับความนิยม
        จุดเด่น:
        การ์ดสำหรับการสะสมและการเล่น
        ออกแบบให้มีความสวยงามและล้ำลึก
        เหมาะสำหรับการใช้งานในเด็คการแข่งขัน</figcaption>
</figure>

<hr>
<figure>
    <!-- รูปภาพที่กดเพื่อดูขนาดใหญ่ -->
    <a href="images/products/4.png">
        <img src="images/products/4.png" 
             alt="Bulbasaur Pokémon Card"
             width="300"
             height="400">
    </a>
    <figcaption>รายละเอียดสินค้า</figcaption>
    <figcaption><strong>Bulbasaur Pokémon Card</strong>
        คุณสมบัติ: การ์ดพื้นฐาน, พลังโจมตีพืช, การ์ดที่ได้รับความนิยม
        จุดเด่น:
        การ์ดเริ่มต้นที่ดีสำหรับผู้เล่นใหม่
        ความคลาสสิกและเป็นที่รู้จักในวงกว้าง
        เหมาะสำหรับการสะสมและการเล่นเบื้องต้น</figcaption>
</figure>
<hr>

</body>
</html>
]
```



- ภาพผลลัพธ์:
[![alt text](image-7.png)]

![alt text](image-8.png)


