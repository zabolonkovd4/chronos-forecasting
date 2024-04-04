# This instruction is tested on Ubuntu 22.04 (*6.5.0-26-generic*)

# Cloning chronos repo
git clone https://github.com/amazon-science/chronos-forecasting.git ${HOME}

# Create directory for demo
mkdir -p ${HOME}/chronos-demo

# Copy chronos src to demo directory
cp -r ${HOME}/chronos-forecasting/chronos ${HOME}/chronos-demo/

# install qt packages
sudo apt install qtbase5-dev qt5-qmake

# install nvidia driver
sudo apt install nvidia-driver:525

# venv usage
sudo apt install python3.10-venv
python3 -m venv ./ 
source ./bin/activate
pip3 install pandas matplotlib torch transformers accelerate PyQt5

# run your demo
python3 chronos-demo.py

