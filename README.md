Steps:
1. Install packages:
    ROS (tested with Kinetic and Melodic)

        sudo apt-get install ros-noetic-navigation
        sudo apt-get install ros-noetic-robot-localization
        sudo apt-get install ros-noetic-robot-state-publisher

    gtsam (Georgia Tech Smoothing and Mapping library)
    

        sudo add-apt-repository ppa:borglab/gtsam-release-4.0
        sudo apt update
        sudo apt install libgtsam-dev libgtsam-unstable-dev

    ceres
        http://ceres-solver.org/installation.html        
        
2. git clone under /catkin_ws/src
3. catkin_make under /catkin_ws
4. Download sample datasets: see https://github.com/TixiaoShan/LIO-SAM
5. Run packages & play bag files(dataset):
```
    roslaunch lio_sam run.launch
    rosbag play your-bag.bag -r 3
```   
Note: If the simulation is lagging, reduce the playback time from 3 to 1 or 2

The parameters in paras.yaml are modified to fit the KITTI dataset.
For other dataset, see the original git website. 

For the Scan Context LIO SAM, please change the branch accordingly. The Scan Context evaluation is based on the framework of https://github.com/gisbi-kim/SC-LIO-SAM
