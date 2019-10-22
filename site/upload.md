# Uploading files

You can upload any file to Fylik API. But before it you should check upload limits

## File upload limits

Send GET request to `https://api.fylik.ru/limits`.

You'll receive limits in JSON format.

	{
	    "max_files_amount": 5,
	    "max_file_size": 100
	}

## Upload a file

Send POST request to `https://api.fylik.ru/upload` with your file as _file_ parameter.

You should get response like this:

	{
	    "code": 201,
	    "file": {
	        "name": "sublime.png",
	        "size": 168182,
	        "type": "image/png",
	        "uid": "eb58",
	        "link": "http://192.168.1.127:8001/dl/eb58",
	        "expires": 1571740828005,
	        "timestamp": 1571740321005
	    },
	    "now": 1571740321075
	}

Where:

| Parameter | Description | Additional info |
|----------------|------------------------------------------------------------|-----------------|
| code | HTTP status code |  |
| file.name | Name of uploaded file |  |
| file.size | Size of uploaded file (in bytes) |  |
| file.type | MIME type of uploaded file |  |
| file.uid | Unique file ID | In hex |
| file.link | Uploaded file download link |  |
| file.expires | Timestamp when uploaded file will be automatically removed | In milliseconds |
| file.timestamp | Timestamp when you uploaded the file | In milliseconds |
| now | Timestamp of now | In milleseconds |