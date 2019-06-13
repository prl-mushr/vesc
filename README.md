# MuSHR VESC (Derived from MIT VESC)

Contains the code for interfacing with the VESC hardware.

Packages:
  - `vesc`: Metapackage
  - `vesc_ackermann`: Code for converting from Ackermann messages to VESC interpretable messages. Also has code for converting vesc responses to odometry.
  - `vesc_driver`: Code for sending messages to the VESC device file.
  - `vesc_main`: Launch files for the vesc code.
  - `vesc_msgs`: Contains only messages related to the VESC.
