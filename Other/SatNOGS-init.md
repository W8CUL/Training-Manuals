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


## Software customization

- K3NG is a very general control system
	- We should put a IMC and a display for feedback
	- add LED's to the control input 
- Change pin configs in `rotator_pins.h`

---
## Internal controller diagnostic

- Open up the controller 
- Check the D1015s and see if they all physically look good