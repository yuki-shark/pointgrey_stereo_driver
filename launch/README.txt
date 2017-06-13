Date: 2017/5/19
Place: 73B2

getting rostopic list
/pointgrey/left/camera_info
/pointgrey/left/image_raw
/pointgrey/right/camera_info
/pointgrey/right/image_raw

bagfile data
-------------------------------------------------------------------
 bagfile        distance(m)     up/down         right/left      hz  
 001.bag        4               up              center          60
 002.bag        4               cdenter         center          60
 003.bag        4               down            center          60
 004.bag        miss
 005.bag        4               up              center          60
 006.bag        4               center          right           60
 007.bag        miss
 008.bag        miss
 009.bag        4               center          right           60
 010.bag        miss
 011.bag        4               center          right           60
 012.bag        4               up              left            60
 013.bag        4               up              left            60
 014.bag        4               center          right           60
 015.bag        miss
 016.bag        miss
 017.bag        miss
 018.bag        4               up              center          60
 019.bag        miss
 020.bag        miss
-------------------------------------------------------------------

'miss' means failing to get clear image data


*USAGE*

fix "rosbag_play.launch" l8
"args="$(find pointgrey_stereo_driver)/bagfile/$(arg bagfile) --clock --loop""
modify your bagfile's path

       roslaunch rosbag_play.launch bagfile:=001.bag

