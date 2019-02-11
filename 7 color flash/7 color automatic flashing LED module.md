7 color automatic flashing LED module<br>
<br>
7 Color Auto Flash LED module uses a 5mm round head high brightness LED, which has the following features:<br>
1) Product Type: LED<br>
2) Product model: YB-3120B4PnYG-PM<br>
3) Product shape: In-line type 5mm round head LED<br>
4) Luminous color: pink yellow green (high brightness)<br>
5) Lens type: white mist<br>
6) Standard forward voltage: 3.0-4.5V

![](https://raw.githubusercontent.com/WengYongHao/37-in-1-sensors-kit-for-Arduino/master/7%20color%20flash/IMG/1.png)

```c
/*
 Arduino test cod:
 Blink
 Turns on an LED on for two second, then off for two second, repeatedly.
 This example code is in the public domain.
 */
void setup() {
 // initialize the digital pin as an output.
 // Pin 13 has an LED connected on most Arduino boards:
 pinMode(13, OUTPUT);
}
void loop() {
 digitalWrite(13, HIGH); // set the LED on
 delay(2000); // wait for a second
 digitalWrite(13, LOW); // set the LED off
 delay(2000); // wait for a second
}
```