# Make a Digital Timer!
 
## Overview
For this assignment, you are going to 

A) [Solder your LCD panel](#part-a-solder-your-lcd-panel)

B) [Write text to an LCD Panel](#part-b-writing-to-the-lcd) 

c) [Using a time-based digital sensor!](#part-c-using-a-time-based-digital-sensor)

D) [Make your Arduino sing!](#part-d-make-your-arduino-sing)

E) [Make your own timer](#part-e-make-your-own-timer) 
 

## Part A. Solder your LCD panel

![alt tag](https://github.com/wario123/IDD-Fa18-Lab2/blob/master/IMG_7320.jpg)

## Part B. Writing to the LCD
 
**a. What voltage level do you need to power your display?**

You need 5V to power the display

**b. What voltage level do you need to power the display backlight?**

You need 3.3V to power the backlight
   
**c. What was one mistake you made when wiring up the display? How did you fix it?**

I made the mistake of connecting the K input to power instead of ground. I figured this out with the connectivity test.

**d. What line of code do you need to change to make it flash your name instead of "Hello World"?**

I would need to change the line 'lcd.print('hello, world!')' to 'lcd.print('Karim Arem!')' in the setup function
 
**e. Include a copy of your Lowly Multimeter code in your lab write-up.**

```
// include the library code:
#include <LiquidCrystal.h>

// initialize the library by associating any needed LCD interface pin
// with the arduino pin number it is connected to
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

int analogPin = 0;
int val = 0;

void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // Print a message to the LCD.
  val = analogRead(analogPin);
  lcd.print(val);
  
}

void loop() {
  // Clear the text that was on LCD before and update resistance value
  lcd.clear();
  val = analogRead(analogPin);
  lcd.print(val);
  lcd.noDisplay();
  // Turn off the display:
  delay(500);
  // Turn on the display:
  lcd.display();
  delay(500);
  
}
```


## Part C. Using a time-based digital sensor

[Link to video!](https://www.youtube.com/watch?v=mNHDKDNMGY0&feature=youtu.be)

## Part D. Make your Arduino sing!

**a. How would you change the code to make the song play twice as fast?**

I would change the line 'int pauseBetweenNotes = noteDuration * 1.30;' to 'int pauseBetweenNotes = noteDuration * 1.30/2;'
 
**b. What song is playing?**


## Part E. Make your own timer

**a. Make a short video showing how your timer works, and what happens when time is up!**

**b. Post a link to the completed lab report your class hub GitHub repo.**
