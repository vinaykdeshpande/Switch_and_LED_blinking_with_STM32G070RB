# Switch_and_LED_blinking_with_STM32G070RB
This project controls the blinking of an LED on the STM32G070RB board using a tactile switch. Each button press changes how fast the LED blinks.
1.  What This Program Does**
  - **Press the button** to change how fast the LED blinks:
  - **1st Press:** LED blinks every 1 second (0.5 Hz)
  - **2nd Press:** LED blinks every 0.5 seconds (1 Hz)
  - **3rd Press:** LED blinks every 0.25 seconds (2 Hz)
  - **4th Press:** LED turns off
  - After the 4th press, it goes back to the first mode.
  - The button press is detected using an **interrupt**.

2.   Hardware Setup:
  - **LED (PA5)**: The onboard or External LED is connected to PA5.
  - If we want to connec External LED make sure use of registor (330ohm)
  - **Button (PA0)**: The User Button is connected to PA0 and triggers an interrupt.

3. Assumptions Made
- The onboard **LED is on PA5** or the external LED is connected
- The **User Button is on PA0** and uses a pull-up resistor.
- Button debouncing is handled with a **200 ms delay** to prevent false triggers.
