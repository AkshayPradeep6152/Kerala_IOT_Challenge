# Kerala-IoT-Challenge
> "Kerala IoT Challenge 2021" is a program launched by Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala to mold IoT experts in Kerala.
# About Me
>Hello everyone👋, I am Akshay Pradeep, a 3rd-year Electronics and Communication Engineering student from College of Engineering Chengannur, I  am participating in this IoT challenge to learn more about the IoT and help others to learn IoT and complete the Kerala IoT Challenge 2021.

# Level 1
>In level 1 we are using Arduino for the experiments,
>Arduino is an open-source electronics platform based on easy-to-use hardware and software. It's intended for anyone making interactive projects.  
>I am using Arduino UNO and Arduino IDE from https://www.arduino.cc/en/software for level 1

## Arduino UNO
>![arduino uno](https://user-images.githubusercontent.com/65575529/146658512-36951b05-7ce5-49ee-bada-169fc0a14437.jpg)
>Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Arduino Uno Components
>![pin out](https://user-images.githubusercontent.com/65575529/146658693-bcd22880-7c50-4188-a3f3-64237a42d9b6.jpg)

# Exp 1: Hello World LED Blinking
>we are starting our IoT journey by Hello World LED Blinking using the microcontroller Arduino UNO

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) LED (Any Color) x 1 Nos  
4) 220 OHM Resistor X 1 Nos  
5) Breadboard  
6) Jumper Wires (Male to Male ) X 2 Nos  

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 2: Traffic Light
>Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED

## Components Required
1) Arduino board *1
2) USB cable *1 
3) Red M5 LED*1  
4) Yellow M5 LED*1  
5) Green M5 LED*1 
6) 220Ω resistor *3  
7) Breadboard*1
8) Breadboard jumper wires* several


## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 3: LED Chasing Effect
>In this experiment, we compile a program to simulate LED chasing effect.
The long lead of LED is the positive side; short lead is negative.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Led *6 
4) 220Ω resistor *6 
5) Breadboard  
6) Jumper Wires *13

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
int BASE = 2;  // the I/O pin for the first LED
int NUM = 6;     // number of LEDs
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
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
} 

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 4: Button Controlled LED
>In this experiment we will control led usinf a push button.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Button switch*1
4) Red M5 LED*1  
5) 220ΩResistor*1
6) 10KΩ Resistor*1  
7) Breadboard  
8) Breadboard Jumper Wire*6

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 5: Buzzer
>Now we are going to learn about the working of buzzer.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Buzzer*1
4) Breadboard*1
5)  Breadboard Jumper Wire*2

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 6: RGB LED
>Now we are going to learn about the working of RGB LED.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) RGB LED * 1
4) Resistor *3
5) Breadboard*1
6) Breadboard Jumper Wire*2

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
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

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 7: LDR Light Sensor
>Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Photo Resistor*1
4) Red M5 LED*1
5) 10KΩ Resistor*1
6) 220Ω Resistor*1
7) Breadboard*1
8) Breadboard Jumper Wire*5

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int potpin=0;// initialize analog pin 0, connected with photovaristor
int ledpin=10;// initialize digital pin 11, 
int val=0;// initialize variable val
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin 11 as “output”
Serial.begin(9600);// set baud rate at “9600”
}
void loop()
{
val=analogRead(potpin);// read the value of the sensor and assign it to val
Serial.println(val);// display the value of val
analogWrite(ledpin,val);// set up brightness（maximum value 255）
delay(10);// wait for 0.01 
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 8: Flame Sensor
>We are using Infrared Receiver (IR )for detecting Flame.

## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) Flame Sensor *1 
4) Buzzer*1
5) 10K Resistor *1
6) Breadboard*1
7)  Breadboard Jumper Wire*2

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;

void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    Serial.println("Fire!!!");
    digitalWrite(buzzerPin, HIGH);
  }
  else
  {
    Serial.println("No worries");
    digitalWrite(buzzerPin, LOW);
  }
}
```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 9: LM35 Temperature Sensor
>LM35 is a common and easy-to-use temperature sensor.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) LM35*1
4) Breadboard*1
5) Breadboard Jumper Wire*2

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 10: IR Remote Control Using TSOP
>Now we are going to learn about the working of IR Remote Control Using TSOP.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Infrared Remote Controller(You can use TV Remote or any other remote) *1
4) Infrared Receiver *1
5) LED *6
6) 220ΩResistor *6
7) Breadboard*1
8) Breadboard Jumper Wire*2

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 #include <IRremote.h>
int RECV_PIN = 10;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
int LED4 = 5;
int LED5 = 6;
int LED6 = 7;
long on1  = 0x00FF6897;
long off1 = 0x00FF9867;
long on2 = 0x00FFB04F;
long off2 = 0x00FF30CF;
long on3 = 0x00FF18E7;
long off3 = 0x00FF7A85;
long on4 = 0x00FF10EF;
long off4 = 0x00FF38C7;
long on5 = 0x00FF5AA5;
long off5 = 0x00FF42BD;
long on6 = 0x00FF4AB5;
long off6 = 0x00FF52AD;
IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if ((i%2)==1) {
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
  pinMode(LED5, OUTPUT);
  pinMode(LED6, OUTPUT);  
  //pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
       on =!on;
//       digitalWrite(8, on ? HIGH : LOW);
       digitalWrite(13, on? HIGH:LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);
    if (results.value == on4 )
       digitalWrite(LED4, HIGH);
    if (results.value == off4 )
       digitalWrite(LED4, LOW); 
    if (results.value == on5 )
       digitalWrite(LED5, HIGH);
    if (results.value == off5 )
       digitalWrite(LED5, LOW); 
    if (results.value == on6 )
       digitalWrite(LED6, HIGH);
    if (results.value == off6 )
       digitalWrite(LED6, LOW);        
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 11: Potentiometer analog Value Reading
>In this experiment we are reading value(Analog Value) from a Potentiometer

## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) 10K Potentiometer *1
4) Breadboard*1
5) Breadboard Jumper Wire*3

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 12: 7 Segment Display
>LED segment display is a semiconductor light-emitting device. Its basic unit is a light-emitting diode (LED). LED segment display can be divided into 7-segment display and 8-segment display according to the number of segments.

## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) 1-digit LED Segment Display*1
4) 220Ω Resistor*8
5) Breadboard Jumper Wire*2
6) Breadboard*1

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
// Include the library
#include <TM1637Display.h>

// Define the connections pins
#define CLK 3
#define DIO 4

// Create a display object of type TM1637Display
TM1637Display display = TM1637Display(CLK, DIO);

// Create an array that turns all segments ON
const uint8_t allON[] = {0xff, 0xff, 0xff, 0xff};

// Create an array that turns all segments OFF
const uint8_t allOFF[] = {0x00, 0x00, 0x00, 0x00};

// Create an array that sets individual segments per digit to display the word "dOnE"
const uint8_t done[] = {
  SEG_B | SEG_C | SEG_D | SEG_E | SEG_G,           // d
  SEG_A | SEG_B | SEG_C | SEG_D | SEG_E | SEG_F,   // O
  SEG_C | SEG_E | SEG_G,                           // n
  SEG_A | SEG_D | SEG_E | SEG_F | SEG_G            // E
};

// Create degree celsius symbol
const uint8_t celsius[] = {
  SEG_A | SEG_B | SEG_F | SEG_G,  // Degree symbol
  SEG_A | SEG_D | SEG_E | SEG_F   // C
};

void setup() {

}

void loop() {
  // Set the brightness to 5 (0=dimmest 7=brightest)
  display.setBrightness(5);

  // Set all segments ON
  display.setSegments(allON);

  delay(2000);
  display.clear();

  // Show counter 0-9
  int i;
  for (i = 0; i < 10; i++) {
    display.showNumberDec(i);
    delay(50);
  }

  delay(2000);
  display.clear();

  display.showNumberDec(-12);     // Prints _-12
  delay(2000);
  display.clear();
  
  display.showNumberDec(-999);    // Prints -999
  delay(2000);
  display.clear();
  
  display.showNumberDec(31, false); // Prints __31
  delay(2000);
  display.clear();
  
  display.showNumberDec(31, true);  // Prints 0031
  delay(2000);
  display.clear();
  
  display.showNumberDec(14, false, 2, 1); // Prints _14_
  delay(2000);
  display.clear();
  
  display.showNumberDec(-5, false, 3, 0); // Prints _-5_
  delay(2000);
  display.clear();

  // Prints 12:34
  display.showNumberDecEx(1234, 0b11100000, false, 4, 0);

  delay(2000);
  display.clear();

  // Prints 15°C
  int temperature = 15;
  display.showNumberDec(temperature, false, 2, 0);
  display.setSegments(celsius, 2, 2);

  delay(2000);
  display.clear();
  
  // Prints dOnE
  display.setSegments(done);

  while(1);
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Assignment 1: Flame Sensor
>We are using Infrared Receiver (IR )for detecting Flame.

## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) Flame Sensor *1 
4) Buzzer*1
5) 10K Resistor *1
6) Breadboard*1
7)  Breadboard Jumper Wire*2

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;

void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    Serial.println("Fire!!!");
    digitalWrite(buzzerPin, HIGH);
  }
  else
  {
    Serial.println("No worries");
    digitalWrite(buzzerPin, LOW);
  }
}
```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Assignment 2: Flame Sensor
>We are using Infrared Receiver (IR )for detecting Flame.

## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) Flame Sensor *1 
4) Buzzer*1
5) 10K Resistor *1
6) Breadboard*1
7)  Breadboard Jumper Wire*2

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;

void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    Serial.println("Fire!!!");
    digitalWrite(buzzerPin, HIGH);
  }
  else
  {
    Serial.println("No worries");
    digitalWrite(buzzerPin, LOW);
  }
}
```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
