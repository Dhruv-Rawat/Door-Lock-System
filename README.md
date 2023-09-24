<h1> Door Lock System </h1>

This is an Arduino-based RFID Door Lock System project that allows you to control access to a door using RFID cards. It is implemented in C++ and includes functionality for managing an LCD display, RFID cards, LEDs, a buzzer, and a relay for locking/unlocking the door.

<h2> Components Used </h2>
Arduino board (e.g., Arduino Uno)<br>
MFRC522 RFID reader module<br>
LiquidCrystal_I2C display module<br>
LEDs (Green and Red)<br>
Buzzer<br>
Relay module<br>
Push-button switch<br>
RFID cards/tags

<h2> Installation </h2>
Clone or download this repository to your local machine.<br>

Open the Arduino IDE on your computer.

Connect your Arduino board to your computer using a USB cable.

Install the necessary libraries:

<b>MFRC522 library:</b> You can install this library via the Arduino Library Manager.
<b>LiquidCrystal_I2C library:</b> You can install this library via the Arduino Library Manager.

Open the DoorLockSystem.ino sketch in the Arduino IDE.

Make sure you have the appropriate board and port selected in the Arduino IDE under the "Tools" menu.

Upload the sketch to your Arduino board.

<h2> Usage </h2>
Connect the RFID reader module, LCD display, LEDs, buzzer, relay, and push-button switch to your Arduino board as per the wiring diagram.

Power up your Arduino board.

Place an RFID card/tag on the reader.

If the RFID card/tag matches the configured UID (by default, "53 0B 5D 11"), the door will unlock, and the green LED will light up. The LCD display will show "Door Un-Locked," and the buzzer will produce a sound.

If an unauthorized RFID card/tag is detected, the door will remain locked, the red LED will light up, and the LCD display will show "Invalid RFID Tag." The buzzer will produce a different sound.

You can manually unlock the door by pressing the push-button switch.

<h2> Configuration </h2>
<p>
You can configure the following parameters in the DoorLockSystem.ino sketch:

<b>SS_PIN</b> and <b>RST_PIN</b>: Define the pins used for the RFID reader module.<br>
<b>LED_G</b> and <b>LED_R</b>: Define the pins for the green and red LEDs.<br>
<b>BUZZER</b>: Define the pin for the buzzer.<br>
<b>RELAY</b>: Define the pin for the relay.<br>
<b>Btn</b>: Define the pin for the push-button switch.<br>
<b>content.substring(1)</b>: Change the UID value to match the RFID card/tag that should be granted access.
</p>
