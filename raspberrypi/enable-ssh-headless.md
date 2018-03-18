# Enable SSH headless

Raspbian disables SSH by default. To enable it without having to attach a monitor and keyboard you can put an empty file called `ssh` in the root directory of the SD card and it will enable SSH on the first boot. The file gets deleted afterwards automatically.