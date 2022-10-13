# LiDAR_Intrinsics_Calib_While_Mapping
## Sensor Setup
LiDAR: Velodyne VLP-32C

IMU: ADIS16505-2, 2000HZ

We use a customized metal frame to fix LiDAR and IMU tightly together. Mapping drift is evaluated against GNSS/RTK trajectory.
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/hardware/sensor_setup.jpg" width = "1080" align=center />

## Recalib LiDAR Intrinsics
We build map of surroundings while the car is moving. the same surface element can be observed many times by differnt laser line in different distance. We estimate 
LiDAR intrinsics by minimize observation difference.

## Reducing mapping drift

experiment on our dataset 
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_track/ZJG01_result.png" width = "1080" align=center />

experiment on KITTI-RAW dataset
| KITTI-09-30-0020 | KITTI-10-03-0042 |
|  ----  | ----  |
| <img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/Kitti/map_track/KITTI-09-30-0020.png" width = "540" align=center /> | <img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/Kitti/map_track/KITTI-10-03-0042.png" width = "540" align=center /> |

## Improving map details

<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/road_slice_view_no_calib.png" width = "1080" align=center />
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/road_slice_view_after_calib.png" width = "1080" align=center />
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/wall_top_view_no_calib.png" width = "1080" align=center />
<img src="https://github.com/liuxiyao123/LiDAR_Intrinsics_Calib_While_Mapping/blob/main/doc/MyDataset/map_detail/wall_top_view_after_calib.png" width = "1080" align=center />
