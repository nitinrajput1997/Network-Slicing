# Network-Slicing

Network slicing overlays multiple virtual networks on top of a shared network. There are some limits imposed by the physical networks. The idea of living is to use an underlying physical network and takes its capabilities and divide it into the logical section where each section can have different performance characteristics. Now for different performance characteristics, we also need corresponding security. 

The security rule is also specific to a specific slice. In the 5G network, the slice that corresponds to let's say a self-driving car will have a different security perimeter compared to a slice that carries let's say sensor information and to be able to achieve these security rules and performance characteristics. We will have a different logical topology that makes the particular network. 
So each slice caters to that specific performance characteristic that is expected from that particular slice. 

This is the illustration of the 5G network. There are different network functions different routers and also have RAN. On top of the 5G network, we can have different use cases running. We can have a smart meter to get electricity reading online and also we can have a robot connected to a 5G network and also a car connected to the same 5G network. In this case, they all are sharing one physical network which is also one logical network. 

Now, if we introduce network slicing in the same 5G network we will have a different logical network. We can have a certain logical network particularly tailored for utilities and we have we can also have a 5G network logically designed for automotive use cases and also we can have a 5G network logically designed for manufacturing. Within the capabilities of the 5G network, we can assign different topologies so that each use case is a network that is tailored and made for that particular requirement. 

**Working**

Let us take a 5G network that has three slices. We have one slice for all the smartphones, one slice for autonomous cars and one slice says or massive IoT devices. There is a scenario where there was a self-driving car which would like to connect to a 5G network. Now the car itself has NetFlix installed because it is a self-driving car and the user can user of the car can watch Netflix. So it wants to connect to a smartphone slide because it is going to use mobile broadband. 
In addition, if it was a self-driving car it also wants to connect to a slice 2 which is particularly designed for autonomous driving. So, in this case, this car will have two PDU sessions and each connected to a different network slice and depending on what is the use case that sends the traffic, the particular slice resolves the demand of the device. In this way, all the traffic is handled differently to achieve the required performance and security characteristics. 


**Characteristic** 

When we get a network slicing, some important characteristics make up the network slicing such as 

i) Customization
 We have different network slices and each goes from end to end, from device to RAN, to core network and both on the user plane and control plane. So we should have a customized performance. If we want a slice to optimize battery life, it should be done on end to end level. If we want to optimize it for latency, we should be able to optimize this also on and when devil. So each network slide should be customizable for desert performance. 

ii) Isolation
 The network slice should be isolated depending on the independence of what happens on one slice. The other slides should have smooth performance. It should make sure that one slice should never interfere with the performance or security of another slice.

iii) Quality Assurance
 Since each slice will have a different desired performance it should be optimized in such a way that it should be able to guarantee the desired quality levels for example the network size that is optimized for low latency it should make sure to ensure the latency performance deck particular slice. If you optimize for data rates like mobile broadband slice, then it should be able to assure the quality in terms of broadband speed is quite guarantee for that particular set slice.

iv) Unified Platform
 Slices operate on one big physical resource pool but there is only one physical 5G network or any operator in the slices is operating on this particular unified platform.
