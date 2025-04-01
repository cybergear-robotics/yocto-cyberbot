# Yocto for CyberBot with Raspberry PI

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/cybergear-robotics/ros2-cyberbot/activity)
[![ROS_2](https://img.shields.io/badge/ROS_2-Jazzy-orange.svg)](https://docs.ros.org/en/jazzy/index.html)
[![Yocto](https://img.shields.io/badge/Yocto-Scarthgap-purple.svg)](https://docs.yoctoproject.org/5.0.8/)

This yocto builds an Raspberry PI SD-card image which boots ROS2 and brings up the cyberbot service.


# Setup

1. Install development environment for Yocto Scarthgap: [Preparing the build host](https://docs.yoctoproject.org/next/dev-manual/start.html#preparing-the-build-host).

2. Setup build directory
   ```bash
   TEMPLATECONF=sources/meta-cyberbot/conf/templates/default . sources/poky/oe-init-build-env
   ```

3. Optionally provide SSID and password for an access point. This will allow the Raspberry PI to connect to the Wifi.
   Update following variables in `build/conf/local.conf`:
   ```
   WPA_SSID = "MeinWLAN"
   WPA_PSK = "MeinPasswort"
   ```

4. Build image
   ```bash
   bitbake ros-image-cybebrot
   ```
