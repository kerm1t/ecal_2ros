# ecal_2ros

this node converts eCAL data to ROS.

it can be done
1. live
2. from hdf to .bag

## How to build
```
git clone git@github.com:kerm1t/ecal_2ros.git
mkdir build
cd build
cmake ..
make -B
```

## How to run

- start 2 terminals
- terminal 1
```
roscore // start ros broker
rosparam set use_sim_time false // optional
```
- terminal 2
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
  
