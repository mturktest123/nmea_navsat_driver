nmea_navsat_driver
===============

ROS driver to parse NMEA strings and publish standard ROS NavSat message types. Does not require the GPSD daemon to be running.

API
---

This package has no released Code API.

The ROS API documentation and other information can be found at http://ros.org/wiki/nmea_navsat_driver

Allan's notes:

NMEA (for gps data):
cd rover_ros_ws/src    (aka catkin_ws/src)
git clone https://github.com/ros-agriculture/nmea_navsat_driver.git
cd up to /home/allan/rover_ros_ws (with cd ..)
catkin_make
cd ..
source .bashrc
?? cd rover_ros_ws
?? source /devel/setup.bash
roslaunch nmea_navsat_driver nmea_serial_driver.launch

Reference docs:
which port is my device connecting to?
https://askubuntu.com/questions/398941/find-which-tty-device-connected-over-usb

my device was connecting to ttyACM0 vs ttyUSB0:
https://rfc1149.net/blog/2013/03/05/what-is-the-difference-between-devttyusbx-and-devttyacmx/

fix for port giving an ‘access denied error’:
https://stackoverflow.com/questions/27858041/oserror-errno-13-permission-denied-dev-ttyacm0-using-pyserial-from-pyth
https://www.linuxquestions.org/questions/linux-software-2/usb-issue-device-dev-ttyusb0-access-failed-no-such-file-or-directory-4175428160/
