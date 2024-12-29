# Low cost EFHW Build
by KE8TJE - December 2024

End fed half waves are easy to setup antennas and have great performance on multiple bands. An EFHW consists of a impedance transformer which is often called a "ballon".  Having a ready to go EFHW transformer is a good addition for any hams go kit.

You can find multiple build kits and guides online that shows the process of building these. I found the guides usually lacking tuning information/ details that makes the build process easy.

After rewinding the transformer with different methods the following are the main take aways that I got out of the build

- I used gauge 20 wire. I found using one with a thicker outer coating helps in getting a closer impedance to $50  \Omega$ at the end of the antenna 
- Primary winding - Do not twist the wired too tightly. [ARRL guide step 5](https://www.arrl.org/end-fed-half-wave-antenna-kit)
- Windings
	- For a 49:1 
		- using 3 primary turns worked best for me when using a [1002](https://www.digikey.com/en/products/detail/fair-rite-products-corp/2643251002/8594030?gclsrc=aw.ds&&utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Medium%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20223376311_adg-_ad-__dev-c_ext-_prd-8594030_sig-CjwKCAiAg8S7BhATEiwAO2-R6t9dEbFLvC5a-d3NxnAcrBF5lYvRLZYHAjGt_xCcXn2LpeJh433X7RoCockQAvD_BwE&gad_source=1&gbraid=0AAAAADrbLlieBr-7QPR0Ja63U6O5XHhnB&gclid=CjwKCAiAg8S7BhATEiwAO2-R6t9dEbFLvC5a-d3NxnAcrBF5lYvRLZYHAjGt_xCcXn2LpeJh433X7RoCockQAvD_BwE&gclsrc=aw.ds) core
		- 21 total windings are needed.
		- crossing the core at turn 10/11 is fine. This is done to make the output location convenient. Refer [this video](https://www.youtube.com/watch?v=2-4J8ECkoe4&ab_channel=DL2MAN) for more information
	- Testing during building
		- You can use a 2.5 k resister between the ground and the antenna and test the SWR
			- Without the cap attached it should be a quadratic going from 3-30 MHz
				- Change the range of the VNA to 1 per Div.
			- With the cap installed the SWR at Higher frequencies should drop to < 3
	- Pending actual testing
		- SWR readings with a wire goes down to 1:1.01 (20MHz wire I had was too short)

- Materials used
	- 1002 Core: [Digikey](https://www.digikey.com/en/products/detail/fair-rite-products-corp/2643251002/8594030?gclsrc=aw.ds&&utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Medium%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20223376311_adg-_ad-__dev-c_ext-_prd-8594030_sig-CjwKCAiAg8S7BhATEiwAO2-R6t9dEbFLvC5a-d3NxnAcrBF5lYvRLZYHAjGt_xCcXn2LpeJh433X7RoCockQAvD_BwE&gad_source=1&gbraid=0AAAAADrbLlieBr-7QPR0Ja63U6O5XHhnB&gclid=CjwKCAiAg8S7BhATEiwAO2-R6t9dEbFLvC5a-d3NxnAcrBF5lYvRLZYHAjGt_xCcXn2LpeJh433X7RoCockQAvD_BwE&gclsrc=aw.ds)
	- enclosure: [3.3"X2.3"X1.3" box on Amazon](https://www.digikey.com/en/products/detail/fair-rite-products-corp/2643251002/8594030?gclsrc=aw.ds&&utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Shopping_Product_Medium%20ROAS%20Categories&utm_term=&utm_content=&utm_id=go_cmp-20223376311_adg-_ad-__dev-c_ext-_prd-8594030_sig-CjwKCAiAg8S7BhATEiwAO2-R6t9dEbFLvC5a-d3NxnAcrBF5lYvRLZYHAjGt_xCcXn2LpeJh433X7RoCockQAvD_BwE&gad_source=1&gbraid=0AAAAADrbLlieBr-7QPR0Ja63U6O5XHhnB&gclid=CjwKCAiAg8S7BhATEiwAO2-R6t9dEbFLvC5a-d3NxnAcrBF5lYvRLZYHAjGt_xCcXn2LpeJh433X7RoCockQAvD_BwE&gclsrc=aw.ds)
	- 150 pF cap: Might be better to go with a 100 pF

Final build Image 

![](res/Pasted%20image%2020241229181035.png)