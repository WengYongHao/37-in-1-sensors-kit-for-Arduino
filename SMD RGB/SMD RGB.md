
![](https://raw.githubusercontent.com/WengYongHao/37-in-1-sensors-kit-for-Arduino/master/SMD%20RGB/IMG/1.png)

3 color - full color LED module<br>
<br>
Overview:<br>
The RGB LED module is made of a plug-in full-color LED that can be adjusted by the PWM voltage inputs of the R, G, and B pins.<br>
The intensity of the three primary colors (red/blue/green) is achieved to achieve a full-color color mixing effect. Control of the module with Arduino<br>
Cool lighting effects.<br>
<br>
Product Features:<br>
1, use plug-in full color LED<br>
2, RGB three primary color connected to the current limiting resistor to prevent burnout<br>
3, through the PWM adjustment three primary colors can be mixed to get different colors<br>
4, can interface with various microcontrollers<br>
5, working voltage: 5V<br>
6, LED drive mode: common negative drive




```c
//Arduino test code：
int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
	pinMode(redpin, OUTPUT);
	pinMode(bluepin, OUTPUT);
	pinMode(greenpin, OUTPUT);
	Serial.begin(9600);
}
void loop()
{
	for(val=255; val>0; val--)
	 {
		 analogWrite(11, val);
		 analogWrite(10, 255-val);
		 analogWrite(9, 128-val);
		 delay(1);
	 }
	for(val=0; val<255; val++)
	 {
		 analogWrite(11, val);
		 analogWrite(10, 255-val);
		 analogWrite(9, 128-val);
		 delay(1);
	 }
	 Serial.println(val, DEC);
}
```