# Welcome to Fylik API Documentation

Fylik API is backend system for [Fylik Project](https://fylik.ru/about).

Fylik has open source code and public REST API. You can download these sources or use hosted Fylik API in your projects.

## Requirements

- Debian based machine;
- NodeJS & yarn installed;
- MongoDB installed;

## Installation

1. Clone [this repository](https://github.com/aleoheen/fylik-server) to your local machine;

2. Install all dependencies executing `yarn install`

## Configuring

Create an .env file in root directory and fill it:

| Parameter | Description | Additional info | Example |
|------------------------------|----------------------------------------------------------|-----------------|-----------------------------------------------|
| HTTP_IP | HTTP Server IP |  | 127.0.0.1 |
| HTTP_PORT | HTTP Server Port |  | 8011 |
| MAX_FILE_SIZE | Max upload file size | In megabytes | 100 |
| MAX_FILES_AMOUNT | Max upload files amount per IP |  | 5 |
| MIN_FILE_TERM, MAX_FILE_TERM | Upload file terms. Generating randomly every file upload | In seconds | 180 1800 |
| FILE_STORAGE_SIZE | Size in megabytes available for all uploaded files | In megabytes | 10240 |
| UPLOAD_DIR | Directory where uploaded file located in | Absolute path | /home/alexander/projects/fylik-server/uploads |
| FILE_BASE_URL | Main URL for Fylik API |  | https://api.fylik.ru |
| DB_NAME | MongoDB Database name |  | fylik |
| DB_HOST | MongoDB host |  | 127.0.0.1:27017 |

## Running API

### In production mode

`yarn start`

### In development mode

`yarn run debug`