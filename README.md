# NPS-Admission-form-auto-application-numbering

# NPS Admission Form Number Automation

## Overview

This Python script automatically generates numbered Nalanda Public School Admission Application Forms.

For each admission number:

* Page 1 = Application form with admission number printed automatically.
* Page 2 = Application form second page.
* Both pages are combined into a single PDF.
* No intermediate PDF files are created.
* The output file name is generated automatically based on the admission number range.

---

## Script Name

```text
NPS_Admission_form_no_automation.py
```

---

## Required Files

Place the following files in the same folder as the Python script:

```text
Application_form.pdf
Application_form_page2.pdf
NPS_Admission_form_no_automation.py
```

### File Description

#### Application_form.pdf

First page of the admission form.

The admission number will be printed automatically on this page.

#### Application_form_page2.pdf

Second page of the admission form.

This page will be inserted after every numbered first page.

---

## Required Python Libraries

Install once:

```bash
pip install reportlab PyPDF2
```

or in Google Colab:

```python
!pip install reportlab PyPDF2
```

---

## How to Use

Open the Python script and edit only the following section:

```python
start_number = 2201
end_number = 2300
```

### Example 1

```python
start_number = 2201
end_number = 2300
```

Output:

```text
New Admission Application Form 2201 to 2300.pdf
```

---

### Example 2

```python
start_number = 2301
end_number = 2400
```

Output:

```text
New Admission Application Form 2301 to 2400.pdf
```

---

## Admission Number Position

If the admission number is not perfectly aligned, adjust:

```python
x_position = 65
y_position = 697
```

### Horizontal Position

```text
Increase X = Move Right
Decrease X = Move Left
```

### Vertical Position

```text
Increase Y = Move Up
Decrease Y = Move Down
```

---

## Font Settings

Current settings:

```python
font_name = "Courier-Bold"
font_size = 18
```

Courier-Bold is used to create a bold typewriter-style appearance.

---

## Output Structure

Example:

```text
2201 - Page 1
Application Form Page 2

2202 - Page 1
Application Form Page 2

2203 - Page 1
Application Form Page 2
```

---

## Output File Naming

The script automatically creates the file name:

```text
New Admission Application Form START_NUMBER to END_NUMBER.pdf
```

Example:

```text
New Admission Application Form 2201 to 2300.pdf
```

---

## Number of Pages Generated

Formula:

```text
Total Pages = Number of Forms × 2
```

Example:

```text
2201 to 2300
= 100 Forms

100 × 2
= 200 Pages
```

---

## Recommended Workflow

1. Keep all files in one folder.
2. Change only:

```python
start_number
end_number
```

3. Run the script.
4. Verify the generated PDF.
5. Print the PDF.

---

## Version

Nalanda Public School
Admission Form Number Automation
Version 1.0
