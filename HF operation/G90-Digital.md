# G90 - Digital modes
by KE8TJE and KC3YLF 
last updated: December 2024

#HF #G90 #Digital #FT8 

- To use and operate on Digital modes you need the Digital add ons for the G90. 
- At the time of writing these were housed in a brown cardboard box.
- The content of the box is shown below 
	- A: USB sound card interface with CAT control
	- B: USB C cable
	- C: mini Din connector
	- D: 3.5 mm audio connector

![](res/Pasted%20image%2020241229191640.png)

---
## Configuration with FT8

- Connect the DE19 unit to the radio
	- Mini DIN connector -> back of the radio
	- 3.5 mm Audio cable -> to the head of the radio data port (icon with a man)

- Once you have the connections made turn on the radio and plug in the USB.
- It should show up as an extra sound card and a USB serial port
	- If the com port is not shown a driver is needed can be found [here](https://www.radioddity.com/pages/xiegu-download?srsltid=AfmBOoqLrWdmAihtAQWSQnbb37YU3xDsbe_omabtoGfEIx_bvfyXcE1P)
	- At the time of writing on win 11 (Jan 2025)
		- The available setup.exe did not work to install it
		- Go to device manager
		- Right click on the device with errors
		- Browse the drive manually 
- To use the device change the following settings in WSJT-x or any other applications
	- Select "Xiegu G90" as the radio
	- Baud rate: 19200
	- CAT control 
	- Test the connection 

