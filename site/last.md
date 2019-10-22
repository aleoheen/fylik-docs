# Get last uploaded files (polling)

You can use long polling to subscribe uploaded files list updates.

Send GET requests to `https://api.fylik.ru/last`. __Note that Fylik API server will return you last 50 files__. Server will response you max one time per second.

You should get response like this:

	{
	    "code": 200,
	    "files": [
	        {
	            "name": "sublime.png",
	            "size": 168182,
	            "type": "image/png",
	            "uid": "eb58",
	            "link": "http://192.168.1.127:8001/dl/eb58",
	            "expires": 1571740828005,
	            "timestamp": 1571740321005
	        }
	    ],
	    "total": 1,
	    "now": 1571740720900
	}

Where:

| Parameter | Description | Additional info |
|-----------|---------------------------|-----------------|
| code | HTTP status code |  |
| files | Array of loaded files | Max 50 files |
| total | Amout of all loaded files |  |
| now | Current timestamp | In milliseconds |