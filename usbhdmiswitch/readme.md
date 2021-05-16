The udev script reacts on usb being disconnected (device numbers found by lsusb).
Put udev rule in /etc/udev/conf.d/ and reload rules by doing 
sudo sh -c "udevadm control --reload-rules && udevadm trigger"

The udev script calls the laptop/desktop scripts, which are just a single ddccontrol command to switch screen input. Valid inputs are 15 to 18.
