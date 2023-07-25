//dc 
int motorPin = 3;

void setup() {

}

void loop() {
   digitalWrite(motorPin, HIGH);
}
![Screenshot (10)](https://github.com/ALI-A23/Arduino23/assets/138877069/58324340-2ab6-4b84-8a12-14fe931e55a0)
//servo 
![Screenshot (13)](https://github.com/ALI-A23/Arduino23/assets/138877069/96632de5-2ca7-4031-8f60-83c63a244c6f)
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
