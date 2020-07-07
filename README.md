# p3-at-mobile-robot

## Install Ubuntu

Disable login for user
Connect via cable to internet
Install all packages (open-cv, ros...)

## ROS:

Install ros

```bash
cd catkin_ws/src
cp backup/rosaria . 
cp backup/LMS1xx . 
# or alternatively
git clone https://github.com/clearpathrobotics/LMS1xx.git
rosdep install --from-paths src --ignore-src -r -y
# Rosdep also install libaria (from the repo)
```

Alternatively install aria (from backup)

## Hotspot 

Create hotspot using GUI

Edit /etc/NetworkManager/system-connection/Hostspot

```
autoconnect=true
[ipv4]
address1=192.168.1.1/24,192.168.1.1
```

## LMS1xx

Ubuntu Settings -> Network -> enp3s0 -> 
- Enable interface
- Disable IPv6
- IPv4 fixed IP 192.168.0.2 subnet 255.255.255.0

## SSH

Create ssk-keygen

Copy robot public key to laptop
Copy laptop public key to robot

Edit /etc/hosts on robot and laptop to give names to the IP addresses of the robot and the laptop

make sure you can ssh from the laptop to the robot and vice versa without a password

## BASHRC

edit the .bashrc file

```
export ROS_MASTER_URI=http://laptop:113111/
export PATH=$PATH:/home/robot/bin
source /opt/ros/melodic/setup.bash
source /home/robot/catkin_ws/devel/setup.bash
```

