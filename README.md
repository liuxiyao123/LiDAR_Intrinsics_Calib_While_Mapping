# LiDAR_Intrinsics_Calib_While_Mapping
## Sensor Setup
LiDAR: Velodyne VLP-32C

IMU: ADIS16505-2, 2000HZ

We use a customized metal frame to fix LiDAR and IMU tightly together. Mapping drift is evaluated against GNSS/RTK trajectory.
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/hardware/sensor_setup.jpg" width = "1440" align=center />

## Recalib LiDAR Intrinsics
LiDAR intrinsics tends to drift slowly due to aging, vibration and temperature change. Inaccurate intrinsics leads to unsatisfactory mapping result such as blurry detail and higher drift.

When building map of surrounding environment, the same surface element can be observed many times by differnt laser line from different distance. We iteratively adjust intrinsics to decrease observation difference and building remaining map with new intrinsics.

## Reducing map drift

experiment on our dataset 
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_track/ZJG01_result.png" width = "1440" align=center />

experiment on KITTI-RAW dataset
| KITTI-09-30-0020 | KITTI-10-03-0042 |
|  ----  | ----  |
| <img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/Kitti/map_track/KITTI-09-30-0020.png" width = "900" align=center /> | <img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/Kitti/map_track/KITTI-10-03-0042.png" width = "900" align=center /> |

## Improving map details

Pointcloud colored by lasar line number.
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/road_slice_view_no_calib.png" width = "1800" align=center />
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/road_slice_view_after_calib.png" width = "1800" align=center />
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/wall_top_view_no_calib.png" width = "1800" align=center />
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/wall_top_view_after_calib.png" width = "1800" align=center />

| laser line with largest deviation | after intrinsics recalib |
|  ----  | ----  |
| <img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/no_calib.png" width = "900" align=center /> | <img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/after_calib.png" width = "900" align=center /> |
