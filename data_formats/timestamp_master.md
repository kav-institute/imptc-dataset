#### Master Timestamp data format:

---
**Master ts data:**
 - _ts_ : Timestamps are in UTC data format
 - _id_ : ID of timestamp compared to first ts, start counting from 0
 - _weather_data_ : Flag to indicate if a weather data update is available, update rate is every 10 seconds
 - _traffic_lights_data_ : Flag to indicate if a traffic light signal data update is available, update rate is every second

---
```
{
    "ts_0": 
    {
        "id": val (int)
        "weather_data": val (bool)
        "traffic_lights_data": val (bool)
    },
    "ts_1": 
    {
        "id": val (int)
        "weather_data": val (bool)
        "traffic_lights_data": val (bool)
    },
    ...
}
```
---