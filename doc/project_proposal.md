## Project Proposal: IoT Home Security System
From: Zhihao Xue

To: Dr. Jianjian Song

#### Introduction
The Internet of things (IoT) refers the devices embedded with various senors and connect to the Internet. These devices capture abundant data and information everyday. In our daily life, these devices include mobile devices, such as smart phones, smart watches and tablets, home air conditioning systems, and even the cars. 

A IoT home security system usually consists of one or more surveillance cameras to record image and video, a microphone to capture ambient sound, a speaker to play loud siren and some others sensors to monitor the home. And these different devices connect to a hub or a wireless module, so they can communicate with the Internet. 

When the motion sensors detect any movements, it will trigger the cameras to record images and send notification to the householder. Then the householder can choose to dismiss this warning if this is caused by their pets, or alarm the siren and call the emergency if there is a burglar. 

The preliminary goal of this project is to build a in-door monitoring system that has ability to detection motion, capture image, send notification to householder and householder can remotely live view the camera screen. Then, I can stretch from this and add some new features. These new features may include fingerprint door lock and face recognition camera. Furthermore, it could be a good try to integrate this project with Apple HomeKit®.

#### Description
This home security system will be a self-designed system. I will design and build this system with products already on the market. All sensors and Internet cameras will be connected via wire for now and could be switched to wireless in the future. And to achieve the preliminary goal, I will build a model first to test the system,then apply this system to my current apartment. 

The system will use a Intel® Edison Kit for Arduino as the central hub. All peripheral devices such as cameras and sensors will connect to this hub. The Edison is made by Intel, an IoT pioneer. The Intel® Atom processor provides powerful computing capability. Since it support Arduino platform, it means there are plentiful libraries and modules available online. This can help me save lots of time to develop the drivers. In addition, Edison supports Bluetooth and Wi-Fi connection. All sensors data will collected by Edison, then the hub will process these data and send them to the cloud. 

There are two major parts in software control. The first part is based on the Edison. This part runs locally on the system. It will interact will all sensors, cameras and speakers, collect and record their data, monitor any abnormal status. It will log these information into a database for householder reviewing and analyzing. The second part relies on IBM Bluemix®, a cloud-base platform. With Bluemix, I can bring this security system online. I can remotely monitoring these cameras and sensors and save data into cloud storage. 

The primary challenge of this project is to coordinate different sources of data. Since I will use existing sensors instead of creating by myself, I need to find a way to convert their raw data into a standard format in order to communicate with each other and log into database. And so far I am still looking for a method to solve this. 

#### Objectives and Specifications
* Design and build a in-door security system
* Implement software control program to collect and process sensors data
* Implement cloud-base control program capable of viewing system status remotely

#### Tasks 
* Initialize Edison and Bluemix
* Build a test system that consist of some simple sensors
* Test the system locally
* Program system to make it online
* Apply test system into a real life apartment
* Try stretch goals


#### Budget
This project is self-found, so this budget is only a roughly estimation. The real expanse will be recorded during the project.

##### Equipment:
* Intel Edison Kit for Arduino	&nbsp; &nbsp;&nbsp;	$100
* Internet camera 	 &nbsp; &nbsp;&nbsp;    $50 each
* Breadboard	 &nbsp; &nbsp;&nbsp;   $20
* Power supply  &nbsp; &nbsp;&nbsp;   $20
* Miscellaneous sensors &nbsp; &nbsp;&nbsp;	$100
* Electronics 	&nbsp; &nbsp;&nbsp; $20
* Shipping 	&nbsp; &nbsp;&nbsp; $20


#### Timetable
|             Task             | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|:----------------------------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|
|      Initialize Project      | x |   |   |   |   |   |   |   |   |    |
| Purchase necessary equipment | x | x | x |   |   |   |   |   |   |    |
|       Build test system      |   | x | x |   |   |   |   |   |   |    |
|      Bring system online     |   |   | x | x | x | x |   |   |   |    |
|      Apply to real life      |   |   |   |   | x | x | x | x | x |  x |
|       Test and Stretch       |   |   |   |   |   |   | x | x | x |  x |