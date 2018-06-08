# Instllation

    cd ${YOUR_WORKSPACE}/src
    git clone https://github.com/yuki-shark/pointgrey_stereo_driver.git
    git checkout vt_perception
    cd ../
    catkin build
    
When *catkin build* fails, please install some dependant packages from source.

    sudo apt-get install ros-kinetic-jsk-perception ros-kinetic-jsk-pcl-ros ros-kinetic-jsk-pcl-ros-utils ros-kinetic-jsk-recognition
    catkin build
    
# Usage of color detection for Tiger

**bash 1**  
Start openni2 launch.

    roslaunch openni2_launch openni2.launch
    
**bash 2**

    source ${YOUR_WORKSPACE}/devel/setup.bash
    roslaunch pointgrey_stereo_driver hsv.launch
    
**bash 3**

    source ${YOUR_WORKSPACE}/devel/setup.bash
    rosrun pointgrey_stereo_driver centroid.py
    
If this python script do not work, please try following commands.

    cd ${YOUR_WORKSPACE}/src/pointgrey_stereo_driver/scripts
    ./centroid.py

If you want to change hsv color filter threshould, please change values in *hsv.launch*.
