Overview
=======
Fork of the madzak/python-json-logger library with additional features:
* support for static extra fields passed to the Formatter constructor
* support for custom format field names

JSON configuration example
=======
```javascript
    "formatters": {
        "json": {
            "()": "pythonjsonlogger.jsonlogger.JsonFormatter",
            "format": "%(asctime)s %(levelname)s %(name)s %(message)s",
            "datefmt": "%Y-%m-%d %H:%M:%S",
            "custom_format_field_names": {
                "asctime": "timestamp",
                "name": "subsystem",
                "levelname": "eventtype"
            },
            "static_fields": {
                "system": "smadapter",
                "host": "playmark"
            }
        },
        "human_readable": {
            "format": "%(asctime)s %(levelname)-7s %(name)-20s: %(message)s",
            "datefmt": "%Y-%m-%d %H:%M:%S"
        }
    }
```
