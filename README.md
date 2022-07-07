# Metro Wrapper in Python

We extracted the Metro implementation from "https://github.com/cnr-isti-vclab/vcglib/tree/main/apps/metro" and created a python wrapper so we can call it from python.

## Installation
Please make sure you have pybind11 installed ("https://pybind11.readthedocs.io/en/stable/installing.html")

mkdir build
cd build
cmake ..
make 
make install

This will create a .so file in lib/ folder. To use it, you need to set the path to this folder and import metro.