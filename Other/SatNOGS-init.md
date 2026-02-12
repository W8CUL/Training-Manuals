# SatNOGS


## 02.07.2025  
by KE8TJE + KC3YAL

Temp docs for easy access: https://pad.education/p/arc-sat
### Yagi controller designs 

#### online docs

- https://github.com/k3ng/k3ng_rotator_controller
- https://www.minikits.com.au/doc/K3NG_Quick_Start.pdf
	- Most of these commands were tested and they work as expected 
#### PCB schematic 
- Find the schematic + PCB
- We labeled some of the pins
### Pin out map
- Needs filling by KC3YAL. convert image to a table here
### Observations  - KE8TJE

- We tested the pin outs documented above 
- the Ardunio and the hat that had been built tested fine
- One direction was not triggering 
	- BLUE wire on the external interface connector 
	- It would work when tested manually by connecting it to the ground pin
	- With the BJT it would not work 
		- Some internal issue. BJT is fine 
		- likely option is that the internal rotator controller interface has a slightly different value
		- options to test: 
			- [x] Use a BS170 and try if that works
				- This works with 5V supplied by the arduino, but not with digital IO
				- Possible that the configuration was the issue
			- [ ] Reduce the $R_c$ resistance and see if that changes any thing


### Software customization

- K3NG is a very general control system
	- We should put a IMC and a display for feedback
	- add LED's to the control input 
- Change pin configs in `rotator_pins.h`

---
## Internal controller diagnostic

- Open up the controller 
- Check the D1015s and see if they all physically look good
	- Opened it up but nothing significant


---
## 2025.02.15
by KE8YJE +KC3YAL 

- Fixed all the electrical issues in the PCB
	- Soldering was not great, there were shorts on the analog input side preventing calibration efforts
	- They are now acting as expected. With the addition of a BS170 for the Right signal(Blue wire)
- Start guide https://www.minikits.com.au/doc/K3NG_Quick_Start.pdf
	- Not working: Calibration may be out dated
- To-DO
	- New instructions and calibration testing command [here](https://github.com/k3ng/k3ng_rotator_controller/wiki/500-Heading-Calibration)
	- available command: https://github.com/k3ng/k3ng_rotator_controller/wiki/820-Command-Reference
		- `\d` command will give you status and should help calibrate and debug
	- Antennas are mounted in the wrong orientation. They need to be rotated fix the rotation
### Pin specs for the PCB

- 1 V Feedback (Purple)
- 2 Right > Q4 > D6 (Green)
- 3 Up > Q3 > D7 (Yellow)
- 4 Left > Q2 > D8 (Blue)
- 5 Down > Q1 > D9 (Orange)
- 6 H Feedback > A0 (Grey)
- 7 VIN- not used >A1 (Red)
- GND (White/Black)

#### Observations - KC3YAL
- New circuit board was made for the LEFT(CCW) signal
	- This fixed the intermittent connection on the blue wire (PIN 4)
- Pins Soldered directly to the PCB
	- A New PCB will have to be made that includes Debugging LED's and a 8 Pin jack for easier/better connection
---
## 2025.02.16

- Fixed all the software issues 
- Rotated it to the correct orientation
- Debug log for later comparison

![](res/Pasted%20image%2020250216095152.png)

- Things to be fixed
	- Put lock washers in the VHF side
- hamlib can be used to interface the arduino
	- `rotctld -m 603 -vvv -r /dev/ttyACM0 -t 4533 -s 9600`
- I am using Gpredict to both control the Yagi and an SDR frequency correction 
- Tracking threshold was set to $5\degree$  for usable tracking
- Calibration for Az was redone - this needs to be confirmed actually with the system to see if the rotation is consistent with the needle and the controller software
- Initial test image from NOAA 19: there was a bug on the calibration at the time
	- EL was working smoothly
	- AZ was saturated and this was identified and fixed
![](res/Pasted%20image%2020250216122735.png)

### Notes on K3NG SW
- No major changes are needed after the correct branch was used
- Saving settings and calibration are the most important settings
- I physically moved the rotator to have N corrected. software corrections are available as well

----
## Contacts

- Status: https://www.amsat.org/status/
- Log contacts 

---
