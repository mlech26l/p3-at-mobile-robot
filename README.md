# p3-at-mobile-robot

## Install Ubuntu

Disable login for user
Connect via cable to internet
Install all packages (open-cv, ros...)

## Steps:

Install aria
Install ros

clone rosaria to catkin_ws
catkin_make to see if rosaria can be built

Download ros lms1xx package using apt-get

## Hotspot 

Create hotspot using GUI
Edit /etc/NetworkManager/.../

Set IP range and autoconnect=true


## SSH

Create ssk-keygen

Copy robot public key to laptop
Copy laptop public key to robot

Edit /etc/hosts on robot and laptop to give names to the IP addresses of the robot and the laptop

make sure you can ssh from the laptop to the robot and vice versa without a password
