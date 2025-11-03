# space-bot-assignment
## 1. Webex messaging API

- API base URL: https://webexapis.com/v1/rooms i used this to list rooms
- Authentication: Bearer Token
- Endpoints:
- Endpoint to list rooms: /rooms
- Endpoint to list messages: /messages
- Enpoint to send messages: /messages
- data format: JSON
## 2. ISS current location API
- API base URL: http://api.open-notify.org/iss-now.json
- Endpoint for current ISS Location: /iss-now.json
- Sample response format (Example JSON)
{
  "timestamp": 1762199960,
  "message": "success",
  "iss_position": {
    "latitude": "-37.4654",
    "longitude": "-45.4561"
  }
}
 

## Geocoding API
- API Base URL: http://api.openweathermap.org/geo/1.0
- Endpoint for reverse geocoding: /reverse
- Authentication method: API key appid
- Required query parameters: lat, lon,limit, appid
- Sample request with latitude/longitude: https://api.openweathermap.org/geo/1.0/reverse?lat=32.4541&lon=129.3857&limit=1&appid=d5955724d09243872fc64278f2d49abb
- Sample JSON response (formatted example):
- [
    {
        "name": "Nagasaki",
        "local_names": {
            "ml": "നാഗസാക്കി",
            "eo": "Nagasako",
            "de": "Nagasaki",
            "ascii": "Nagasaki",
            "sv": "Nagasaki",
            "zh": "长崎市",
            "nl": "Nagasaki",
            "uk": "Нагасакі",
            "ja": "長崎市",
            "no": "Nagasaki",
            "fr": "Nagasaki",
            "es": "Nagasaki",
            "en": "Nagasaki",
            "cs": "Nagasaki",
            "ar": "ناغاساكي، ناغاساكي",
            "da": "Nagasaki",
            "th": "นางาซากิ",
            "mr": "नागासाकी",
            "ur": "ناگاساکی",
            "hu": "Nagaszaki",
            "feature_name": "Nagasaki",
            "bn": "নাগাসাকি",
            "pl": "Nagasaki",
            "ca": "Nagasaki",
            "pt": "Nagasaki",
            "he": "נגסאקי",
            "lt": "Nagasakis",
            "ru": "Нагасаки",
            "ko": "나가사키",
            "hi": "नागासाकी",
            "et": "Nagasaki"
        },
        "lat": 32.7501611,
        "lon": 129.8781002,
        "country": "JP"
    }
]

## Epoch to human time conversion (Python time module)
- Library used: Time
- Function used to convert epoch: time.ctime()
- Sample code to to convert timestamp :
  import time
  epoch_time = 1762204269
  human_readable = time.ctime(epoch_time)
  print(human_readable)

## Web architecture & MVC design pattern
- Client: The python Space bot
- Server: The Webex API, ISS API, and geocoding API
- The communication between them is the client send HTTPS requests to the internet and then thats how we recieve these JSON responses. 
  
