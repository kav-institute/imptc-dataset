#### Weather data format:

---
#### Weather status coding:

| State code | Weather type |
|:----------:|:------------:|
| 0 | sunny_cloudy |
| 1 | light_rain |
| 2 | strong_rain |
| 3 | foggy |
| 4 | snowy |

---
**State data:**

 - _ts_ : Timestamps are in UTC data format
 - _air_pressure_ : Air pressure in hectopascal (hPa)
 - _air_temperature_ : Air temperature in degree celsius (°C)
 - _relative_humidity_ : Humidity in percent from 0% till 100%
 - _wind_speed_ :  Wind speed in (m/s)
 - _wind_direction_ : Wind direction in degree (°)
 - _precipitation_intensity_ : Percipitation Intensity 
 - _precipitation_amount_ : Percipitation type, 0 => None, 1 => Rain, 2 => Snow  
 - _visibility_ : Overall visibility from 0 till 2000 meters in (m)
 - _weather_nws_ : not relevant
---

```
{
    "overview": 
    {
        "first_ts": val (int)
        "last_ts": val (int)
        "duration": val (int)
        "status": val (int)
        "name": val (string)
    },
    "weather_data": 
    {
        "ts_0": 
        {
            "air_pressure": val (float)
            "air_temperature": val (float)
            "relative_humidity": val (float)
            "wind_speed": val (float)
            "wind_direction": val (float)
            "precipitation_intensity": val (float)
            "precipitation_amount": val (float)
            "visibility": val (float)
            "weather_nws": val (int)
        },
        "ts_1":
        {
            ...
        },
        "ts_2":
        {
            ...
        }
    }
}
```
---