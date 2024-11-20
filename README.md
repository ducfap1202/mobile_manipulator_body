cách chạy code: 

bắt đầu nhập lệnh trong ubuntu:

    cd catkin_ws/src
  
    git clone https://github.com/ducfap1202/mobile_manipulator_body.git
  
    cd ..
  
    catkin_make
  
    cd
  
bắt đầu vào rviz

    roscd mobile_manipulator_body/urdf
  
  
    roslaunch urdf_tutorial display.launch model:=robot_base.urdf
  
mở thêm 1 ubuntu 20.04 mới và chạy gazebo

    cd ~/catkin_ws/
  
    roslaunch mobile_manipulator_body base_gazebo_control.launch
  
mở thêm 1 ubuntu 20.04 mới để mở bảng điều khiển

điều khiển bằng bàn phím

    rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/robot_base_velocity_controller/cmd_vel
    
mở world + robot gazebo 

    roslaunch mobile_manipulator_body tett.launch
