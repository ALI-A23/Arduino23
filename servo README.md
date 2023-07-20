![Screenshot 2023-07-20 211012](https://github.com/ALI-A23/Arduino23/assets/138877069/11d1e3a4-eb50-405a-a76c-8b0ec3258c10)
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
