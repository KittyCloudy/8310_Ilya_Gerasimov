# Отчет №1
## Илья Герасимов
### Группа 8310

[Ссылка на проект 3.1](https://www.tinkercad.com/things/4DQcLbs9mjk-neat-allis/editel?tenant=circuits)
![Alt text](img/Neat-Allis.png)

## Листинг программы 3.1
```C++
int LED1 = 13, LED2 = 12, i;
void setup()
{
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
}

void loop()
{
  for(i = 0; i < 4; i++)
  {
    delay(100);
    digitalWrite(LED2, HIGH);
    delay(550);
    digitalWrite(LED2, LOW);
    delay(550);
  }
  
  delay(1000);
  
  for(i = 0; i < 6; i++)
  {
    delay(100);
    digitalWrite(LED1, HIGH);
    delay(500);
    digitalWrite(LED1, LOW);
    delay(500);
  }
  delay(1000);
}
```
