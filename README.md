# Kerala-IoT-Challenge

> [**Foxlab Makerspace**](https://www.facebook.com/foxlabmakerspace/) in association with [**GTech - Group of Technology Companies**](https://atfg.gtechindia.org/) in Kerala is launching our prestigious program **“Kerala IoT Challenge 2021”**, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

> This page is maintained so as to keep the track of my experiments at different levels of the **Kerala IoT Challenge**.

# About Me
Hi,everyone I am Ansel Sebastian ,Currently pursuing B-tech from RIT Kottayam,My field of intrest are
* Robotics
* IoT
* Automation
* Projects 

# Experiment-1 HELLO WORLD LED BLINKING
Iintoduction to Arduino IDE and Its programming is intended here

## Components Required
* Arduino Uno R3 *1
* Bread Board *1
* Jumper Wires(Male to male ) *2
* LED *1
* 220 Ohm resistor *1
* Usb A to B cable *1
 
## Circuit Diagram
 ![](https://user-images.githubusercontent.com/95708160/147387609-b5e0f3f3-b38d-4238-9df4-a200e6406678.jpeg)
 
##  Code
 ```
 
 int ledPin=5;  //defining ledpin as pin 5
void setup() {
   pinMode(5,OUTPUT); //define pin5 as output type: 
}

void loop() {
  digitalWrite(ledPin,HIGH);//setting pin to on position
  delay(1000); //delay of 1 second
  digitalWrite(ledPin,LOW);//set led to off position
  delay(1000); //wait for a second
  
  

}
 ```
## Output
The LED blinks with a delay of one second 
 ![](https://user-images.githubusercontent.com/95708160/147388479-4a22307c-f547-4966-bcf2-cfc4f9be810f.gif)
 
 
 
# Experiment-2 Traffic Light

## Components Required

* Arduino board *1
* USB type A to B cable *1
* Red Led*1
* Yellow  LED*1
* Green LED*1
* 220ohm resistor *3
* Breadboard*1
* Breadboard jumper wires* several

## Circuit Diagram
![](https://user-images.githubusercontent.com/95708160/147388021-c1dcd075-6980-4278-acdc-6e65f96adda9.jpeg)

## Code

```
int Green=5;//defining ledpin as pin 5
int Yellow=8;//defining ledpin as pin 8
int Red=6;//defining ledpin as pin 6
void setup() {
   pinMode(5,OUTPUT); //define pin5 as output type: 
   pinMode(8,OUTPUT); //define pin8 as output type:
   pinMode(6,OUTPUT); //define pin6 as output type:
}

void loop() 
{
  digitalWrite(Green,HIGH);//setting Green to On position
  delay(5000); //delay of 5 second
  digitalWrite(Green,LOW);//set led to off position
  delay(1000); //wait for a second
  for(int i=1;i<=3;i++)
     {
      digitalWrite(Yellow,HIGH);//setting Yellow to On position
      delay(500); //delay of 0.5 second
      digitalWrite(Yellow,LOW);//set led to off position
      delay(500); //wait for 0.5 second
     }    // Blinks Yellow 3 times
      digitalWrite(Red,HIGH);//setting RED to On position
      delay(500); //delay of 5 second
      digitalWrite(Red,LOW);//set led to off position
      delay(500); //wait for 0.5 second
     
}
```
## Output
The green Led lights for five seconds followed by yellow LED blinking three times with a delay of 0.5seconds followed by the red LED ON for 5 seconds 
![](https://user-images.githubusercontent.com/95708160/147835010-9d50fff5-8f44-44a2-96e3-e504d8294237.gif)
## Observed Limitation  
When all the six Leds turn on at a time the brightness of LEDs reduce owing to the higher power demand than the output.


# Experiment-3 LED Chasing Effect
 In this experiment, we compile a program to simulate LED chasing effect.
 
## Components Required
* Arduino Uno *1nos
* Bread Board *1nos
* Usb Type A to Type B *1nos
* Jumper Cable *13nos
* Led *6nos
* 220ohm resistor*6nos

## Circuit Diagram
![](https://user-images.githubusercontent.com/95708160/147388050-c91db1bd-febc-4b23-bbd1-5cbe55789a78.jpeg)

## Code
```
int BASE = 2;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    //  turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // turning on LED s one by one
     delay(200);        // delay
   }  
}
```
##  OUTPUT
The Leds will all lights up with a delay of 0.2 seconds and then turns of one by one with a delay of 0.2 second
 ![](https://user-images.githubusercontent.com/95708160/147388536-50e1d46d-23a3-4101-9b8d-a555aab5759c.gif)
 
 
 # Experiment 4 BUTTON CONTROLLED LED
 
 Taking feedback from a button to control any output pin,also to study setting of pins as input.
 ## Components Required 
 * Arduino Uno*1
 * Usbtype A to type B cable*1
 * Button switch*1
 * Red M5 LED*1
 * 220ΩResistor*1
 * 10KΩ Resistor*1
 * Breadboard*1
 * Breadboard Jumper Wire*6
 
 ## Circuit Diagram
 ![](https://user-images.githubusercontent.com/95708160/147835043-41ab71e6-49de-4430-9aa3-c20a88e0f40e.jpeg)
 
 ## Code
 ```
 int ledpin=11;
int button=7;
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as output type
pinMode(button,INPUT);// set button as input pin
}
void loop()
{
val=digitalRead(button);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
  {
  digitalWrite(ledpin,LOW);
  }
else
  { 
  digitalWrite(ledpin,HIGH);}
  }
  ```
  ## OUTPUT 
  The led blinks as the button is pressed.
  ![](https://user-images.githubusercontent.com/95708160/147835211-cbac1881-55e0-43f8-83cb-5df7f88f2ae7.gif)
  
  
 # EXPERIMENT 5 Buzzer
 
 ## AIM
 To control a buzzer and manipulate delay to make tunes
 
 ## COMPONENTS REQUIRED
 * Arduino Uno
 * Buzzer*1
 * Breadboard*1
 * Breadboard Jumper Wire*2
 * USB type A to type b*1
  
 ## CIRCUIT DIAGRAM
 ![](https://user-images.githubusercontent.com/95708160/147835057-cecfa081-db21-4fb0-a296-7445a9cc94f5.jpeg)
 
 ## **CODE**
 ```
int buzzer=8;
void setup() 
{ 
  pinMode(buzzer,OUTPUT);
} 
void loop() 
{
digitalWrite(buzzer, HIGH);// produce tune
delay(100);
digitalWrite(buzzer, LOW);
delay(100);

}
```


## OUTPUT
The buzzer buzzes with a delay of 100ms
![](https://user-images.githubusercontent.com/95708160/147835183-a98a47b6-c13e-42b0-b464-de36c3074a94.gif)

# EXPERIMENT 6 RGB LED

## AIM
To control the RGB LED to give diffrent pattern output

## Note
An RGB LED bulb uses three diodes in Red, Green and Blue. These are mixed in different intensities to produce a variety of different colours. The process is based on additive color mixing, the same technique which is used in TV sets, computer monitors and flat screens.

analogWrite() takes two or three arguments:

pin: the number of the pin whose value you wish to set
value: the duty cycle: between 0 (always off) and 255 (always on). Since 0.6.0: between 0 and 255 (default 8-bit resolution) or 2^(analogWriteResolution(pin)) - 1 in general.
frequency: the PWM frequency (optional). If not specified, the default is 500 Hz.


## Components required
* Arduino Uno *1
* USB Cable type A to type B * 1
* RGB LED * 1
* Resistor 220ohm *1
* jumper wire*5
## Code
```
int redpin = 11; // red LED
int bluepin =10; //  blue LED
int greenpin =9;//  green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
```
## Circuit Diagram
![](https://user-images.githubusercontent.com/95708160/147835078-a7bffb41-32f2-4910-8369-1106b5a2ac6b.jpeg)

## OUTPUT
The  RGB LED glows with aspecific pattern and brightness level
![](https://user-images.githubusercontent.com/95708160/147835168-fe700260-dfc5-407d-a829-485e1f8a3c28.gif)

  
 




