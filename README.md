# ID Generator and Validator

## Overview

This repository contains a Python script for generating fake IDs and validating them by extracting information from PDF-based ID documents. It utilizes Optical Character Recognition (OCR) with Tesseract and various image processing libraries to manipulate and analyze ID documents.

## Code Overview

### 1. Libraries Installation

Make sure to have the following Python libraries installed:
- `pytesseract`
- `pdf2image`
- `faker`
- `PIL` (Pillow)
- `opencv-python`

### 2. Fake ID Generator

#### Steps:
1. **Extract Information**:
   - Use `pytesseract` to extract text from images or PDF pages.
   - Extract specific fields like name and expiration date using regular expressions.

2. **Generate Random Information**:
   - Create random names and expiration dates using the `faker` library.

3. **Overlay Text on Image**:
   - Modify images by overlaying new names and expiration dates on the existing ID images, effectively replacing old information.

4. **Save as PDF**:
   - Save the modified images as PDF files.

### 3. Extraction and Matching

#### Steps:
1. **Extract Text from PDF**:
   - Extract text from PDF files and process the images or PDF content for validation.

2. **Extract Employee Information**:
   - Extract name and expiry date from the processed text.

3. **Match and Validate**:
   - Compare extracted information with ticket details (name and expiry) to validate authenticity.

## Example Usage

pdf_path = "path/to/your/file.pdf"  
ticket_first_name = "RAYAN"  
ticket_father_initial = "N"  
ticket_last_name = "BESHAWRI"  
ticket_julian_expiry = "24221"  

result = main(pdf_path, ticket_first_name, ticket_father_initial, ticket_last_name, ticket_julian_expiry)  
print(result)

## Requirements

- `pytesseract`
- `pdf2image`
- `faker`
- `PIL` (Pillow)
- `opencv-python`
