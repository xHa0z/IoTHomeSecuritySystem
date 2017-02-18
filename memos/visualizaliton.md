## Visualize Data
From: Zhihao Xue

To: Dr. Song

------
In this week, the main work is to visualize data on the Internet. So user can access the data and monitor remotely. 

To achieve this goal, I choose freeboard.io as my platfrom. 

Freeboard.io is a simple dashboard for Internet of Things devices. You don't need to know how to write a web page and you still can build a dashboard and display your devices data. 

The most necessary information is the data source, this is where your data comes from. In this project, the data comes from Bluemix of course. In order to send data out of the Bluemix, a http request should be established and the content of event message should be accessible. 

To solve this problem, in Bluemix, I create a global variable to store the message payload from the device. Then send out this variable via that http request in JSON format to freeboard.io. 

Back to freeboard.io, in the console, I can add a new data source, which is the http request I created in the Bluemix. With this URL, freeboard.io is able to continuously receive data sending from Bluemix and use different widgets to extract different data from this entire event message. 

As all sensors data could be displayed on dashboard correctly, all majors goals for this project have been achieved. Next step is to finish up the final report.