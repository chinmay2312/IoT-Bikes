# IoT-Bikes

# Inspiration<br>
We realized that riding a bicycle to and fro from within a selected region should not be charged as it does not involve any fuel.
Now, making a bicycle free of cost would compromise the security and that is why we made use of IOT devices Dragonboard and Arduino in order to make the cycle secured.
Apart from that since the bicycle is free of cost people will prefer it over fueled vehicles thus, reducing the emissions and creating a environment friendly smart city.
It can also help people in maintaining a healthy lifestyle by taking up bicycles more often than cars.

# What it does<br>
Dragonboard keeps track of the location of the bicycle.
Arduino looks after it's security and weather data collected from bikes.
Together these two devices help in creating a solution which makes bicycles available to everyone free of charge.
Machine learing analytics of sensors data in GCP
# How we built it<br>
Arduino is interfaced with the sensors to help collect data from the bikes or their docks (or both).This will help detect if someone is throwing bike in water then humidity will increase.If someone tries breaking the bike or takes it to a rugged location then we use vibration sensor.Also placing these devices on the dock can help us determine the weather data of that location then we know that more bikes are needed at the spot based on analytics.
We have used Dragon Board.
The GPS data is transmitted from the dragonboard to Google Cloud Platform(GCP) and stored on Firebase.
A Twilio API sends the SMS if the readings of the sensors goes beyond a threshold.
A Debian OS is mounted on the Dragonboard.
A Node.js application receives the location data from a python API and sends it to Google Cloud Platform.
The sensors on Arduino are present to detect any damages done to the box( mounted on bike and the dragonboard is present inside this box.
![Architecture Diagram](https://github.com/harsh543/IoT-Bikes/blob/master/images/Arch.png "Architecture Diagram")

# Challenges we ran into<br>
The GPS sensor cannot be activated on the dragonboard because specific gps modules cannot be used on Debian version. Samsung gear s3 gps and bluetooth transfer issues.
Configuration and setup issues specifically conflict with the python version on google cloud platform.
Accomplishments that we're proud of
Utilized HERE maps to location dynamically of the bikes in a confined zone.
Setting up Google Cloud Platform and Firebase.

# What we learned<br>
We should be prepared with all sensors that are required for implementing a hardware hack. Else you might run into issues of sensors not being supported for the particular hardware/device that you are working on.
What's next for Shield Bikes
Shield bikes have a tremendous potential to completely change the way bicycle industry operates by making it more accessible to people.

# Built With<br>
node.js
dragonboard-410c
arduino
google-cloud
firebase
express.js
fitbit
twilio
python

# Interfacing instruction with Arduino Uno/101<br/>
Set Baud rate to 9600 <br/>
Connect the A0 with the light sensor <br/>
Interface the A1 with temperature/humidity sensor<br/>
Connect the A2 with buzzer<br/>
connect A3 with temperature sensor(for fire detection)<br/>
Connect the A4 with vibration sensor<br/>
### Please note: Even if you don't connect all these sensors the code will still be downloaded and the available sensors will function as expected.
# Future work
To make these devices run on Battery which lasts for a couple of years atleast.

