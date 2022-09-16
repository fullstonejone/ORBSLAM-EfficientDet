# ORBSLAM-EfficientDet
Modify ORBSLAM to add dynamic object culling using EfficientDet
## ORBSLAM
SLAM(Simultaneous positioning and mapping)
在机器人、无人驾驶领域广泛使用的技术，其目的使带有相机或激光雷达的设备，恢复在位置环境中的运动状态，并通过匹配关系建立地图，供无人机、车等实现路径规划、碰撞检测、无人驾驶等任务。
ORBSLAM 使基于特征(ORB特征)的SLAM系统，可在大小型室内外环境中实时运行。


## EfficientDet

## Moving points culling


## run step
> TUM/rgbd_dataset_freiburg3_walking_xyz：

./Examples/RGB-D/rgbd_tum Vocabulary/ORBvoc.txt Examples/RGB-D/TUM3.yaml path/to/rgbd_dataset_freiburg3_walking_xyz path/to/associate.txt detect_result/TUM_f3xyz_yolov5m/detect_result/

