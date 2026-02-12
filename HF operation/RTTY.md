# RTTY Operation 
By KE8TJE


- Interesting mode to operate. I tested operating during the 2025 WPX RTTY contest
- Made a total of 45 contacts for about 2h of operating and testing on 10/20/40 m bands

![400](res/Pasted%20image%2020250209221128.png)

- Used FLDIGI + N3FJP 
- Made a contact with **N3FJP**

## Setup instructions

### N3FJP
- Radio configuration was already done based on the setup
- Enable TCP connection on port 1100
### FLDIGI

- Open Config
- Audio config: set up the correct port for the radio you are using
- Contest: 
	- WPX: needed to send the log id this needs to be setup in the contest page
- Logger: Select N3FJP and click on connect
	- Looking for a green icon under the connect checkbox
	- once connected the text box should populate data and also mirror radio band settings correctly
- Setting up Macros:
	- CQ: `<TX> <MYCALL> <MYCALL> CQ <RX>`
	- RPLY: `<TX> <MYCALL> <MYCALL> <RX>`
	- Exchange: `<>`
