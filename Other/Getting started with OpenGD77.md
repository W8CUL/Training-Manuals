## Getting started with DMR with GD77
*Last updated: January 2024 by KE8TJE*

This is a guide written to program GD77 Radios using the openGD77 firmware.
## Setting up the CPS

In order to program new channels, Radio ID you need the following installed in your system.
If you are using the new shack computer most of this setup is already done on that computer

- Install the CPS. [latest](https://www.opengd77.com/downloads/PC_CPS/Latest/)
- The installer will ask for a password and that is the version number starting with R. This will be shown in the installer title. eg R2023.11.26.02
- Once you have it installed to enable DMR when you are programming you need a portion of the original GD77 software. its available in this [repo](./binary) or from the GD77 original firmware 4.6 Ham version
- Follow instructions [here](https://www.opengd77.com/viewtopic.php?f=5&t=1770) to setup the CPS
- **Note:** to program this radio you need a Radiodity cable. ***DO NOT USE OTHER CABLES THIS CAN HARM THE RADIO**
- An initial code-plug is available as a starting point: [here](./binary)
	- Change the following:
		- radio ID
		- Boot screen name to indicate your call sign
	- Current code-plug is arranged with a couple of zones for organization. You can think of a zone as a collection of channels/repeaters you would at any given time.
		- for an example I have the following zone
			- Morgantown : The main 2m/70cm repeaters available, M16,M22,APRS ,146.520 
			- W8CUL-DMR: DMR channels that can be used with our repeater
			- Travel : APRS,146.520,146.550
			- GMRS/FRS
			- Weather
---
### Useful links
- https://www.opengd77.com/
- [Radio Manual](https://github.com/LibreDMR/OpenGD77_UserGuide/blob/master/OpenGD77_User_Guide.md)
- keymap : 
![|400](res/Pasted%20image%2020240121125008.png)

--- 
## Alternate method to program the Radio-ID

- The primary method for installing and updating you DMR ID is to re-programme the radio using the latest CPS with a new code plug 
- If you want to test a club radio for a net/some short term activity its possible to set a custom DMR ID for a selected DMR channel
	- Select the needed DMR channet. *i.e.* W8CUL-L (the local repeater with TG:310796) 
	- Enter settings (green button)
	- Select DMR ID > Enter your DMR id > save (green button)
	- To change to the current code plug press (blue + green) this will exit the menu and changes will be committed to memory. (***Note: after use return the setting to DMR ID 0000**

---
# Basic operation in DMR

listing down a couple of terms that are used often 

- Color code (CC):  this is similar to the CTCSS tone in analog FM needs to be matched in order to use a repeater
- Talk Group (TG):  These you can think of as separate chat rooms that a connected via the internet
- Time slot(TS): we have 2 time slots in W8CUL and if some one is using TS1 more to TS2. Note TS2 should be used always when using the TG-3154 (this is the West Virginia state wide link)
- Private Call(PC): This would be a point-to-poin connection to the specific contact

---
## First test - Parrot

Once you have programmed the radio with your callsign and the radio ID you can use the Parrot to see if you can reach the repeater and how the signal propagation is.

- Select W8CUL DMR zone: (Blue + up/down arrow untill you are in the correct zone)
- Select W8CUL-D TS1: use up arrow to move channels. ch1 in the default codeplug
- select Parrot 9990: left key until you find the correct one
- Double check the time slot and color code shown on the very top of the display
---
1. Once you have it selected the above channel and the PC key up the repeater.
	- RED TX led will start with a blink and stabilize once a connection is established with the repeater and no one else is transmitting. 
	- in case you don's see a solid red light you are out of rage of the repeater. please change your location/antenna and try again
3. If you see a solid red light  then give your call sign and a short phrase (eg. KE8TJE Testing DMR) and release your PTT.
4. The light should turn green and after a short delay you will here your recorded voice. You can get an idea of how you sound like and change settings as needed.
	- Advanced settings: DMR Mic gain and AGC are available options 
5. **Congratulations !!  If you get to this point you have configured your radio correctly and every thing is working you are ready for DMR**
---
## Using a TG:

- Select the following and set them 
	- Repeater: W8CUL-DMR
	- TS:1
-  Once you have every thing set up to attach a new TG
	- if its already programmed in to the radio select the TG and key up the repeater
	- if its a new/know talk group 
		- click `#` to get in to the `TG entry` menu
		- Enter the ID
		- Key up the repeater 
---
### Disconnecting a TG

Disconnecting a TG is often is a good practice. Our repeater is configured internally to drop any inactive channels after 20 minutes of inactivity
If you want to force terminate a TG
- using the same TS make a contact to `TG 4000`. This will cause the repeater to drop the connection 
- Its important to make this contact while no active transmission is on the active Talk group. I have found it often very hard to un-link from popular/busy TG's 


*Note: Question/Comments [email KE8TJE](mailto:ke8tje@gmail.com).*


