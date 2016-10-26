### Video Streaming On YouTube
From: Zhihao Xue

To: Dr. Jianjian Song

#### Introduction 
In this project, a main propose is to stream video via a web camera to the Internet. At the first, I tried to use OpenCV and Intel Edison Dev Board to achieve this goal. However, Edison does support video steaming on local host, it became difficult when you try to push your streaming out to the Internet. Luckily, Raspberry Pi solved this problem.

#### Intel Edison
In the beginning, I used Edison as my dev board, because this board support multiple programming languages and has built-in wireless connections such as Wi-Fi and Bluetooth, which are very important for Internet of Things. During the week 2 and week 3, I successfully ran a video streaming demo with OpenCV and flask. This demo set up Edison itself as a servo and host the video service. In this demo, OopenCv capture raw image from the web cam and sent these buffer images continuously to the server to mimic the video streaming. In this way, you can see the streaming on local host frame by frame. The resolution is about 640 by 480. And frame rate is round 10 fps. So, in this demo, you can see obvious latency and remnant trace. 


#### YouTube Live
Recently, YouTube support live streaming. Each person can set up their own live channel to streaming their lives or various events, such as making up, or playing games. The set up is really easy, you just need a encoding software (I use ffmpeg here) and some streaming info, then you can broadcast in the front of the world. 

#### Streaming
In previous part, I mentioned I can use ffmpeg to stream my web cam video to YouTube. When I first try this on Edison, it gives me some domain name error. I found someone had similar issue on Intel forum, when I follow his solution to change domain name, it still cannot solve the problem. Even I change the IP address to 0.0.0.0 and 127.0.0.1, which can represent all local IP addresses. (I forgot to capture screen shot at this time, will attach them in the final report)

#### Pi
After trails and errors, I still cannot get video done and broadcast to YouTube. And I found some threads talking about Raspberry Pi may do a nice work instead Edison, when I try to figure out how to stream on Edison. So I made a decision to switch the project from Edison to Pi. One reason I guess is that Edison is still a very new Dev board. It is only about two years from it release, the support libraries may not sufficient. With Pi, you can access abundant libraries to help you achieve your goal. And the problems you occurred, someone else might already solved. 

#### USB Cam VS Pi Cam Module
For Pi streaming, I can simply use ffmpeg library to broadcast to YouTube. But this seems not support USB cam very well. When I tried to use USB cam to stream, ffmpeg does find the device, but will return some errors. After I switch to official Pi Cam Module, problem solved. 

#### Quality of the Streaming
YouTube supports up to 1080p resolution, and I strict it to 720p to save bandwidth and enhance transmit speed. After test, I can get very high quality video streaming on YouTube with 30M bandwidth Internet connection at home. There is one issue I still try to find answer. There is about 16s late between local side and YouTube side. I was thought this is about initialization and Internet censorship. 

