# IOT-Smart-Highways-Using-Intel-Gallileo

Road traffic accidents remain a real scourge. Despite improved road safety, particularly in developed countries,every year, road accidents claim the lives of 1.3 million people worldwide.Low-income and middle-income countriesaccount for 93% of the no of deaths, while the same countries account for only 54% of global feet and economiccost of these accidents exceeds$500 billion.Though it is claimed that self-driving cars could eventually improvesafety, their feasibility is yet to beestablished and they come at prohibitive costs. Also, vehicle-to-vehicle (V2V)communication requires the installation of signal receivers built along roadsides, known as roadside units (RSU), which, of course, wouldrequire a massive infrastructure investment. Moreover, it may not be viable to provide such infrastructure in ruraland less developed areas where collision warning systems are most needed. Hence to tackle the global crisis ofroad safety, we have developed a low-cost, easily implementable and disruptive GNSS-based collision warning system innovation We imagine the cars of tomorrow to work as a cooperative, organized and harmonious organismrather thanindividual and independent vehicles.Our solution requires better satellite navigation infrastructure and faster mobile Internet speeds, both of which areon the verge of becoming a reality.Since the past three years, the world of satellite navigation is undergoing dramatic changes with the rapiddevelopment of multi-constellation Global Navigation Satellite Systems (GNSS). By early 2020, all the five major GNSS constellations, including GALILEO, GLONASS and BeiDou, will be operational and will cover most parts ofthe world. As a result, about 120 satellites will be available for precise positioning and about 30 satellites will be  inview from any given location, enhancing accuracy, speed and integrity of location data.Technologies such as 5G and LTE could drop network latency by almost 10 times compared to latency by almost 10 times compared to the urrent speeds,and thus make mobile Internet the ideal medium of communicating location data among vehicles.Further, with the development of stream processing, Fast Data and Big Data platforms, applications that require
real-time dataprocessing, such as collision avoidance, can become a reality. 


Project objective is to save the lives of people  with  the implementation of a robust system for real time monitoring of highways. Various sensors have been deployed on highway which report the status of the same to a central control station.Project were integrated using Intel Galileo Gen 2 IoT kit. Arduino IDE was used to write sequential codes for the modules.All the sensors used ZigBee protocol for wireless serial communication.MATLAB was used to detect accident sounds from the speech signals obtained.Each module is described below: Sound Signal Based Accident Detection BySpeech signal processing
The input to the system is a 3-s segment of audio signal. The system can be operated in two modes: the two-class and multiclass modes. The output of the two-class mode is a label of "crash" or "noncrash." In the multiclass mode of operation, the system identifies crashes as well as several types of noncrash incidents, including normal traffic and construction sounds. The system is composed of three main signal processing stages: feature extraction,
feature reduction, and classification.Network of audio sensors installed on the highway collect the data which is first preprocessed and their intensity is calculated by local(nearer to sensor) Intel Galileo Gen-2.If the intensity of captured data is higher than threshold then Intel Galileo sends this entire data frame to command center usingwireless communication (Xbee).At command center, from given data audio signal is reconstructed. After reconstruction of the signal one can can do the re sampling on desired rate (in this case it is 16 kHz).After Preprocessing and resampling of the data, Spectrogramic analysis is done for accident and non-accident audio signals.Then MFCC of the data frame is calculated and KNN classifier is used for classification. Training has been done with numerous accident and non accident sound samples.Classifier is providing very high efficiency classification.Figures below show spectrograms of accident and non-accident sound signals.
*Collision Avoidance System using IR sensors
*Collision avoidance sensors provide analog proximity measurements for various collision occurring hazards.
*Collision avoidance sensors are used to prevent collision of automatic guided vehicles with either to some other
vehicle or person moving on the road. In addition, collision avoidance sensors are also used as a protective system
in robot arms and docking bays, and as a safety system in automatic shelving.
The system comprises of 3 components • IR transmitters on the fence • IR sensors mounted on the vehicle • Intel
galileo gen 2 mounted on vehicle .The IR transmitters on the fence create a region of IR rays around the
fence.When the vehicle is in close proximity of the fence, the IR sensors sense the rays and send the signal to the



<p align="Left">
<img src="images/Logo.jpg" width="800"/>
</p>

## Hardware

The aforementioned modules were integrated using [Intel Galileo Gen 2](https://software.intel.com/en-us/iot/hardware/galileo) IoT kit. Arduino IDE was used to write sequential codes for the modules. 


The highway monitoring system is divided into different modules:
* **Smart fencing**
* **Sound signal based accident detection**
* **Weather detection**
* **RFID toll tax collection**
* **Activity based road light**
* **Collision avoidance system**


<p align="center">
<img src="images/16106796_10209857079115973_925678796_o.png" width="500"/>
</p>

All the sensors used [ZigBee](https://www.digi.com/lp/xbee) protocol for wireless serial communication. MATLAB was used to detect accident sounds from the speech signals obtained.

Each module is described below:

### Audio Signal Based Accident Detection(Speech signal processing)

The input to the system is a 3-s segment of audio signal. The system can be operated in two modes: the
two-class and multiclass modes. The output of the two-class mode is a label of "crash" or "noncrash." In the multiclass
mode of operation, the system identifies crashes as well as several types of noncrash incidents, including normal traffic and construction sounds. The system is composed of three main signal processing stages: feature extraction, feature reduction, and classification.

* Network of audio sensors installed on the highway collect the data which is first preprocessed and their intensity is calculated by local(nearer to sensor) Intel Galileo Gen-2. 
* If the intensity of captured data is higher than threshold then Intel Galileo sends this entire data frame to command center using wireless communication (Xbee). 
* At command center, from given data audio signal is reconstructed. After reconstruction of the signal one can can do the re sampling on desired rate (in this case it is 16 kHz). 
* After Preprocessing and resampling of the data, Spectrogramic analysis is done for accident and non-accident audio signals.
* Then MFCC of the data frame is calculated and KNN classifier is used for classification. Training has been done with numerous accident and non accident sound samples. 
* Classifier is providing very high efficiency classification.


Figures below show spectrograms of accident and non-accident sound signals.

<img src="images/crash.png" width="350"/>              <img src="images/non-crash.png" width="350"/>

### [RFID based Toll-Tax Collection](RFID-toll-collector)

Toll collection booths often become bottlenecks of the highway which leads to stagnant traffic. We have tried to automate this process by proposing a RFID based solution for automatic toll collection.

* A RFID transmitter is assumed to be in the number plate of the car. This gives every car a unique identification number. There is a RFID reader installed on the road a sufficient distance before from the gate. 
* When a car approaches the toll booth the RFID reader reads the tag installed on the car. The identification number is linked to the account of the customer. 
* If the toll is successfully collected the gate is opened for the approaching vehicle. In case the car is stolen and a complaint has been registered the toll booth is notified and the gate remains closed.

<p align="center">
<img src="images/rfid.png" width="400"/>
</p>  

### Collision Avoidance System using IR sensors

Collision avoidance sensors provide analog proximity measurements for various collision occurring hazards. Collision
avoidance sensors are used to prevent collision of automatic guided vehicles with either to some other vehicle or person moving on the road. In addition, collision avoidance sensors are also used as a protective system in robot arms and docking bays, and as a safety system in automatic shelving.

The system comprises of 3 components
• IR transmitters on the fence
• IR sensors mounted on the vehicle
• Intel galileo gen 2 mounted on vehicle

* The IR transmitters on the fence create a region of IR rays around the fence.
* When the vehicle is in close proximity of the fence, the IR sensors sense the rays and send the signal to the Intel Galileo gen 2 on the vehicle.
* Depending on which sensor sensed the IR rays, the board then issues a warning to the driver indicating the direction in which, the driver is close to the fence.

<p align="center">
<img src="images/circuit.png" width="400"/>
</p>

### [Smart Street Light](Smart-Street-Light)

Street Lights in areas with sparse activity are source of major power drainage. Here is proposed an activity based rood light. This includes controlling the circuit of Road lights with self-designed sensors using basic
components like IR Sensor, LDR, Transistors, resistors and capacitors.

* The module consists of an IR transmitter mounted on the base of the street light, an IR sensor on the opposite side of the road which is connected to an intermediate comparator circuit which is then further connected to intel galileo gen 2.
* During night, when there is no activity, the sensor receives the IR signal continuously and hence, the comparator sends no signal to the galielio board. In this case, only 1 out of every 10 street lights are switched on.
* Whenever there is an activity on the street, there is discontinuity in the received IR signal and a signal is sent the galilieo board. In this case, 5 street lights on either side of the sensor are switched on by the galileo board, and remain so for a fixed delay as to provide smooth transition for a moving vehicle.

### [Smart Fencing for Landslide and Accident Detection](smart-fence)

Highways built on hilly terrains have very frequent sharp turns which might become hazardous for vehicles. Now and
then we hear incidents of vehicles falling off the cliff resulting in casualties as help could not be offered on time. The probability of detecting such a mishap and sending help on time is very less as there is no preventive system for that.

* The idea proposed is that accelerometers will be mounted on the fence at particular intervals on the fence running throughout the highway.
* The intel galileo on the sensor side will receive the acceleration of the fence in X, Y and Z direction at a particular sampling rate.
* This vector will be sent to control centre using wireless communication. At the control centre magnitude of the acceleration is calculated.
* If there is an impact on the fence, there will be a sudden rise in the magnitude of the acceleration. If the rise is greater than the preset threshold, the impact will be reported and will initiate the process to send help at the location.

Another aim of this module is to detect landslides which are too very common in hilly terrains. The same method will
be used to detect the impact of debris on the fence so that the alert can be broadcasted.

