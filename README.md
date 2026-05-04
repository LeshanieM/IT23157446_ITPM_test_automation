# Test Automation Project

This project automates the testing of the Chat Translator application using Playwright and Excel for test case management.

## 🚀 Getting Started

Follow these steps to set up and run the automation script.

### 1. Prerequisites (One-time Setup)

Ensure you have the following installed on your system:
- **Python 3.11 or 3.12**: [Download Python](https://www.python.org/downloads/)
- **Google Chrome** (Recommended) or let Playwright install Chromium.

### 2. Project Environment Setup

1.  **Extract the Project**: Save the provided ZIP file to your `D:` drive and extract it.
2.  **Open Command Prompt**: Press `Win + R`, type `cmd`, and press Enter.
3.  **Navigate to Project**:
    ```cmd
    cd /d D:\test_automation
    ```

### 3. Install Dependencies

From the `D:\test_automation` directory, run the following commands:

```cmd
pip install -U pip
pip install playwright openpyxl
playwright install
```

### 4. Prepare Test Cases

1.  Open `IT23157446.xlsx` located in the project folder.
2.  Fill in the following columns with your test data:
    - `TC ID`
    - `Input length type`
    - `Input`
    - `Expected output`
3.  **Important**: Do NOT enter any values under the `Actual output` and `Status` columns; these will be filled automatically.

### 5. Run the Automation Script

Execute the following command in your Command Prompt:

```cmd
python test_automation.py --excel "IT23157446.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

> [!NOTE]
> Adjust the path if your Excel file is in a different location (e.g., `"data/IT23157446.xlsx"`).

### 6. Verify Results

1.  Navigate to the project folder.
2.  Reopen the `IT23157446.xlsx` file.
3.  Verify the values automatically recorded under the `Actual output` and `Status` columns.

### 7. Documentation & Assessment

After reviewing the results, add the following two columns next to the `Status` column:
- `Singlish input types covered`
- `Evidence or rationale for the input type covered`

Manually fill in these values based on your assessment, referring to the template provided in **Appendix 2** of the assignment document for guidance.

---

## 🛠 Command Arguments Explained

| Argument | Description |
| :--- | :--- |
| `--excel` | Path to the Excel file containing test cases. |
| `--url` | The URL of the application to test. |
| `--wait-ms` | Time to wait (in ms) for the translation to complete. |
| `--type-delay-ms` | Delay (in ms) between each keystroke. |
| `--slow-mo-ms` | Slows down Playwright operations by the specified amount. |
| `--save-every` | Saves the Excel file after every 'n' test cases. |
| `--keep-open` | Keeps the browser window open after execution. |
