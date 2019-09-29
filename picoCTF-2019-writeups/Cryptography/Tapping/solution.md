# Tapping
Points: 200

# Category
Cryptography

# Question
Theres tapping coming in from the wires. What's it saying nc 2019shell1.picoctf.com 45168.

# Hint
What kind of encoding uses dashes and dots?
The flag is in the format PICOCTF{}

# Solution

By typing the following command: nc 2019shell1.picoctf.com 45168, we were greeted by a dots and dashes encoding scheme.

![dots](https://user-images.githubusercontent.com/55530196/65829663-3f0bda00-e2da-11e9-84a2-c36ae2a67017.PNG)

Upon researching online, i realised that it was a morse code. Therefore, i used a tool online called: Boxentriq (https://www.boxentriq.com/code-breaking/morse-code) to decode the flag.

![morsecode](https://user-images.githubusercontent.com/55530196/65829729-dc670e00-e2da-11e9-8b38-82ebd6e0edad.PNG)

``` picoCTF{M0RS3C0D31SFUN348887105} ```
