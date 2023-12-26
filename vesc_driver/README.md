# Udev rules setup

Note: The following steps are only required when installing the package from source. When installing a binary debian package the udev rules are set up automatically.

Make sure your catkin workspace has been successfully compiled. To set up the udev rules for the VESC USB devices, run the following commands:

roscd vesc_driver
sudo cp debian/udev /etc/udev/rules.d/99-vesc6.rules
sudo udevadm control --reload-rules

Afterwards, disconnect the USB cable and plug it in again (or run sudo udevadm trigger).
