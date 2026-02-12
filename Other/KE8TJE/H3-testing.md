# H3 testing

## Charge controller bug

- Tested the H3 battery charging externaly out of the radio with USB C
	- after charging completed: 11.5 V (green LED)
	- disconnected the USB C: 8.4 v 
	- reconnected for charging: 8.4 V (indicated as charged by LED)
		- After 3h the voltage is still correctly at 8.4 V
- Retesting the used battery
	- 1641 : 7.5 V on the input
	- external connector is exposing the USB input at 5 V
	- 