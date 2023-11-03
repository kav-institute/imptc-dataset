#### Ground plane / Segmentation map data format:

---
**Segmentation map coding:**

| Label ID | Color | Type |
|:----------:|:-----:|:-----:|
| 0  | [128,64,128] | road |
| 1  | [244,35,232] | sidewalk |
| 2 | [81,0,81] | ground |
| 3 | [150,100,100] | curb |
| 4 | [157,234,50] | road line |
| 5 | [229,165,10] | crosswalk |
| 6 | [98,160,234]| bikelane |
| 7 | [128,128,128] | unknown |

Map is available as .ply point cloud data with additional RGB label for each XYZ point. The coordinate system is the same as for the trajectory data.

!["Segmentation map"](ground_plane.png  "Segmentation map")
