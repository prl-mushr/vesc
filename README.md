# MuSHR VESC  
## (Derived from MIT VESC)

Contains the code for interfacing with the VESC hardware.

### Packages:
  - `vesc`: Metapackage
  - `vesc_ackermann`: Code for converting from Ackermann messages to VESC interpretable messages. Also has code for converting vesc responses to odometry.
  - `vesc_driver`: Code for sending messages to the VESC device file.
  - `vesc_main`: Launch files for the vesc code.
  - `vesc_msgs`: Contains only messages related to the VESC.

### API
For adjusting params see `vesc_main/config/`.
#### Publishers
Note, some topics are omitted because they are only published and subscribed to within the vesc. For more info `rosnode list.`

Topic | Type | Description
------|------|------------
/vesc/sensors/core | [vesc_msgs/VescStateStamped](https://github.com/prl-mushr/vesc/blob/master/vesc_msgs/msg/VescStateStamped.msg) | Barebones motor command
/vesc/sensors/servo_position_command | [std_msgs/Float64](http://docs.ros.org/api/std_msgs/html/msg/Float64.html) | Barebones steering command
/vesc/odom | [nav_msgs/Odometry](http://docs.ros.org/api/nav_msgs/html/msg/Odometry.html) | Odometry from motion model

#### Subscribers
Topic | Type | Description
------|------|------------
/mux/ackermann_cmd_mux/output | [ackermann_msgs/AckermannDriveStamped](http://docs.ros.org/api/ackermann_msgs/html/msg/AckermannDriveStamped.html) | Output from mux to be converted to direct controls
