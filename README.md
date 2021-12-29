# Dataset for Spatiotemporal Registration for Event-based Visual Odometry
The RobotEvt dataset contains sequences under different motion models, speeds and brightness from a static scene, specifically
 - 4 motion models: PureRot - pure rotation; ParRot partial rotation; PureTranslate - pure translation and FullMod - full rigid motion model.
- 3 speeds: Fast - maximum speed of the robot arm (1m/s); Mid - 75% of the maximum speed and Slow - 50% of the maximum speed.
- 2 brightness conditions: On and Off means bright and dark conditions, respectively.

![UR5 robot arm with DAVIS 240C event camera, and sample APS image and event image captured with our setup.](https://github.com/liudaqikk/RobotEvt/blob/main/robot_setup.png?raw=true)
 
This dataset were recored with a [DAVIS240C](https://inivation.com/wp-content/uploads/2019/08/DAVIS240.pdf), attatched on the endpoint of a UR5 robot arm. Ground truth were generated from the UR5 robot arm.
# Dataset format!
Events, raw images and IMU measurements are stored in the [rosbag](http://wiki.ros.org/rosbag) file.
- **dvs/events**: event information (timestamp x y polarity).
- **dvs/images**: raw images at fix rate.
- **dvs/imu**: IMU measurement at fix rate. 

Ground truth are provided with a txt file, where the poses are represented using rotation matrix and translation. One pose per line (timestamp r11 r12 r13 r21 r22 r23 r31 r32 r33 t1 t2 t3) .

# Download links
Download link for Pure Rotation sequences can be downloaded [here](https://drive.google.com/drive/folders/1uhnCR2iDIEZhVNmL-2a-FWmo1J-Ip_vv?usp=sharing), which contains the measurement of events, raw images and IMU. 
More sequences with full rigid motion and higher resolution generated using [Prophesee cameras](https://www.prophesee.ai/) will be released soon.
# Citing
Please cite the following paper when using this datase for academic usage.

Daqi Liu, Álvaro Parra, Tat-Jun Chin. [Spatiotemporal registration for event-based visual odometry.](https://openaccess.thecvf.com/content/CVPR2021/papers/Liu_Spatiotemporal_Registration_for_Event-Based_Visual_Odometry_CVPR_2021_paper.pdf) Conference on Computer Vision and Pattern Recognition (CVPR) 2021
