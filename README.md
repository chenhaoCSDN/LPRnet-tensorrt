# 

The Pytorch implementation is [xuexingyu24/License_Plate_Detection_Pytorch](https://github.com/xuexingyu24/License_Plate_Detection_Pytorch).

## How to Run

```
1. generate LPRnet.wts from pytorch

git clone https://github.com/chenhaoCSDN/LPRnet-tensorrt.git
git clone https://github.com/xuexingyu24/License_Plate_Detection_Pytorch.git

genwts.py into License_Plate_Detection_Pytorch/
// go to License_Plate_Detection_Pytorch/
python genwts.py
// a file 'LPRnet.wts' will be generated.

2. build LPRnet and run

// put LPRnet.wts into LPRnet
// go to LPRnet
mkdir build
cd build
cmake ..
make
sudo ./LPRnet -s  // serialize model to plan file i.e. 'LPRnet.engine'

sudo ./LPRnet -d  // deserialize plan file and run inference
