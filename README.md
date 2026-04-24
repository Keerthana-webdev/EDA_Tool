## EDA Tool
A web-based Exploratory Data Analysis (EDA) tool built with Flask that allows users to upload CSV or Excel files, automatically detect and clean data, generate visualizations, and export reports.

---

### Features
- **File Upload**: Support for CSV and XLSX file formats
- **Automatic Data Cleaning**: 
  - Detects numeric columns from text data
  - Handles missing values (mean for numeric, mode for categorical)
  - Limits analysis to first 5 numeric columns for performance
- **Data Visualization**: Generates histograms with KDE plots for numeric columns
- **Interactive Web Interface**: Clean, modern UI with responsive design
- **Export Options**:
  - Download cleaned CSV data
  - Generate and download PDF reports with tables and plots
- **Real-time Processing**: Processes files up to 1000 rows for quick analysis

---

### Project Structure
```
EDA-Tool/
├── app.py                 # Main Flask application
├── analyzer.py            # Alternative analyzer (not used in main app)
├── static/
│   ├── css/
│   │   └── report.css     # Styles for report template
│   └── output/             # Directory for generated output(plot images)
├── templates/
│   ├── index.html         # Main upload page
│   └── report_template.html # Results display page
├── uploads/               # Temporary upload directory
└── README.md              # Project Documentation
```
---

### Installation

#### Prerequisites
- Python 3.7+
- pip package manager

#### Dependencies
Install the required packages using the provided requirements.txt:
```bash
pip install -r requirements.txt
```
---

### Usage
1️⃣ **Start the application**:
   ```bash
   python app.py
   ```
2️⃣ **Access the web interface**:
   - Open your browser and navigate to `http://127.0.0.1:5000`
   - You'll see the main upload page

3️⃣ **Upload a file**:
   - Click "Choose File" and select a CSV or XLSX file
   - Click "Upload and Analyze"
   - The tool will process your data and display:
     - Data preview (first 20 rows)
     - Generated plots
     - Download links for cleaned CSV and PDF report

4️⃣ **Download results**:
   - Use "Download CSV" to get the cleaned dataset
   - Use "Download PDF" to get a comprehensive report

---

### API Endpoints
- `GET /` - Main page
- `POST /upload` - File upload and processing
- `GET /download_csv` - Download cleaned CSV
- `GET /download_pdf` - Download PDF report

---

### Future Enhancements
- Support for more file formats (JSON, Parquet)
- Additional plot types (scatter plots, box plots, correlation matrices)
- Statistical summary generation
- Data type detection improvements
- Batch processing capabilities
- User authentication and file management
- API endpoints for programmatic access

---

### Author

#### Keerthana S



