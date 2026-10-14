# Alcohol
To dected where  wearer drink alcohol 
void setup()
{
  // put your setup code here, to run once:
  pinMode(2,INPUT);
  pinMode(7,INPUT);
  pinMode(4,OUTPUT);
  Serial.begin(9600);
}

void loop() 
{
  int a,b;
  a=digitalRead(7);
  b=digitalRead(2);
  Serial.print("a= ");
  Serial.println(a );
  Serial.print("b= ");
  Serial.println(b);
  delay(500);
  if(a==1&&b==1)
  {
    digitalWrite(4,HIGH);
  }
  if(a==0&&b==1)
  {
    digitalWrite(4,LOW);
  }
  
    if(a==1&&b==0)
  {
    digitalWrite(4,LOW);
  }

}
