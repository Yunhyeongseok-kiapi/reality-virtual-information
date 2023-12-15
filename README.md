# KIAPI
## Korea Intelligent Automotive Parts Promotion Institute(KIAPI) 
## <img src="https://github.com/Yunhyeongseok-kiapi/KIAPI_dataset/assets/85465084/9304bae8-7878-4b71-853f-08cff6392d4e" width="300" height ="100">

### (KIAPI)Development of reality-virtual information convergence and edge-based autonomous driving simulation SW technology
Precision simulation SW and system linkage framework for co-simulation in conjunction with real (vehicle, PG environment, etc.) based on precise virtual environment-based sensing/cognitive/judgment or control information in line with the due diligence environment (vehicle, PG environment, etc.)

#### GOALS
- LoD4 -level autonomous driving mock test that supports precision textures static/dynamic asset content
- Virtual-Development of autonomous driving simulators and interfaces for edges for real information convergence verification
- Signal distortion, precision heterogeneous sensor modeling reflecting the attenuation
- Co-simulation framework linked car, artificial intelligence solution, edge server
- Test case for autonomous driving verification, scenario creation and verification
- Synthetic datuments for artificial intelligence and benchmark sites for performance verification

  #### KIAPI : Simulation-between autonomous vehicles Data exchange system

  ##### Introduction
   - Name : Simulation-between autonomous vehicles Data exchange system
   - Company : KIAPI
   - Function
     
     ● Data exchange system between the simulator and autonomous driving system  
     ● Data transmission and reception using TCP communication based on Ethernet connection between system hardware  
     ● In the simulator, the object data generated from the virtual environment -based simulation  
     ● In autonomous driving system, virtual object data can be used by analyzing the received data  
     ● The autonomous driving system can evaluate autonomous driving functions on various scenarios using virtual object data other than the existing autonomous driving system

   - Specifications and configuration
 
     ● configuration

    1) Interface configuration      
       : The simulation system is interface with an autonomous driving system and a TCP, and the simulation system is transmitted and receiving and receiving and receiving data to the server and autonomous driving system to TCP Client       
 

       | Server (Simulation system) | Client | (Autonomous system) |    비고  |
       |:--------------------------:|:------:|:-------------------:|:--------:|
       |           IP               |  Port  |                     |          |
       |       192.165.10.10        | 15128  |   192.168.10.20     | Ethernet |     


    2) TCP default message definition       
       : Self-defined packet proceeds based on non-engine              
       : Byte order: Little-endian
       |          |                     Header                                | Data |
       |   Type   | Packet Type | Current Sequence |   Time Stamp | Data Size |   -  |    
    4) Object data message definition      

