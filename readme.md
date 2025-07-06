![โลโก้ภาษา DragonT](assets/images/logo.png)
# ภาษา DragonT

## Demo
### 🇹🇭 ภาษาไทย  
ลองใช้งานภาษา DragonT ได้ที่ [DragonT Language Playground](https://11techasia.github.io/DragonT/)

### 🇬🇧 English  
Try DragonT online here [DragonT Language Playground](https://11techasia.github.io/DragonT/)

### 🇨🇳 中文  
点击这里体验 DragonT [DragonT 语言演示](https://11techasia.github.io/DragonT/)


**DragonT** คือภาษาโปรแกรมที่ออกแบบด้วยแนวคิดใหม่ โดยใช้ **คำสั่งภาษาไทย** เพื่อให้ทุกคนสามารถเรียนรู้และเขียนโปรแกรมได้อย่างเข้าใจง่าย เหมาะกับคนเริ่มต้น  
โดยไม่จำเป็นต้องมีพื้นฐานด้านภาษาอังกฤษ


## จุดประสงค์
เพื่อสร้างภาษาที่เขียนง่าย เหมาะกับคนเริ่มต้น และรองรับการประมวลผลคำนวณข้อมูลด้านต่างๆภายในองค์กร  
พร้อมทั้งสามารถต่อยอดไปสู่การใช้งานในภาคธุรกิจ การศึกษา หรือภาครัฐ

ภาษา **DragonT**
**มีความยืดหยุ่นสูง ปรับแต่งง่าย และสามารถเขียนโค้ดโดยใช้ภาษาไทย**
- รองรับการใช้ภาษาไทยเต็มรูปแบบ
- เข้าใจง่ายแม้ไม่มีพื้นฐานการเขียนโปรแกรม


## **พัฒนาและดูแลโดย:** บริษัท 11TECH Co., Ltd.
**เวอร์ชัน:** 0.1
**วันเปิดตัว:** 07/07/2025
**ผู้เขียน:** Eakkasit Tunsakool <lóng><龙>

## ตัวอย่างการใช้งาน
```bash
- สร้างไฟล์นามสกุล `.dragont` เช่น `example.dragont`
- รันผ่าน command-line ด้วยคำสั่ง:

dragont example.dragont
```
## ติดตั้งสำหรับ (Linux/macOS)
```bash
sudo cp target/release/dragont /usr/local/bin/dragont
```
## ติดตั้งสำหรับ Website
```bash
#vite , react
import init, { run_dragont } from './pkg/dragont.js';
import wasmUrl from './pkg/dragont_bg.wasm?url';
```
```bash
  useEffect(() => {
    init(wasmUrl)
      .then(() => {
        wasmReady.current = true;
        setOutput("พร้อมใช้งาน");
      })
      .catch((err) => {
        console.error(err);
      });
  }, []);

  const run = () => {
    if (!wasmReady.current) {
      setOutput("กำลังโหลด");
      return;
    }

    try {
      const result = run_dragont(code);
      setOutput(result);
    } catch (err) {
      console.error(err);
    }
  };
```

## ทดสอบ
```bash
dragont path/to/your_file.dragont
```



## ตัวอย่างเบื้องต้น

```plaintext
เริ่มโปรแกรม
รวม 5 กับ 10
ลบ 20 กับ 4
แสดง "จบการทำงาน"
จบโปรแกรม
```



## คำสั่งพื้นฐาน

- คำสั่งพื้นฐาน: `เริ่มโปรแกรม`, `จบโปรแกรม`
- พิมพ์: `แสดง "ข้อความ"`
- การคำนวณพื้นฐาน: `รวม`, `บวก`, `ลบ`, `คูณ`, `หาร`
- เงื่อนไข if-else: รองรับรูปแบบ `ถ้า 1 + 1 เท่ากับ 2:`



## สิ่งที่อยู่ระหว่างการพัฒนา

- [ ] รอบรับตัวแปร
- [ ] วางแผนสำหรับ Interpreter แบบมีระบบบันทึก
- [ ] โหมดรับคำสั่งแบบ REPL
- [ ] รองรับคำสั่ง CLI เช่น dragont --help
- [ ] ภาษา DSL สำหรับ AI, การเงิน



