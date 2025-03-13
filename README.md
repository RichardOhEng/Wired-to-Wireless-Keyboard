# Wired-to-Wireless-Keyboard
Turn any wired keyboard wireless (does not support consumer inputs)

A Raspberry Pico W/ pico-sdk based project that turns a wired keyboard wireless. 

DISCLAIMER: This project is not completely finished and is no longer supported by me. The code base is not organized or formatted well.

Uses the pico-sdk's host stack to read HID inputs from keyboards and transmit them using BLE. Do note that it is not able to read consumer inputs as the HID report descriptor for the consumer profile cannot be read dynamically. If you happen to find a solution, please message me! For this project, dedicated buttons would need to be connected to the pico to access consumer functions. There is a workaround to this, and it is currently being sold as "SterlingKey", which sends the report descriptor directly to the Bluetooth host for it to decipher the inputs. However, this program deciphers the HID inputs on the microcontroller, so it is not able to do so. 

Please also note that a Pico W might not be the best MCU for this task, as the power consumption is relatively high. A Pico 2 W, NRF, or ESP32S3 will be more suited for this task as they have deep sleep functions. A NRF or Pico 2 W is likely the best candidate for this type of device. I do not think it is very difficult to transfer the code over especially for the Pico 2 W. 
