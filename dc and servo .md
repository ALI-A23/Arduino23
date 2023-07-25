//dc 
![Screenshot 2023-07-25 045800](https://github.com/ALI-A23/Arduino23/assets/138877069/a02b5e01-f33e-4d4b-ad83-d817120ed6fe)

int motorPin = 3;

void setup() {

}

void loop() {
   digitalWrite(motorPin, HIGH);
}

//servo 
![Screenshot 2023-07-25 045532](https://github.com/ALI-A23/Arduino23/assets/138877069/74f3b635-4303-465d-9cb7-0b038d15289e)

#include <Servo.h>

int pos = 0;

Servo servo_9;

void setup()
{
  servo_9.attach(11, 1000, 20);
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
