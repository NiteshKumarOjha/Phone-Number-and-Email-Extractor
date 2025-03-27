# Phone Number and Email Extractor

## Overview
This Python script extracts phone numbers and email addresses from text copied to the clipboard. It uses regular expressions to identify and extract valid phone numbers and email addresses, then copies the extracted data back to the clipboard for easy use.

## Features
- Detects phone numbers with or without area codes.
- Supports various phone number formats (e.g., `123-456-7890`, `(123) 456-7890`, `123.456.7890`).
- Identifies phone numbers with extensions (e.g., `123-456-7890 x123`).
- Extracts valid email addresses.
- Copies the extracted contacts back to the clipboard for easy pasting.

## Prerequisites
Ensure you have Python installed on your system. This script requires the `pyperclip` module for clipboard operations.

### Install Dependencies
Run the following command to install `pyperclip`:
```bash
pip install pyperclip
```

## Usage
1. Copy any text containing phone numbers or email addresses.
2. Run the script:
   ```bash
   python phoneEmail.py
   ```
3. If valid phone numbers or emails are found, they will be copied to the clipboard.
4. Paste the extracted contacts anywhere (e.g., Notepad, Word, Terminal) using `Ctrl + V` (Windows/Linux) or `Cmd + V` (Mac).

## Code Explanation
The script consists of:
- **Regular expressions (`re`)**: Used to match phone numbers and email addresses.
- **Clipboard handling (`pyperclip`)**: Reads copied text and stores extracted contacts back into the clipboard.
- **Processing logic**:
  - Searches for phone numbers and emails in the copied text.
  - Formats and stores valid matches.
  - If matches are found, they are printed and copied to the clipboard.
  - If no matches are found, a message is displayed.

## Example Input & Output
### Input (Copied Text):
```
John's number is (123) 456-7890 and his email is john.doe@example.com.
Contact support at 987-654-3210 ext 55 or email support@company.org.
```

### Output (Copied to Clipboard):
```
123-456-7890
987-654-3210 x55
john.doe@example.com
support@company.org
```

## Contributions
Feel free to fork this repository, submit issues, or suggest improvements via pull requests!

