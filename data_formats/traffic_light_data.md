#### Traffic light signal data format:

---
**Light color state coding:**

| State code | Color |
|:----------:|:-----:|
| 2  | yellow-blinking |
| 4  | green |
| 10 | red |
| 11 | disabled |
| 20 | yellow |
| 30 | red-yellow |

---
**Status data:**
 - _ts_ : Timestamps are in UTC data format
 - _k1-k6_ : Vehicle lane and driving direction signals
 - _f1-f3_ : The three signalized pedestrian crossings signals
 - _b1-b3_ : Not relevant

---
```
{
    "overview": 
    {
        "first_ts": val (int)
        "last_ts": val (int)
        "duration": val (int)
    },
    "status_data": 
    {
        "ts": 
        {
            "k1": val (int)
            "k2": val (int)
            "k3": val (int)
            "k4": val (int)
            "k5": val (int)
            "k6": val (int)
            "f1": val (int)
            "f2": val (int)
            "f3": val (int)
            "b1": val (int)
            "b2": val (int)
            "b3": val (int)
        },
        "ts":
        {
            ...
        },
        "ts":
        {
            ...
        }
    }
}
```
---