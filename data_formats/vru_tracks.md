#### Single vru track data format:

---
**Class ids:**

| Class ID | Class name | Color |
|:--------:|:----------:|:-----:|
|     0    | Pedestrian |  red  |
|     2    | Bicycle    | blue  |
|     3    | Motorcycle | green |
|     4    | Scooter    | gold  |
|     5    | Stroller   | pink  |
|     6    | Wheelchair | lime  |
|     10   | Unknown    | gray  |

---
**Track data:**
 - _ts_ : Timestamps are in UTC data format
 - _status_: Track classification status, 1 => Track Candidate, 2 => Accepted and valid track
 - _class_prob_: Probability of class identification in percantage 0-1
 - _coordinates_: Track 3d coordinates in intersection coordinate system in meters (m)
 - _velocity_: Velocity of object in kilometers per hour (kmh)
 - _ground_type_: Track ground classification
 - _z_offset_: Track height offset to intersection coordinate system origin
 - _source_type_: Which sensor(s) are responsible for current object detection, 0 => Lidar, 1 => lidar+camera, 2 => camera 

---
**Data format:**
```
{
    "overview": 
    {
        "first_ts": val (int)
        "last_ts": val (int)
        "length": val (int)
        "duration": val (int)
        "class_id": val (int)
        "class_name": val (string)
    },
    "track_data": 
    {
        "ts_0": 
        {
            "ts": val (int)
            "status": val (int)
            "class_prob": val (int)
            "coordinates": list [x, y, z] (float)
            "velocity": val (float)
            "ground_type": val (int)
            "z_offset": val (float)
            "source_type": val (int)
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