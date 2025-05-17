# Data Processing Application Task3

This is a Python application for data processing and analysis. It provides a web interface for uploading data files, viewing basic statistics, and visualizing data distributions.

## Features
- Data loading and preprocessing (CSV and Excel files)
- Basic statistical analysis
- Data visualization
- Data transformation and cleaning
- User-friendly web interface (Flask)
- Dockerized for easy deployment

## Project Structure
- `main.py`: (Legacy) Main application entry point for CLI
- `app.py`: Flask web application entry point
- `data_processor.py`: Core data processing functionality
- `requirements.txt`: Project dependencies
- `data/`: Directory for input/output data files
- `data/sample_data.csv`: Sample CSV file for testing
- `templates/index.html`: Web interface template
- `Dockerfile`: Docker configuration
- `docker-compose.yml`: Docker Compose configuration
- `.dockerignore`: Docker build exclusions

## Setup & Running the Application

### Option 1: Using Docker (Recommended)
1. **Build and start the application:**
   ```bash
   docker-compose up --build
   ```
   This will build the Docker image and start the web server at [http://localhost:5000](http://localhost:5000).

2. **Access the web interface:**
   - Open your browser and go to [http://localhost:5000](http://localhost:5000)

### Option 2: Local Python Environment
1. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Flask application:**
   ```bash
   python app.py
   ```
4. **Access the web interface:**
   - Open your browser and go to [http://localhost:5000](http://localhost:5000)

## How to Test the Application

1. **Upload a Data File:**
   - Use the provided sample file: `data/sample_data.csv`
   - Or upload your own CSV or Excel file with at least one numeric column and a header row.

2. **Steps:**
   - Click "Choose File" in the web interface.
   - Select `sample_data.csv` from the `data` directory (or your own file).
   - Click "Upload and Process".

3. **View Results:**
   - The application will display basic statistics for numeric columns (e.g., Age, Salary).
   - A data distribution plot for the first numeric column will be shown.
   - A message will confirm that the processed data has been saved in the `data` directory (e.g., `processed_sample_data.csv`).

## Notes
- Supported file formats: `.csv`, `.xls`, `.xlsx`
- The application ignores empty columns, rows, and unnamed columns automatically.
- The processed data file will be saved in the `data` directory with a `processed_` prefix.
- For best results, ensure your data file has a header row and at least one numeric column.

## Example Data File (CSV)
```
Name,Age,Salary,Department
Alice,30,70000,Engineering
Bob,25,50000,Marketing
Charlie,35,90000,Sales
Diana,28,60000,Engineering
Ethan,40,120000,Management
```

---

If you have any issues or want to extend the application, feel free to ask! 