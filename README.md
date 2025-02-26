## Introduction

This project is an image processing system designed to handle CSV files containing product information and image URLs. The system performs the following tasks:

1. Validates and processes CSV files.
2. Asynchronously compresses images by 50%.
3. Stores product data and processed images in a database.
4. Provides an API to check processing status via a unique request ID.
5. Sends webhook notifications upon completion of image processing.

## Features

- Asynchronous image processing.
- CSV file validation.
- Database storage for product and request data.
- Webhook notifications upon task completion.
- API endpoints for uploading CSV files and checking processing status.

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Image Processing**: Sharp
- **HTTP Requests**: Axios

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/image-processing-system.git
   cd image-processing-system
   ```

## Configuration

1. Set up the MongoDB connection string in the `.env` file.
2. Configure the server port in the `.env` file.
3. Specify the webhook URL in the `.env` file to receive notifications upon image processing completion.

## Running the Application

1. Start the server:
   ```bash
   npm start
   ```
2. Run the worker script for image processing:
   ```bash
   node workers/processImages.js
   ```

## Error Handling

- Logs errors in processing CSV files and images.

- Provides meaningful error messages via API responses.

- Implements retries for failed image processing tasks.

## Future Improvements

- Implement authentication and authorization for API endpoints.

- Add support for additional image formats.

- Optimize database queries for better performance.

- Enhance webhook features with retry mechanisms.# process-image-data
