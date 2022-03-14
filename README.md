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
2. git clone under /catkin_ws/src
3. catkin_make under /catkin_ws
4. Download sample datasets: see https://github.com/TixiaoShan/LIO-SAM
5. Run packages & play bag files(dataset):
    roslaunch lio_sam run.launch
    rosbag play your-bag.bag -r 3
    
I've modified extrinsic and some related parameters in paras.yaml to fit KITTI dataset.
For other dataset, see the original git wesite.
