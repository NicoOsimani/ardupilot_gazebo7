# ArduPilot & Gazebo 7 plugin

Ardupilot & Gazebo 7 plugin based on the https://github.com/khancyr/ardupilot_gazebo plugin. This assumes that your are using Ubuntu 16.04

## Installation:

On a terminal:
````
git clone https://github.com/NicoOsimani/ardupilot_gazebo7.git
cd ardupilot_gazebo7
mkdir build
cd build
cmake ..
make -j4
sudo make install
echo 'source /usr/share/gazebo/setup.sh' >> ~/.bashrc
echo 'export GAZEBO_MODEL_PATH=~/ardupilot_gazebo7/models:${GAZEBO_MODEL_PATH}' >> ~/.bashrc
echo 'export GAZEBO_RESOURCE_PATH=~/ardupilot_gazebo7/worlds:${GAZEBO_RESOURCE_PATH}' >> ~/.bashrc
echo 'export GAZEBO_PLUGIN_PATH=~/ardupilot_gazebo7/build:${GAZEBO_PLUGIN_PATH}' >> ~/.bashrc
source ~/.bashrc
````

## Usage:

On a terminal, start Gazebo:
````
gazebo --verbose ardupilot_gazebo7/worlds/my_drone_arducopter_runway.world
````

On a new terminal, start ArduPilot SITL:
````
./ardupilot/Tools/autotest/sim_vehicle.py -v ArduCopter -f gazebo-iris --console --map
````
