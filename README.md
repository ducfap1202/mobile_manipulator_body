Yêu cầu cơ bản:
- cài code teleop keyboard

        sudo apt-get install ros-noetic-teleop-twist-keyboard
  
cách chạy code: 

bắt đầu nhập lệnh trong ubuntu:

    cd catkin_ws/src
  
    git clone https://github.com/ducfap1202/mobile_manipulator_body.git
  
    cd ..
  
    catkin_make
  
    cd
        
Sau khi tải và load shader robot, ta có thể chạy theo nhu cầu của bản thân 
theo các option dưới đây

Option 1: vào rviz

    roscd mobile_manipulator_body/urdf
  
  
    roslaunch urdf_tutorial display.launch model:=robot_base.urdf
  
Option 2: mở thêm 1 ubuntu 20.04 mới và chạy gazebo

    cd ~/catkin_ws/
  
    roslaunch mobile_manipulator_body base_gazebo_control.launch
  
Option 3: chạy gazebo + map 3d
    
    roslaunch mobile_manipulator_body map.launch

  
mở thêm 1 ubuntu 20.04 mới để mở bảng điều khiển robot bằng bàn phím

    rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/robot_base_velocity_controller/cmd_vel

Know issues:
    - camera: chỉ chạy robot không thì camera + cảm biến lidar hoạt động ngon
                còn chạy với map thì chỉ cảm biến lidar hoạt động
