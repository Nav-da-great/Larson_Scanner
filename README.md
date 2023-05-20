# Larson_Scanner using Arduino Uno R3
https://www.tinkercad.com/things/9acZBzF07nD

# This is the code for my version of the Larson Scanner
```int Pin[] = {13,12,11,10,9,8}; //Initializing pins
void setup()
{
  int counter1;		//Creating an iterator for the loop
  for(counter1 = 0; counter1 < 6; counter1++){
    pinMode(Pin[counter1], OUTPUT); //Sending OUTPUT signal to respective pins
  }
}

void loop()
{
  int counter2;		//Creating another iterator for the loop
  //Creating a loop for left to right
  for(counter2=0; counter2 < 6; counter2++){
  	digitalWrite(Pin[counter2], HIGH);	//Sending a digital signal for 100 milliseconds
    delay(100);
    digitalWrite(Pin[counter2], LOW);
  }
  //Creating a loop for right to left
  for(counter2=4; counter2 > -1; counter2--){
    digitalWrite(Pin[counter2], HIGH);
    delay(100);
    digitalWrite(Pin[counter2], LOW);
  }
  delay(100);	//Delaying the overall loop by 100 milliseconds
}

//Voila! :)
