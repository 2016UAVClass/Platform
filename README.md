# Platform
Navigation, Flight, and Ground Control


Communicating with Mavros
  source /opt/ros/indigo/setup.bash
  roslaunch mavros px4.launch // if using usb
  roslaunch mavros px4.launch  fcu_url:="/dev/ttyUSB0:921600" //replace ttyUSB0 and 921600 with required baudrate
  
Once launched and connected
  rosrun <cmd> <parameters>

Commands
  Mavcmd: sends command to vehicle i.e. mavcmd 1 168 1 1000 0 0 0 0 0 0 will activate the actuator
    error: Unexpected command for any command sent in this method
    list of commands can be found here: https://pixhawk.ethz.ch/mavlink/
    
  mavsafety: can be used to arm/disarm and set up geo-fences
  
  mavwp: can be used to send wp or a wp file to the pixhawk
  
  other commands: http://wiki.ros.org/mavros
  
Parameters
  https://pixhawk.org/firmware/parameters
  need to tune PID parameters when extra weight is added
  
