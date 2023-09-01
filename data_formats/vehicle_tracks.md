#### Single vehicle track data format:

---
**Class ids:**

| Class ID | Class name | color  |
|:--------:|:----------:|:------:|
|     7    | Car        | brown  |
|     8    | Truck/Bus  | orange |

---
**Track data:**
 - _ts_ : Timestamps are in UTC data format
 - _cuboid_: Object enclosing cuboid. The cuboid data is represented by its 12 edges. Every edge is described by its two connecting 3d points like this: [ [x1, y1, z1], [x2, y2, z2] ]
 - _coordinates_: Track 3d coordinates in intersection coordinate system in meters (m)
 - _volume_: Cuboid volume of object in cubic meter (m³)
 - _velocity_: Velocity of object in kilometers per hour (kmh)
 - _ground_type_: Track ground classification
 - _z_offset_: Track height offset to intersection coordinate system origin


---
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
            "cuboid": list [[[x, y, z], [x, y, z]], [[x, y, z], [x, y, z]], ...] (float)
            "coordinates": list [x, y, z] (float)
            "volume": val (float)
            "velocity": val (float)
            "ground_type": val (int)
            "z_offset": val (float)
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