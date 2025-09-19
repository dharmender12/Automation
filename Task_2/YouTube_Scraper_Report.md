# YouTube Scraper Report

## Objective
The objective of this task was to develop a scraper to extract specific details from YouTube videos, including video title, channel name, video description, publish date, and view count. The extracted data was to be stored in a structured format in Google Sheets for easy reference, with additional storage in JSON and Excel files.

## Implementation Details

### Tools and Technologies
- **Programming Language**: Python
- **Libraries**:
  - `googleapiclient.discovery`: For interacting with the YouTube Data API to fetch video details.
  - `pandas`: For data manipulation and exporting to Excel.
  - `gspread`: For integrating with Google Sheets.
  - `json`: For saving data in JSON format.
  - `oauth2client`: For Google Sheets authentication.
- **YouTube Data API**: Used to retrieve video metadata programmatically.
- **Google Sheets API**: Used to store data in Google Sheets.
- **Output Formats**: JSON file, Excel file, and Google Sheets.

### Scraper Functionality
The scraper was designed to:
1. **Authenticate with APIs**:
   - Utilized a YouTube Data API key for accessing video data.
   - Used OAuth 2.0 credentials for Google Sheets API to enable writing to a specified spreadsheet.
2. **Extract Data**:
   - Fetched video details (title, channel name, description, publish date, view count) for a list of specified YouTube video URLs or IDs.
   - Handled API quotas and errors to ensure robust data retrieval.
3. **Store Data**:
   - Saved the extracted data in a JSON file for raw storage.
   - Exported the data to an Excel file using `pandas` for structured offline access.
   - Uploaded the data to a Google Sheet for online access and collaboration.

### Data Structure
The extracted data was organized as follows:
- **Video Title**: The title of the YouTube video.
- **Channel Name**: The name of the channel that uploaded the video.
- **Video Description**: The description provided for the video.
- **Publish Date**: The date the video was published.
- **View Count**: The total number of views for the video.

The data was stored in the following formats:
- **JSON**: A file named `youtube_data.json` containing a list of dictionaries, each representing a video's details.
- **Excel**: A file named `youtube_data.xlsx` with columns for each data field.
- **Google Sheets**: A spreadsheet with a worksheet named "YouTube Data" containing the same columnar structure as the Excel file.

## Execution Summary
- **Data Collection**: The scraper successfully extracted data from the specified YouTube videos using the YouTube Data API.
- **Data Storage**:
  - The JSON file (`youtube_data.json`) was generated and saved locally, containing all extracted video details in a structured format.
  - The Excel file (`youtube_data.xlsx`) was created with a clean, tabular format for easy offline analysis.
  - The data was uploaded to a Google Sheet, accessible via a shared link, ensuring easy reference and collaboration.
- **Error Handling**: The scraper included error handling for invalid video IDs, API quota limits, and authentication issues to ensure reliability.
- **Performance**: The scraper processed the videos efficiently, with execution time dependent on the number of videos and API response times.

## Challenges and Solutions
- **API Quota Limits**: The YouTube Data API has daily quota limits. To mitigate this, the scraper was designed to batch requests and handle quota-exceeded errors gracefully by pausing and retrying.
- **Authentication**: Setting up Google Sheets API authentication required OAuth 2.0 credentials. A `credentials.json` file was used, and a token was generated for seamless access.
- **Data Cleaning**: Some video descriptions contained special characters or lengthy text. The scraper truncated long descriptions and sanitized text to ensure compatibility with Excel and Google Sheets.

## Results
- **JSON Output**: The `youtube_data.json` file contains all extracted data in a structured, machine-readable format.
- **Excel Output**: The `youtube_data.xlsx` file provides a tabular view of the data, suitable for analysis in spreadsheet software.
- **Google Sheets Output**: The data was successfully uploaded to a Google Sheet, with columns for Video Title, Channel Name, Video Description, Publish Date, and View Count, accessible for real-time collaboration.

## Conclusion
The YouTube scraper was successfully developed and executed, meeting all requirements. It extracted the specified video details and stored them in JSON, Excel, and Google Sheets formats. The implementation is robust, handles errors effectively, and provides structured data for easy reference and analysis.