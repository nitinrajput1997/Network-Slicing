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


**Use Cases**

i) Industries
   it has been seen that different industries might require different flies on their own please stop for example if we take railways, it is a nationwide network and rings are mostly connected to let's say 4G network. We need to update them to the 5G network because the railways are safety-critical and have different performance characteristics they might type to a slice of their own instead of connecting to a normal broadband network play store that way it was assured most performance and security of railway network. Similarly, all the autonomous cars are industrial of their own and have their dedicated network slices. 

ii) Services
   we have smartphones which are mobile broadband use cases and then we have a sensor which is a massive machine type communication use case and we have a robot which is usually ultra-reliable and low latency communication because these have different performance characteristics, we can also make sure the slices are divided in such a manner that each of these different kinds of traffic has their slices.

iii) Public Safety
   we can have different network slices have different aspects of a public requirement. For example, fire servicemen could have their own logical network lies and the police force can have their own logical network slice similarly a public civilian can also have their own logical network slices for whatever service they use.

iv) Application
   the fourth possible way of dividing applications, for example, we can have a different network size for AR VR use cases. Alternatively, we can have dedicated networks lies for gaming. Similarly, we can have another network slice for videos, etc. So the application presents another way how we can struct Network slices.


**Implementation**
 
 There are four components 
i) RAN 
    Whenever a PDU session is established from a device. That PDU session will be associated with the slicer identifier. The slice identifier in 5G is called NSSAI (single network slice selection assistance identifier), which is an ID which says that this PDU session corresponds to a massive machine type communication or this particular network slice corresponds to mobile broadband networks. So it is simply a number that indicates which slice that divides wants this produce awesome to belong. Once it is established, every time the device is sending or receiving data. The RAN can look at that particular video and decide that this particular video belongs to this particular network slice. So they will be going to treat it accordingly. Each video is associated with corresponding data radio bearers on RAN. So depending on which radio bearers in the PDU belong.  The packet will be treated differently by the RAN. The scheduler is responsible for creating different network slices differently on the RAN level. 

There are two options for how the RAN can handle this either we have 
a) Hard Partitioning 
	let's say we have 50 megahertz of spectrum and half of it can be dedicated for slice them in half of it can be dedicated to slicing two. Whether they are utilized or not the resources are divided hardly both these slices. 

b) Soft Partition 
	when the resources in the other slides are not used, then the other slides which need those resources can go and use them. For example, assuming that slice 1 and slice 2 both have dedicated resources. And slice 2 might not have much traffic right now due to some reason in such situations slides one can go and make use of those resources to serve its use cases.


ii) Core Network
	In this, the network function is virtualized so it is easy to create four instances of the core network function. We have two options either a given network function handles the different network slices differently or alternatively, we can create new instances of the network function particularly for each slice. There are two parts as control plane network function and the user plane network function
a) User-plane function (UPF)
	often depending on the use cases the UPS has to be different in the different space for example if we have one network dedicated to low latency then the UPS have to be as close to the device as possible on the other hand for mobile broadband the UPS does not have to be very close so for these two network slices it can make sense to have two different instances of UPM that are also in different parts of the 5G network 
b) Control plane network function 
	these are almost always in the central data centre they are usually physically in the same location but each slice can get different logical instances corresponding to each network slice this is how the core network disconnected slices. 

iii) Transport 
	this is the network which connects the RAN to the core network. These are different operations such as 
a) if this layer use IPv6, this has a certain feature called labels which can be used to differentiate different IP packets. For each, network slices can be associated with the different flow levels and then transport networks treat the different packets differently according to the flow labels. 
b) we can have different VPN virtual private networks or VPNs could get put to cater to different use cases and network slices. 

iv) Operation
	"How can the network operator handle different network slices". There are two parts 
a) Automation 
	the 5G network is defined for a high degree of automation so whenever we want to define a new network slice or to change the parameter of given network slices. It does not mean that the 'n' number of engineers had to go and reconfigure thousands of devices across the network to make sure network slicing needs are met. Since 5G network components are designed for a high degree of automation so that when the network slides are defined at the central location to which all the devices can be automatically configured for a specific configuration that is needed for the given network slice description. 

b) Monetization 
	Also, the operation part of a device is designed so that the different network slices can be monetized differently. We should be able to measure how much consumption is happening in each slice. So that we can build them differently and accordingly. The operation is enabled for networks by supporting automation and monetization to facilitate network slicing.
