 # KIAPI(reality-virtual-information)   
## Korea Intelligent Automotive Parts Promotion Institute(KIAPI) 
## <img src="https://github.com/Yunhyeongseok-kiapi/KIAPI_dataset/assets/85465084/9304bae8-7878-4b71-853f-08cff6392d4e" width="300" height ="100">

### (KIAPI)Development of reality-virtual information convergence and edge-based autonomous driving simulation SW technology
Precision simulation SW and system linkage framework for co-simulation in conjunction with real (vehicle, PG environment, etc.) based on precise virtual environment-based sensing/cognitive/judgment or control information in line with the due diligence environment (vehicle, PG environment, etc.)

<img src="https://github.com/Yunhyeongseok-kiapi/reality-virtual-information/assets/85465084/7cd81715-3128-471c-a1f5-96908db05a16" width="1583" height ="413">

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
 

       <img src="https://github.com/Yunhyeongseok-kiapi/reality-virtual-information/assets/85465084/ee3ae54a-74b7-4864-95d5-dd50cafcf3e5" width="455" height ="88">     


    2) TCP default message definition       
       : Self-defined packet proceeds based on non-engine              
       : Byte order: Little-endian

       <img src="https://github.com/Yunhyeongseok-kiapi/reality-virtual-information/assets/85465084/8bffd788-5062-4838-8de3-811238664772" width="455" height ="88">            

       : (Packet Type)Set to distinguish the service by TCP packet type      
       : (Current sequence) Packet number and packet separators, which are used to distinguish between the packets received and the current packet currently received       
       : (Timestamp) Use to check the message transmission time       
       : (Data Size) Except for 9 bytes of header, the unit is the unit      

    3) Object data message definition        
       : Defines object data elements for transmitting to autonomous driving systems in data generated in the simulation system
       
       <img src="https://github.com/Yunhyeongseok-kiapi/reality-virtual-information/assets/85465084/7a19615b-707f-4bc1-acde-d10da8e97444" width="456" height ="588">            
       
       : Object data has a difference in functions for each simulation, so all the elements available in the autonomous driving system have been defined, and data that cannot be provided in the simulation is used by entering zero value           
       : Details are “KIAPI-Technical Documents -2. Refer to the CO-SIMULATION framework “Develop a vehicle connection system”

    4) Data exchange system               
       : The server and the client system uses TCP/IP SOCKET communications using data transmission and reception       
       : The data transmitting system of the server transmits the data by extracting the data of the simulation when the simulation is in operation       
       : The client works only when the server is in operation, and receives data after linking with the server 
       <img src="https://github.com/user-attachments/assets/0143a42c-8ad3-43e0-b0ed-822e0b59f0e0" width="600" height ="320">

  ##### Result
  <img src="https://github.com/user-attachments/assets/e0a29529-dce8-4873-9a6f-dd05b31281a1" width="600" height ="320">



 
