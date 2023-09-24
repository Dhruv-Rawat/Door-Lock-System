<h3> Door Lock System </h3>

This is an Arduino-based RFID Door Lock System project that allows you to control access to a door using RFID cards. It is implemented in C++ and includes functionality for managing an LCD display, RFID cards, LEDs, a buzzer, and a relay for locking/unlocking the door.

<h2> Components Used </h2>
Arduino board (e.g., Arduino Uno)
MFRC522 RFID reader module
LiquidCrystal_I2C display module
LEDs (Green and Red)
Buzzer
Relay module
Push-button switch
RFID cards/tags

<h2> Installation </h2>
Clone or download this repository to your local machine.

Open the Arduino IDE on your computer.

Connect your Arduino board to your computer using a USB cable.

Install the necessary libraries:

MFRC522 library: You can install this library via the Arduino Library Manager.
LiquidCrystal_I2C library: You can install this library via the Arduino Library Manager.

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
You can configure the following parameters in the DoorLockSystem.ino sketch:

SS_PIN and RST_PIN: Define the pins used for the RFID reader module.
LED_G and LED_R: Define the pins for the green and red LEDs.
BUZZER: Define the pin for the buzzer.
RELAY: Define the pin for the relay.
Btn: Define the pin for the push-button switch.
content.substring(1): Change the UID value to match the RFID card/tag that should be granted access.
