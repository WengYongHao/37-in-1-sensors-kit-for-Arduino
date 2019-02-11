![](https://raw.githubusercontent.com/WengYongHao/37-in-1-sensors-kit-for-Arduino/master/two-color%20LED%20(common-cathode)%20module/IMG/1.png)


/**
	TWO-color
	3mm red and green two-color LED (common-cathode) module
	
	Luminous color: green + red
	Diameter: 3mm
	Package color: none
	Package Type: Diffusion
	Use voltage (V): 2.0-2.5
	Current used (MA): 10
	Luminous angle: 150
	Wavelength (NM): 571 + 644
	Luminous intensity (MCD): 20-40; 40-80
	Bracket type: long foot
	Products are widely used in electronic dictionaries, PDA, MP3, headphones, digital cameras, VCD, DVD, car audio, communications, computers,
	Chargers, amplifiers, instrumentation, gifts, electronic toys and mobile phones and many other fields.

*/


![](https://raw.githubusercontent.com/WengYongHao/37-in-1-sensors-kit-for-Arduino/master/two-color%20LED%20(common-cathode)%20module/IMG/2.png)




//Arduino test code:
int redpin = 11; // select the pin for the red LED
int bluepin =10; // select the pin for the blueLED
int val;
void setup() {
 pinMode(redpin, OUTPUT);
 pinMode(bluepin, OUTPUT);
 Serial.begin(9600);
}
void loop()
{
for(val=255; val>0; val--)
 {
 analogWrite(11, val);
 analogWrite(10, 255-val);
 delay(15);
 }
for(val=0; val<255; val++)
 {
 analogWrite(11, val);
 analogWrite(10, 255-val);
 delay(15);
 }
 Serial.println(val, DEC);
}
