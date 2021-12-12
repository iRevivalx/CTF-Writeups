# Mem-X
84 Points obtained at that moment

# Category
Web Exploitation

# Question
Do you ever find yourself forgetting about {mem_promo_list_rnd}? Well, you're not alone. That's why we created Mem-X, rigorously designed through hundreds of medical and psychological trials to be the perfect memory preservation system. You can find the Discord bot on the X-MAS CTF server, it is the Mem-X#0493 user.

Start your memory journey today with !help.

Hint: Flag is in /flag.txt

Author: plaaosert

# Solution
I first started of by sending a direct message to the bot with the help of the !help function. 

Upon using the the !help function, i was given only 2 options to retrieve information about the flag as shown below.

![Bot's help function](https://user-images.githubusercontent.com/55530196/145699229-dafc8da4-5e7e-4404-9dcd-f892dd142364.png)

Upon trying out the !note function, i realised that whatever word you typed, it will be automatically converted into hash which does not really provide me much informaton. Therefore, I went on to try a possible !flag function that might contains the flag which turns out showing no results. Upon recalling that this is the web exploitation challenge which i thought that i have to tamper with the bot to recognise the !flag function. To my surprise, i recalled about the hint that the flag is hidden in the /flag.txt which therefore i tried using the !remember function. 

At first, it did not work as i used the command !remember /flag.txt which gives me the output of unable to find the note called **/flag.txt.txt** as shown below.

![Incorrect Flag Output](https://user-images.githubusercontent.com/55530196/145699395-2c33cf93-d8d8-461b-98ff-1afca255e7b0.png)

Therefore, i realised that by removing the **.txt** extension, the bot might give me the output of the flag which it did.

![Correct Flag Output](https://user-images.githubusercontent.com/55530196/145699436-f70e0280-fc9b-4311-8161-35de1b9dbfd9.png)


``` Flag: X-MAS{f0rgEtt1nG_EvEry7h1Ng_abf91b10e019c} ```
