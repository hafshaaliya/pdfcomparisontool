# pdf-comparison-tool
A comprehensive web application for comparing two PDF documents and visualizing their differences. Built with Python and Flask, this tool provides both a user-friendly web interface and a robust backend for detailed PDF analysis.
Features

Text Extraction & Comparison: Extract and compare text content from PDFs page by page
Metadata Comparison: Identify differences in PDF metadata properties
Similarity Scoring: Calculate overall similarity percentage between documents
Interactive UI: Modern, responsive web interface with:

Drag-and-drop file uploads
Color-coded difference highlighting
Page-by-page navigation
Toggle to show/hide unchanged content
Detailed summary statistics



Screenshots
![Screenshot (26)](https://github.com/user-attachments/assets/fa3930b8-70b7-4dfb-b356-08a5a82898a7)

![image](https://github.com/user-attachments/assets/33cb81cf-90ce-4db8-84cd-b4f34dd54986)

![image](https://github.com/user-attachments/assets/befa8863-7a5f-4e16-b461-002892bed0b1)






Requirements

Python 3.7+
Flask
PyPDF2
PyMuPDF (fitz)
Werkzeug

Usage

Upload PDFs: Drag and drop or browse to select two PDF files for comparison
Compare: Click the "Compare PDFs" button to start the analysis
Review Results:

See the overall similarity score
Review metadata differences in the table
Navigate through pages using the tab interface
Toggle the display of unchanged content as needed



How It Works
Backend
The tool uses a multi-stage process for PDF comparison:

PDF Text Extraction: Uses PyMuPDF (fitz) to extract text from each page of both PDFs
Difference Analysis: Applies Python's difflib to identify added, removed, and unchanged lines
Metadata Extraction: Uses PyPDF2 to extract and compare document metadata
Similarity Calculation: Computes an overall similarity score based on common content

Frontend
The web interface is built with:

Flask: Handles routing and server-side operations
Bootstrap 5: Provides responsive and attractive UI components
JavaScript: Manages interactive elements like file uploads and toggle switches

API Endpoints

GET /: Main page with upload interface
POST /compare: Submit two PDFs for comparison
GET /results/<comparison_id>: View comparison results
GET /api/comparison/<comparison_id>: JSON API for retrieving comparison data

Limitations

Works best with text-based PDFs; image-only PDFs may not yield meaningful comparisons
Large PDFs (>16MB) require adjusting the MAX_CONTENT_LENGTH configuration
Complex document layouts might affect text extraction accuracy

Future Improvements

Visual comparison of PDF pages (image-based diff)
Highlighting specific changes within lines instead of whole-line replacement
Export comparison results as PDF or HTML report
Batch processing for multiple document comparisons
User accounts for saving comparison history

Bootstrap for the UI framework
PyMuPDF and PyPDF2 for PDF processing capabilities
The Flask team for the web framework

Contact
mohammadhafshaaliya@gmail.com
# pdfcomparisontool
