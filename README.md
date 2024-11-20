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

    rosrun rqt_robot_steering rqt_robot_steering
  
  ![image](https://github.com/user-attachments/assets/e3a14f4c-fb96-473f-8c0f-c7558ef3780d)
  
bảng điều khiển sẽ như trên thì ta nhập thêm đoạn code này vào hộp thoại bên cạnh nút stop như trong hình

    /robot_base_velocity_controller/cmd_vel

điều khiển bằng bàn phím

    rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/robot_base_velocity_controller/cmd_vel
    
mở world + robot gazebo 

    roslaunch mobile_manipulator_body tett.launch
