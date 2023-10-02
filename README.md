# raspberrypi_DMX_lights
# Setting up RaspberryPI to control DMX lights using QLC+

The end result of this will enable you to use a RaspberryPI to control you lighting system. This setup uses QLC+, an open source DMX light controller which is great for programming and running light shows.  Then it will use RVNC to remotely control your raspberryPI (and thus your lightshow) from your iphone/ipad/computer.

Setup overview
1) [Install QLC+ on your RapsberryPI.](https://github.com/alan-roth/raspberrypi_DMX_lights/edit/main/README.md#install-instructions)  I had to compile it on the device and then it ran well. 
3) Install and setup RealVNC to remotely control your RaspberryPI from your phone/ipad/computer.
4) Turn on your RapsberryPI
5) Start up QLC+
6) Plug in your USB to DMX cable to the RaspberryPI and your light system.
7) Have fun.

![IMG_3136](https://github.com/alan-roth/raspberrypi_DMX_lights/assets/10735312/7bdc756c-994b-463a-aa91-8cb77a702559)

![IMG_3137](https://github.com/alan-roth/raspberrypi_DMX_lights/assets/10735312/af53079e-6e24-4442-bb7b-b5dd64cd97e8)

# Install Instructions
1) Open a command terminal and enter the following code, which are requied to make it work:
sudo apt-get update
sudo apt-get install g++ make git build-essential qtchooser qt5-qmake qtbase5-dev qtbase5-dev-tools qtscript5-dev qtmultimedia5-dev libqt5multimedia5-plugins qttools5-dev-tools fakeroot debhelper devscripts pkg-config libxml2-utils libglib2.0-dev libpulse-dev
sudo apt-get install libasound2-dev libusb-1.0-0-dev libftdi1-dev libudev-dev libmad0-dev libsndfile1-dev libfftw3-dev

2) Get the QLC code which will create new directory: qlcplus.  Run the following code:

git clone git://github.com/mcallegari/qlcplus.git
cd qlcplus
git pull

3) Compile it. This step will take quite a while. Run the following code to compile - if it gives you errors, its probably missing a depdendency that may need to be installed.
qmake
make

4) Install it by running:
sudo make install
5) then start the program up:
qlcplus

If its not working at this stage, check out this [more indepth guide to building it on linux](https://github.com/mcallegari/qlcplus/wiki/Linux-build-(Qt5--&-qmake))

# How to use QLC+
Here are sevearal tutorials for QLC+  [https://www.qlcplus.org/discover/tutorials](https://www.qlcplus.org/discover/tutorials). Youtube also has some rather helpful tutorials too.

# Where to get a USB to DMX cable?
Amazon has a number of choices of [USB to DMX cables]. (https://www.amazon.com/s?k=usb+to+dmx+cable&crid=37N839E6VSAX5&sprefix=usb+to+dmx+cabl%2Caps%2C256&ref=nb_sb_noss_2)
