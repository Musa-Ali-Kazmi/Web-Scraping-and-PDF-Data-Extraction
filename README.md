# Web-Scraping-and-PDF-Data-Extraction
This Python script performs PDF and web data scraping, transforms the extracted data, stores it in a database, and provides API endpoints for data storage and downloading

### Purpose:
This Python script performs PDF and web data scraping, transforms the extracted data, stores it in a database, and provides API endpoints for data storage and downloading.

### Dependencies:
- `tabula-py`: For extracting data from PDF files.
- `requests`: For sending HTTP requests to web pages.
- `beautifulsoup4`: For parsing HTML content during web scraping.
- `pandas`: For data manipulation and transformation.
- `sqlalchemy`: For interacting with the database.
- `Flask`: For creating API endpoints.
- `openpyxl`: For working with Excel files.

### Usage:
1. Install the required dependencies by running `pip install tabula-py requests beautifulsoup4 pandas sqlalchemy Flask openpyxl`.
2. Replace the placeholder functions and variables with your specific implementation details.
3. Run the script.

### Step-by-Step Guide:

1. **PDF Data Extraction using Scraping API (`extract_data_from_pdf`):**
   - Utilizes Tabula to extract tables from PDF files.
   - Parameters:
     - `pdf_path`: Path to the PDF file.
   - Returns:
     - Cleaned and processed DataFrame containing the extracted data.

2. **Web Scraping for Additional Data (`scrape_additional_data`):**
   - Scrapes additional data from a specified URL using BeautifulSoup.
   - Parameters:
     - `url`: URL of the webpage to scrape.
   - Returns:
     - Extracted additional data.

3. **Data Transformation (`process_and_clean_data`):**
   - Processes and cleans the extracted data.
   - Parameters:
     - `tables`: List of DataFrame tables extracted from PDF.
   - Returns:
     - Unified and cleaned DataFrame.

4. **Database API Interaction (`store_data_in_database`):**
   - Stores the transformed data into a specified database.
   - Parameters:
     - `dataframe`: DataFrame containing the transformed data.
     - `db_url`: URL or connection string of the database.
   - Database Table:
     - Creates or replaces a table named 'data_table' in the database.

5. **API Endpoint for Data Storage (`/store_data`):**
   - Provides an endpoint for storing data in the database via POST request.
   - URL: `/store_data`
   - Method: POST
   - Request Body: JSON format containing the data to be stored.

6. **Download Button for Excel File (`/download_excel`):**
   - Provides an endpoint for downloading the transformed data as an Excel file.
   - URL: `/download_excel`
   - Method: GET
   - Returns:
     - Excel file as a downloadable attachment.

7. **Error Handling and Logging:**
   - Implements basic error handling and logging using the `logging` module.
   - Logs are stored in the `app.log` file.

### Additional Considerations:
- Ensure proper error handling and logging for debugging and monitoring purposes.
- Customize the code according to specific requirements, such as file paths, URLs, database configurations, and API endpoints.
- Test the script thoroughly with various PDF structures, web pages, and database interactions to ensure functionality and reliability.

---

This documentation provides an overview of the script's purpose, dependencies, usage instructions, step-by-step guide, and additional considerations. Adjustments may be needed based on your specific use case and environment.
