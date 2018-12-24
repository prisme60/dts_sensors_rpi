# dts_sensors_rpi
Source of device tree of raspberry pi (tested on Raspberry pi B 1, for the other rapsberry pi models, perhaps it will need small fixes) for devices:
- HUT21 (humidity and temperature sensor)
- BMP280 (pressure and temperature sensor)
- SSD1306 (OLED display : 128x64)
- LCD_RGB_KEYPAD [Buy on Aliexpress](https://aliexpress.com/item/I2C-IIC-1602-16x2-RGB-LCD-Display-Shield-Blue-Backlight-For-Raspberry-Pi-B-B/32666197091.html) : it uses a GPIO expander (Microchip mcp23017) with 16 GPIOS :
   - 5 GPIOS for the keypad buttons
   - 3 GPIOS for the RBG led
   - 8 GPIOS for the LCD display (hd44780: 16 characters on 2 lines)

 ## Advantage of the device tree over the other source codes that uses userspace libraries on the I2C interface :
- less source code
- less maintenance
- more performance (use kernel modules)
- learn how to use device tree (the future)!
