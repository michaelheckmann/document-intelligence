# Document Intelligence

This repository provides a pipeline for processing scanned images into organized, searchable PDF documents. The pipeline uses a combination of tools to achieve this:

- **[PDFKit](https://pdfkit.org/)**: This is a PDF generation library for Node that makes creating complex, multi-page, printable documents easy. In our pipeline, it is used to combine scanned images into a single PDF document.

- **[Tesseract.js](https://tesseract.projectnaptha.com/)**: This is a pure JavaScript port of the popular OCR engine, Tesseract. We use it to perform Optical Character Recognition (OCR) on the scanned images, converting them into searchable text that can be embedded in the PDF.

- **[Typechat](https://github.com/microsoft/TypeChat)**: This is a an LLM tool that is used as a wrapper for GPT-4. We use it to analyze the OCRed text and generate meaningful file names, short descriptions, and tags for the PDFs. This helps in better organization and retrieval of the documents.

The pipeline works as follows:

1. The user inputs scanned images.
2. The images are combined into a single PDF using PDFKit.
3. Tesseract.js performs OCR on the images, converting them into searchable text.
4. Typechat analyzes the text and generates file names, short descriptions, and tags for the PDF.
5. The PDF is saved with the generated file name and the descriptions and tags are stored for future retrieval.

This makes it easy to convert a pile of scanned documents into a well-organized, searchable digital library.
