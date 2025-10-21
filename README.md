# Project Name: Baby Names Data Processing

## Overview
This project automates the process of downloading baby names data from Kaggle, storing it in a MySQL database, and creating contacts in HubSpot.

## Setup Instructions

1. **Clone the repository**
   ```
   git clone <repository-url>
   cd node+typeScript/play
   ```

2. **Install dependencies**
   ```
   npm install
   ```

3. **Configure environment variables**
   - Create a `.env` file in the root directory.
   - Add the following variables:
     ```
     DB_NAME=your_database_name
     DB_USER=your_database_user
     DB_PASS=your_database_password
     DB_HOST=your_database_host
     HUBSPOT_API_KEY=your_hubspot_api_key
     ```

4. **Run database migrations**
   Ensure your MySQL database is set up and ready to accept connections.

## Run Instructions

1. **Download the Dataset from Kaggle**
   - Navigate to the Kaggle dataset page using the script:
     ```
     npx ts-node src/downloadKaggleData.ts
     ```
   - Manually log in to Kaggle when prompted to allow the script to download the dataset.

2. **Process and Store Data**
   - Parse the CSV, store the data in MySQL, and create HubSpot contacts:
     ```
     npx ts-node src/processAndStoreData.ts
     ```

## Dependencies
- TypeScript
- Playwright
- csv-parser
- axios
- Sequelize
- dotenv

## Notes
- Ensure your Kaggle credentials and database configuration are correct in the `.env` file.
- The script requires manual intervention for logging into Kaggle to download the dataset.
