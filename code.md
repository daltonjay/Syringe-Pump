# Code for Syringe Pump Operation

- [Home](/Syringe-Pump/index)
- [Mechanics](/Syringe-Pump/mechanics)
- [Electronics](/Syringe-Pump/electrical)
- [**Code**](/Syringe-Pump/code)

The code below works for Arduino Uno or Mega. Load the code in the Arduino IDE to operate the syringe pump.
Code for the retraction of the syringe pump is commented out, but may be used by removing // characters in front of the line of code you are interested in.

In it's current state, the code will continuously extrude. Step size per revolution is set to accomadate for one sixteenth microstepping to achieve higher resolution.
```
// Define pin connections & motor's steps per revolution
const int dirPin = 2;
const int stepPin = 3;
const int stepsPerRevolution = 3200;

void setup()
{
  // Declare pins as Outputs
  pinMode(stepPin, OUTPUT);
  pinMode(dirPin, OUTPUT);
}
void loop()
{
  // Set motor direction clockwise
 // digitalWrite(dirPin, HIGH);

  // Spin motor slowly
 // for(int x = 0; x < stepsPerRevolution; x++)
  //{
 //   digitalWrite(stepPin, HIGH);
 //   delayMicroseconds(2000);
   // digitalWrite(stepPin, LOW);
   // delayMicroseconds(2000);
 // }
 // delay(1000); // Wait a second
  
  // Set motor direction counterclockwise
  digitalWrite(dirPin, HIGH);

  // Spin motor quickly
  for(int x = 0; x < stepsPerRevolution; x++)
  {
    digitalWrite(stepPin, HIGH);
    delayMicroseconds(1000);
    digitalWrite(stepPin, LOW);
    delayMicroseconds(1000);
  }
 // delay(1000); // Wait a second
}
```
