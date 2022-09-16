# ORBSLAM-EfficientDet
**Modify ORBSLAM to add dynamic object culling using EfficientDet**

## ORBSLAM

**SLAM(Simultaneous positioning and mapping)**
在机器人、无人驾驶领域广泛使用的技术，其目的使带有相机或激光雷达的设备，恢复在位置环境中的运动状态，并通过匹配关系建立地图，供无人机、车等实现路径规划、碰撞检测、无人驾驶等任务。

ORBSLAM 使基于特征(ORB特征)的SLAM系统，可在大小型室内外环境中实时运行。该系统包含了所有SLAM系统共有的模块：跟踪（`Tracking`）、建图（`Mapping`）、重定位（`Relocalization`）、闭环检测（`Loop closing`）。由于ORB-SLAM系统是基于特征点的SLAM系统，故其能够实时计算出相机的轨线，并生成场景的稀疏三维重建结果。**ORB-SLAM2**在ORB-SLAM的基础上，还支持标定后的双目相机和RGB-D相机。

- **ORB-SLAM2系统流程：**

![这里写图片描述](https://img-blog.csdn.net/20161114115058814)

![img](https://img-blog.csdn.net/20161114115114018)

（1）跟踪（`Tracking`）
  这一部分主要工作是从图像中提取ORB特征，根据上一帧进行姿态估计，或者进行通过全局重定位初始化位姿，然后跟踪已经重建的局部地图，优化位姿，再根据一些规则确定新的关键帧。

（2）建图（`LocalMapping`）
  这一部分主要完成局部地图构建。包括对关键帧的插入，验证最近生成的地图点并进行筛选，然后生成新的地图点，使用局部捆集调整（Local BA），最后再对插入的关键帧进行筛选，去除多余的关键帧。

（3）闭环检测（`LoopClosing`）
  这一部分主要分为两个过程，分别是闭环探测和闭环校正。闭环检测先使用BOW进行探测，然后通过Sim3算法计算相似变换。闭环校正，主要是闭环融合和`Essential Graph`的图优化

## EfficientDet



## Moving points culling




## run step
> TUM/rgbd_dataset_freiburg3_walking_xyz：

./Examples/RGB-D/rgbd_tum Vocabulary/ORBvoc.txt Examples/RGB-D/TUM3.yaml path/to/rgbd_dataset_freiburg3_walking_xyz path/to/associate.txt detect_result/TUM_f3xyz_yolov5m/detect_result/

