# UR5e-YOLO-Vision-Integration


# Steps to launch the system
- Launch the Camera 
  - ros2 launch realsense2_camera rs_pointcloud_launch.py
  - ros2 launch realsense2_camera rs_pointcloud_launch.py rgb_camera.color_profile:=1280x720x6 
  
- Launch UR5e
  - ros2 launch ur_robot_driver ur_control.launch.py ur_type:=ur5e robot_ip:=158.125.191.88 [Lboro University IP]

- Launch the YOLOv8 node
  - ros2 run confid_subpub confid_subpub

- Launch the main node for the system
  - launch matlab: matlab -softwareopengl
  - publish topic into: /urscript_interface/script_command 