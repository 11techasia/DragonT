![โลโก้ภาษา DragonT](assets/images/logo.png)
# DragonT 编程语言

## Demo
### 🇹🇭 ภาษาไทย  
ลองใช้งานภาษา DragonT ได้ที่ [DragonT Language Playground](https://11techasia.github.io/DragonT/)

### 🇬🇧 English  
Try DragonT online here [DragonT Language Playground](https://11techasia.github.io/DragonT/)

### 🇨🇳 中文  
点击这里体验 DragonT [DragonT 语言演示](https://11techasia.github.io/DragonT/)

**DragonT** 是一种全新的编程语言，使用 **泰语指令**，让初学者无需掌握英语或编程基础也能轻松编写和理解代码。

---

## 📌 目标

DragonT 旨在成为一种简单而强大的语言，用于企业内部的数据处理，同时也可扩展用于以下场景：

- 商业领域  
- 教育系统  
- 政府部门  

**为什么选择 DragonT？**
- 完整支持泰文语法  
- 初学者友好  
- 灵活、可扩展、可读性强  

---

## 开发与维护单位：11TECH 有限公司  
**版本：** 0.1  
**发布日期：** 2025 年 7 月 7 日
**作者： ** Eakkasit Tunsakool <lóng><龙>
---

## 💡 使用示例

### `.dragont` 示例文件：
```plaintext
เริ่มโปรแกรม
รวม 5 กับ 10
ลบ 20 กับ 4
แสดง "จบการทำงาน"
จบโปรแกรม
```
## 命令行运行方式
```bash
dragont example.dragont
```
## 安装说明
### 适用于 Linux/macOS
```bash
sudo cp target/release/dragont /usr/local/bin/dragont
```
### 适用于网页（Vite + React）：
```bash
import init, { run_dragont } from './pkg/dragont.js';
import wasmUrl from './pkg/dragont_bg.wasm?url';
```
```bash
useEffect(() => {
  init(wasmUrl)
    .then(() => {
      wasmReady.current = true;
      setOutput("Ready");
    })
    .catch((err) => {
      console.error(err);
    });
}, []);

const run = () => {
  if (!wasmReady.current) {
    setOutput("Loading...");
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
## 当前支持功能
```plaintext
- 基本关键词：เริ่มโปรแกรม（开始程序）, จบโปรแกรม（结束程序）

- 输出命令：แสดง "文本"

- 算术操作：รวม（合计）, บวก（加）, ลบ（减）, คูณ（乘）, หาร（除）

- 条件判断：例如 ถ้า 1 + 1 เท่ากับ 2:（如果 1+1 等于 2）
```
## 开发中功能
```plaintext
- 支持变量

- 带日志的解释器

- REPL 交互式命令行模式

- 命令行支持，例如 dragont --help

- 面向 AI、金融等行业的 DSL 支持

```