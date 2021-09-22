# Ardupilot Gazebo 7 plugin

## Installation:

On a new terminal:
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

````
gazebo --verbose ardupilot_gazebo7/worlds/my_drone_arducopter_runway.world
````