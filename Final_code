Final_DIGF-2B03
===============
/*--------------------------------------
 KENIX PO
 2434140
 [Final]
 --------------------------------------*/

#include <DistanceGP2Y0A21YK.h>
DistanceGP2Y0A21YK Dist;

//----------[Variables]----------
int distance;
//
int switchPin = 12;
int pumpPin = 13;


void setup()
{
  Serial.begin(9600);
  Dist.begin(A5);
  //
  pinMode(switchPin, INPUT);
  pinMode(pumpPin, OUTPUT);
}// setup ends

void loop()
{
  //-----[Serial Monitor]-----
  distance = Dist.getDistanceCentimeter();
  Serial.print("\nDistance in centimers: ");
  Serial.print(distance);  
  delay(100);
  //
  if ((digitalRead(switchPin) == HIGH) && (distance <= 10)){
    digitalWrite(pumpPin, HIGH);
    delay(30000);
    digitalWrite(pumpPin, LOW);
    Serial.print("switchState is high");
  }

}// loop ends
