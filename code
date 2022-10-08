#include <Servo.h>

Servo myservo; 

int swPin = A7;
int inputVal = 0;

void setup() {
  myservo.attach(2);  
  Serial.begin(9600);
  myservo.write(10);
}




int inchide(){
  int viteza1 = random(1,10);
  int viteza2 = random(1,50);
  int bec = random(1,10);
  if(bec > 2){
    for(int pos = 0; pos <= 110; pos++){
        myservo.write(pos);
        delay(viteza1);
      }
      delay (random(100,5000));
      for(int pos = 110; pos <= 145; pos++){
        myservo.write(pos);
        delay(viteza2);
      }
      delay(200);
      myservo.write(10);
  }
  
  if(bec == 1){
    for(int pos = 0; pos <= 110; pos++){
        myservo.write(pos);
        delay(viteza1);
      }
      delay(500);
      myservo.write(10);
      delay(random(1000,6000));
            for(int pos = 0; pos <= 145; pos++){
        myservo.write(pos);
        delay(3);
      }
      delay(200);
      myservo.write(10);   
  } 
}

void loop() {
  inputVal = analogRead(swPin);
  Serial.println (inputVal);
  
  if(inputVal > 1000){
    inchide();
  }
 delay(700);
}
