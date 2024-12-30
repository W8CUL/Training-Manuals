# DIY 2m - Slim Jim

Author : KE8TJE 
Last updated: April 2024

A Slim Jim is a rollable/flexible antenna made out of ladder line. It can be connected to your handheld or mobile radio to significantly boost its range.  This would be a good addition to your toolkit as a ham to increase your reach in a practical or emergency situation. 
## 1. Building instructions

Note: Following instruction are based on information available [here](https://m0ukd.com/calculators/slim-jim-and-j-pole-calculator/) and customized based on testing with the material available to us. The following figure will be used when providing dimensions in the following sections 

![200](res/Pasted%20image%2020240417230945.png)

1. Select a section of ladder line (we are using a 450 $\Omega$)  at least about **157 cm** in length. the goal is to solder the top and bottom ends to make a big loop.
2. Trim, Bend and solder the top an bottom joints to match a total length (measurement A) of **154.4 cm**. The following image shows how a typical joint should look like.
	![200](res/Pasted%20image%2020240417231811.png)
	 - Note: If this is your first time soldering ask for help. A key point is you need to heat all the surfaces before you apply solder on to it and keep them stable until they solidify 
3. Remove the outer jacket on both sides of the ladder line from about 5 - 8 cm from one end. This would be the region where the coax cable is going to be soldered in. (tuning needs to be done refer next section)
4. Take the unterminated end of your coax and carefully open up the outer black jacket. (about 3 cm in length)
	- twist the outer shield copper strands to one side
	- clear out the inner jacket (white insulator) for a length of about 1 cm
	- Use solder and tin the ends of the conductors. 
	  Info: tinning is a term often used to describe applying solder to an open end of a wire or a connector
	- ![Image on unsoldered coax is needed here]() 
- Notes: at the end of this step you should have
	- a length of ladder line making a conducting loop and removed jacket sections 
	- A length coax with one end with a BNC connector and the other end tinned and prepared for soldering
## 2. Tuning your antenna 

Please read the following section fully before making any modifications.

- This antenna is mainly tuned by changing the length C to match the general frequency we need. Ideally we would want this antenna to work across the whole band so tuning it at 146.00 MHz would be a good idea.
	- This value can be calculated using online calculators but it is highly sensitive to material properties and even the solder joints.
	- Experimentally I have found out 43 cm from the bottom is a good starting point. and you can shorten the length C incrementally to fine tune it
	- Make a test cut at 43 cm from the bottom of the antenna: and remove 5 mm of conductor
	- Next connect connecting the coax
		- Center conductor should connect to the long side (connector 1)
		- Outer conductor should go to the short side (connector 2)
- The following figure shows you a schematic of what is explained above. If you are unsure about any thing fell free to ask the organizers

- After soldering the coax: 

- Finally make 4 small loops with a diameter of about 10 cm in the coax as close to the ladder line joint as possible. Use tape to make it hold its shape. this is called a ["choke balun"](https://pf9z.com/rf-choke-build-your-own/)

### 3. Actual testing

- Once you have done the first cut and soldered the coax correctly you can take it up to one of the test stations available.
	- One of the key things when tuning a slim Jim is to make sure its in its fully stretched position. Use the provided paracode to mount it properly 
	- During testing keep any conductors from touching/being close to the antenna by atleast 2 ft. this impacts the SWR readings significantly
	- What we are looking for is an SWR of less than 1.5 in the range of 144 - 148 MHz the closer you are to 1.0 the better
	- Read more about the [SWR](). (need ref)

---
### Test equipment

We will have a couple of different options to test
#### Nano VNA 

- This is a good relatively modern tool which became popular in the last 5 years. Its a very capable tool which you can do a lot with
- For today they will be set up for you ! look for the following during tuning
	- Make sure you are using `PORT1` when connecting the antenna
	- We are interested in the yellow curve. That shows the SWR between the selected band
	- lower white text indicate what band limits you are currently testing: In the figure it is in the range from 144.000 - 148.000 MHz
	- Yellow upside down triangle(you can use the toggle switch to move around this along the curve): this is one marker and the yellow text at the top gives you the SWR as a number and the corresponding frequency in white text: in this case SWR is 1.02 @ 145.440 MHz
	- NanoVNA's main controls are with the top toggle and it has a touch screen.

- how a well tuned antenna should look
	

---
#### MFJ SWR analyzers

These are some what older but there are usable devices:
- Turn on the device you will see a frequency shown on the LCD
- and the two analog needles show you the SWR and the input impedance
- Turn the dial to move across the band 144 - 148 MHz and look for the dip in the needle. if this is in the center of the band and its < 1.5 your antenna is probably in tune.
- I would still verify using a VNA just to make sure when one is available 

---
### Additional reading 

- Simple indoor installation: When you don't have the option of installing it outside like most of us who are renting apartments you can get a way with hanging this along the wall close to the window. I use a water bottle as a weight and some pins on the wall to hold its shape. have had good results  
- Outdoor installation: people often use a PVC pipe put the whole slim JIm inside and use a different end connector to make it modular. Come talk to us if you want to know more information about this


