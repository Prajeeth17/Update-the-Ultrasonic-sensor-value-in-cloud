# Ultrasonic sensor program using Arduino Controller

# AIM:
To use ultrasonic sensor and display the distance using Arduino controller.

# Apparatus required:
Arduino Controller  </br>
HC-SR04 Ultrasonic sensor module </br>
Power supply </br>
Connecting wires </br>

# THEORY:

### What is IoT?

Internet of Things (IoT) describes an emerging trend where a large number of embedded devices (things) are connected to the Internet. These connected devices communicate with people and other things and often provide sensor data to cloud storage and cloud computing resources where the data is processed and analyzed to gain important insights. Cheap cloud computing power and increased device connectivity is enabling this trend.IoT solutions are built for many vertical applications such as environmental monitoring and control, health monitoring, vehicle fleet monitoring, industrial monitoring and control, and home automation

![image](https://user-images.githubusercontent.com/71547910/235334044-c01d4261-d46f-4f62-b07f-72a7b6fce5d5.png)


### Arduino Microcontroller

The Arduino microcontroller is a versatile, open-source platform widely used in electronics projects. Featuring a simple programming interface and a variety of compatible sensors and modules, it's favored by hobbyists, educators, and professionals alike. With its vast community and extensive documentation, Arduino offers accessibility and support for users of all skill levels. Its GPIO pins enable easy interfacing with sensors, actuators, and other peripherals. Offering a range of models suited to different project needs, Arduino facilitates tasks ranging from simple LED blinking to complex robotics and IoT applications. Overall, Arduino's affordability, simplicity, and flexibility make it a cornerstone of modern electronics prototyping and education.

### HC-SR04
The HC-SR04 sensor is a compact, high-precision ultrasonic module widely employed for distance measurement in robotics and automation projects. Emitting ultrasonic waves, it calculates object distance by measuring the time taken for the waves to bounce back. With a range of 2cm to 400cm, it offers versatility and accuracy. Its simple interface requires minimal GPIO pins, making it compatible with various microcontrollers like Arduino and Raspberry Pi. Cost-effective and reliable, it enables non-contact sensing suitable for obstacle detection, object tracking, and distance measurement applications, making it a popular choice for hobbyists, educators, and professionals.

# PROGRAM:
```C
const int trigpin=3,echopin=4;
float dist,time;

void setup() 
{
  Serial.begin(9600);
  pinMode(trigpin,OUTPUT);
  pinMode(echopin,INPUT);
}

void loop() 
{
  digitalWrite(trigpin,LOW);
  delay(100);
  digitalWrite(trigpin,HIGH);
  delay(1000);
  digitalWrite(trigpin,LOW);
  time=pulseIn(echopin,HIGH);
  dist=0.017*time;
  Serial.print("The distance:");
  Serial.println(dist);
  
}
```

# CIRCUIT DIAGRAM:

![image](https://github.com/Prajeeth17/Update-the-Ultrasonic-sensor-value-in-cloud/assets/120513885/b3a00112-678c-4cb8-8b5b-6cf446eb845c)

# OUTPUT:

![image](https://github.com/Prajeeth17/Update-the-Ultrasonic-sensor-value-in-cloud/assets/120513885/2821de20-4b71-43ab-84b9-a11f01e98fc3)

# RESULT:

Thus the Ultrasonic sensor value is displayed using Arduino controller.

