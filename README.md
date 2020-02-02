# slippirecorder
slp -> mp4 -> youtube

Steps taken:
* Spin up DigitalOcean ($10/mo)
* Set up https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-vnc-on-ubuntu-16-04, involves installing Putty/VNC Server locally
  * Steps for VNC Server to connect to Putty (https://medium.com/@madhav2code/vnc-over-ssh-using-putty-in-windows-d82ac35dc25e)
* Install CMake (dependency for Slippi: `sudo apt-get -y install cmake`), then restart console to refresh path (otherwise can't find CXX_COMPILER or something)
* Install `sudo apt-get install build-essential` to get CMake to work for below
* Install `sudo apt install cmake pkg-config git libao-dev libasound2-dev libavcodec-dev libavformat-dev libbluetooth-dev libenet-dev libgtk2.0-dev liblzo2-dev libminiupnpc-dev libopenal-dev libpulse-dev libreadline-dev libsfml-dev libsoil-dev libsoundtouch-dev libswscale-dev libusb-1.0-0-dev libwxbase3.0-dev libwxgtk3.0-dev libxext-dev libxrandr-dev portaudio19-dev zlib1g-dev libudev-dev libevdev-dev "libpolarssl-dev|libmbedtls-dev" libcurl4-openssl-dev libegl1-mesa-dev libpng-dev qtbase5-private-dev` as x11 dependency for Dolphin (taken from here: https://wiki.dolphin-emu.org/index.php?title=Building_Dolphin_on_Linux#16.04_LTS)
* `sh -c "$(curl -Ls https://github.com/project-slippi/Slippi-FM-installer/raw/master/setup)"` 
  * `y` yes overwrite installations
  * `y` yes i'm sure
  * `n` no WiiU adapter
  * `Y` desktop shortcut
  * `*` slippi r18
  * `1` 1 CPU thread
