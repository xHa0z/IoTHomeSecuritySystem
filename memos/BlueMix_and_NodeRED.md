## BlueMix and Node-RED
From: Zhihao Xue

To: Dr. Jianjian Song

### Node-RED
Node-RED is a tool for wiring together hardware devices, APIs and online services in new and interesting ways. Current, it can run on Raspberry Pi and BeagleBone Black these two hardware platforms. And three cloud platforms, IBM Bluemix, AWS and Microsoft Azure, as well. 

In my project, I use Node-RED on my Raspberry Pi to read sensor data from SensorHat, a add-on board for Pi bristling with multiple sensors, including gyro, accelerate meter, temperature, humidity, pressure and so on. I used temperature, pressure and humidity and use Node-RED to capture their value, then, split them into 3 individual output to display into console and upload to IBM Bluemix as well.

### Bluemix
Bluemix is developed by IBM. This is a cloud platform for Internet of Things. It does support lots of useful functions, but I just used its IoT service. 
To combine Bluemix with Raspberry Pi, you have to register your device to Bluemix first. Then, in Node-RED, with select 'registered device' option, you can establish a connection between you local device and Bluemix on cloud. 

### What is the procedure
When the Pi and Bluemix is deployed, the Pi will extract sensor data from SensorHat. Then, in local Node-RED pipeline, the sensor metadata is split into three individual data for temperature, humidity and pressure. Then these information will be displayed in Pi's local console, while the Node-RED pipeline will send these data to the Bluemix as well. 
Then in the Bluemix side, you also need a Node-RED pipeline to extract data send from Pi. These data is send encoded with a particular format, while in Bluemix side, it will help you decode these information and display what you have in the console

### What is the next
Since I have the data both on local and the cloud successfully, the next step is figure out how to display these data. The freeboard.io provides a good platform and I will start from there. 