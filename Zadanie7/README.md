# Отчет №2
## Илья Герасимов
### Группа 8310

[Ссылка на проект 4.1](https://www.tinkercad.com/things/bWlSh8A9RAY)
![Alt text](img/5.png)

## Листинг программы 5
```C++
#include<Keypad.h>
const byte ROWS = 4;
const byte COLS = 3;
char hexaKeys[ROWS][COLS] = {
{'1','2','3'}, 
{'4','5','6'},
{'7','8','9'},
{'*','0','#'}
};
byte rowPins[ROWS] = {13, 12, 11, 10};
byte colPins[COLS] = {9, 8, 7};
Keypad customKeypad = Keypad( makeKeymap(hexaKeys), rowPins, colPins, ROWS, COLS); 

void setup(){
Serial.begin(9600);
  pinMode(6, OUTPUT);
  pinMode(7, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(2, OUTPUT);
}

void loop()
{
char customKey = customKeypad.getKey();
  
if (customKey)
{
	Serial.println(customKey);
} 
if (customKey =='1' )
{
	digitalWrite(6, HIGH);
}
  
if (customKey =='2' )
{
	digitalWrite(6, LOW);
}
  
if (customKey =='3' )
{
	digitalWrite(5, HIGH);
}
if (customKey =='4' )
{
digitalWrite(5, LOW);
}
  
  
if (customKey =='5' )
{
	digitalWrite(4, HIGH);
}
if (customKey =='6' )
{
	digitalWrite(4, LOW);
}
     
if (customKey =='7' )
{
	digitalWrite(3, HIGH);
} 
if (customKey =='8' )
{
	digitalWrite(3, LOW);
}
  
if (customKey =='9' )
{
	digitalWrite(2, HIGH);
}
if (customKey =='0' )
{
	digitalWrite(2, LOW);
}
  
}
```