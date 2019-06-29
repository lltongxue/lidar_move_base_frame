# ros_lidar_ws

建图启动过程
启动雷达：roslaunch xdzn_rplidar rplidar.launch
启动底盘：roslaunch ros_arduino_python arduino.launch
启动建图：roslaunch xdzn_mapping robot_mapping.launch

导航过程启动
启动导航和rviz：roslaunch robot_navigation robot_nav.launch
清除里程：rosservice call /arduino/reset_odometry
启动速度平滑处理：roslaunch yocs_velocity_smoother velocity_smoother.launch

录制数据:首先进入录制包：cd bagfiles
                     开始录制所有话题：rosbag record -a
		     录制其中一个话题：rosbag record topic -name
打印速度到命令窗口：rostopic echo /cmd_vel
