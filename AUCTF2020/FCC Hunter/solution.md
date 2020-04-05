# FCC Hunter
Points obtained at that point 300

# Category
Signals

# Question
The flag is the frequency used by Auburn University's Tiger Transit system for their radios in each bus. This will also test your OSINT skills.

Flag format: auctf{xxx.xxx} where each "x" is a digit.

Author: JohnsonJangler

# Solution

Since the topic is related to signals, we definitely have to search for a website that is related to it. From this website https://www.radioreference.com/apps/db/?ctid=41 which is the world's largest scanner frequency and radio communications reference source. We are able to successfully locate the frequency used by Auburn's University. 

![FCC Hunter](https://user-images.githubusercontent.com/55530196/78487218-fdbd2100-7779-11ea-90d3-cedafdc30bb4.PNG)

From the image, we just have to look for the frequency that is used by AU Tiger Transit and take the first 6 digit of it to form the flag.

``` Flag: auctf{462.025} ```
