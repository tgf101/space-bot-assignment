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
- Sample JSON response (formatted example) 
