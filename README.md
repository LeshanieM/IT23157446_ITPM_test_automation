# Test Automation Project – Chat Translator

**BSc (Hons) in Information Technology – Year 3**  
**IT3040 – ITPM | Assignment 1 (Option 1)**

---

## Objective

Automate testing of the **Chat Sinhala** transliteration function at  
[pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator) using Playwright.

Identify **50 failure cases** (minimum 2 cases per the 24 Singlish input types) where chat-style Singlish is incorrectly converted to Sinhala.

---

## What's Included

- `test_automation.py` – Playwright automation script
- `IT23157446.xlsx` – Test case file (rename with your registration number)

---

## Setup Instructions

### 1. Install Prerequisites

- **Python 3.11 or 3.12** – [Download here](https://www.python.org/downloads/)
- **Google Chrome** (recommended)

### 2. Extract & Navigate

Extract the project and open Command Prompt. Navigate to the project directory:

```cmd
cd /d D:\IT23157446_ITPM_test_automation
```

### 3. Install Dependencies

```cmd
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## Run the Automation

```cmd
python test_automation.py --excel "IT23157446.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

| Argument | Purpose |
| :--- | :--- |
| `--excel` | Path to your test case file |
| `--url` | Application URL |
| `--wait-ms` | Wait time for translation (ms) |
| `--type-delay-ms` | Delay between keystrokes |
| `--slow-mo-ms` | Slows Playwright actions |
| `--save-every` | Save Excel after every N tests |
| `--keep-open` | Keep browser open after run |
