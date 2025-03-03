# ecal_2ros

Node to convert eCAL data to ROS.

To be used
1. live
2. convert .hdf5 to .bag

## How to build
```
git clone git@github.com:kerm1t/ecal_2ros.git
mkdir build
cd build
cmake ..
make -B
```

## How to run

- start ROS1
```
roscore // start ros broker
rosparam set use_sim_time false // optional
```
- start ecal2ros node
```
cd build
./devel/lib/testnode/testnode
```
- start eCal player
![Screenshot from 2025-03-03 06-49-43](https://github.com/user-attachments/assets/33b0246c-a197-4c81-8b61-14bbc6334e9c)

- start RViz to verify pointcloud
![Screenshot from 2025-03-03 06-53-07](https://github.com/user-attachments/assets/efedba8f-b50f-489a-915e-6f9a32af999f)

- record .bag file with
```
rosbag record -O mid360.bag -a
```
  
