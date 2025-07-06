![โลโก้ภาษา DragonT](assets/images/logo.png)
# DragonT Language

## Demo
### 🇹🇭 ภาษาไทย  
ลองใช้งานภาษา DragonT ได้ที่ [DragonT Language Playground](https://11techasia.github.io/DragonT/)

### 🇬🇧 English  
Try DragonT online here [DragonT Language Playground](https://11techasia.github.io/DragonT/)

### 🇨🇳 中文  
点击这里体验 DragonT [DragonT 语言演示](https://11techasia.github.io/DragonT/)

**DragonT** is a new programming language that uses **Thai commands** to help beginners write and understand code more easily — without requiring English proficiency or prior coding experience.

---

## Purpose

DragonT is designed to be a simple yet powerful language for internal data processing, with the potential to expand into use cases in:

- Business
- Education
- Government

**Why DragonT?**
- Full Thai language syntax
- Beginner-friendly
- Flexible, extensible, and human-readable

---

## Developed & Maintained by: 11TECH Co., Ltd.  
**Version:** 0.1  
**Release Date:** 07/07/2025
**Author:** Eakkasit Tunsakool <lóng><龙>
---

## Example Usage

### Sample `.dragont` file
```plaintext
เริ่มโปรแกรม
รวม 5 กับ 10
ลบ 20 กับ 4
แสดง "จบการทำงาน"
จบโปรแกรม
```

## Run from command line
dragont example.dragont

## Installation
### For Linux/macOS
sudo cp target/release/dragont /usr/local/bin/dragont

### For Web (Vite + React)
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

## Currently Supported Features
```plaintext
-Basic keywords: เริ่มโปรแกรม, จบโปรแกรม

-Output command: แสดง "text"

-Arithmetic: รวม, บวก, ลบ, คูณ, หาร

-Conditional statements: e.g. ถ้า 1 + 1 เท่ากับ 2:
```

##  In Development
```plaintext
-Variable-support

-Logging-enabled interpreter

-REPL (interactive shell)

-CLI commands like dragont --help

-DSL support for AI, finance, and more
```