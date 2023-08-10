# progroming-and-disagining-servo-and-DC-motor
**DC motor code**
```// C++ code
//
int i = 0;

int B = 0;

int j = 0;

void setup()
{
  pinMode(9, OUTPUT);
}

void loop()
{
  for (B = 0; B <= 255; B += 1) {
    analogWrite(9, B);
    delay(30); // Wait for 30 millisecond(s)
  }
  for (B = 255; B >= 0; B -= 1) {
    analogWrite(9, B);
    delay(30); // Wait for 30 millisecond(s)
  }
}
```
**Servo motor code**
```// C++ code
//
/*
  Sweep

  by BARRAGAN <http://barraganstudio.com>
  This example code is in the public domain.

  modified 8 Nov 2013  by Scott Fitzgerald
  http://www.arduino.cc/en/Tutorial/Sweep
*/

#include <Servo.h>

int pos = 0;

Servo servo_9;

void setup()
{
  servo_9.attach(9, 500, 2500);
}

void loop()
{
  // sweep the servo from 0 to 180 degrees in steps
  // of 1 degrees
  for (pos = 0; pos <= 180; pos += 1) {
    // tell servo to go to position in variable 'pos'
    servo_9.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
  for (pos = 180; pos >= 0; pos -= 1) {
    // tell servo to go to position in variable 'pos'
    servo_9.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
}
```
