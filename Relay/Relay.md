<b>Main Purpose</b><br>
The relay is an automatic switching element with isolation function, which is widely used in remote control, telemetry, communication, automatic control,<br>
Among the mechatronics and power electronics, it is one of the most important control components.<br>
It comes down to the following effects:<br>
1) Expand the control range: For example, when the multi-contact relay control signal reaches a certain value, it can press the contact group<br>
In the same form, switch, disconnect, and turn on multiple circuits at the same time.<br>
2) Amplification: For example, sensitive relays, intermediate relays, etc., can be controlled with a very small amount of control.<br>
Power circuit.<br>
3) Integrated signal: For example, when multiple control signals are input into a multi-winding relay in a prescribed form,<br>
In order to achieve the predetermined control effect.<br>
4) Automatic, remote control, monitoring: For example, the relay on the automatic device can be programmed together with other electrical appliances.<br>
Making lines for automated operation


<b>Precautions</b><br>
1) Rated working voltage: refers to the voltage required by the coil when the relay is working normally.<br>
That is, the control voltage of the control circuit. Depending on the type of relay, it can be AC<br>
The voltage can also be a DC voltage.<br>
2) DC resistance: refers to the DC resistance of the coil in the relay, which can be measured by a multimeter.<br>
3) Pull-in current: refers to the minimum current that the relay can generate the pull-in action. In normal use, the given current must<br>
It must be slightly larger than the pull-in current so that the relay can work stably. And for the working voltage applied by the coil, generally not<br>
To exceed 1.5 times the rated working voltage, otherwise a large current will be generated and the coil will be burnt.<br>
4) Release current: refers to the maximum current that the relay generates to release. When the current in the state of the relay is reduced to one<br>
At a certain level, the relay will return to the unpowered release state. The current at this time is much smaller than the pull-in current.<br>
5) Contact switching voltage and current: refers to the voltage and current that the relay is allowed to load. It determines the relay can control<br>
The voltage and current should not exceed this value when used, otherwise it will easily damage the contacts of the relay.


<b>Module Test</b><br>
The pin description is as follows:
![](https://raw.githubusercontent.com/WengYongHao/37-in-1-sensors-kit-for-Arduino/master/Relay/IMG/20190211210333.jpg)

Description: COM is connected to VCC, and NO is connected to the anode of the LED we want to control.<br>
When the relay is turned on, the LED will light up;<br>
Look at what you need to prepare to complete this test. They have specific<br>
Arduino Controller × 1<br>
USB data cable × 1<br>
1 way relay module × 1<br>
Led indicator × 1<br>
Resistance of resistance 330 × 1<br>
<br>
Physical connection for reference:<br>
![](https://raw.githubusercontent.com/WengYongHao/37-in-1-sensors-kit-for-Arduino/master/Relay/IMG/20190211212939.png)

```c
int relay = 10; //Relay turn-on trigger signal - active high

void setup()
{
 pinMode(relay,OUTPUT); //Define port properties as output
}
void loop()
{
 digitalWrite(relay,HIGH); //The relay is turned on
 delay(1000);
 digitalWrite(relay,LOW); //Relay switch disconnected
 delay(1000);
} 
```

