# SH1106 OLED Display Driver

![text_example](https://github.com/tomedwa/SH1106_OLED/assets/135190075/2edf90f6-6c05-4618-b33d-63af727c4820)

This is a simple driver for the SH1106 OLED screen. Most of the functions are similar to 
what is found in the various Adafruit libraries for similar components. I have also created 
some custom xbm fonts that work with this library. I used the Peter Fleury i2cmaster.h library
to drive the i2c communication between the atmega328p and the SH1106 screen.


## Features

Quick summary of the main features of this library.

| Feature           | Description |
|---|---|
| Screen rotation   | Rotate the display by a 90, 180, 270 degree clockwise. |
| Text and Images   | Draw text and images on the screen in different orientations. |
| Invert display    | Options to invert the entire display or just a region of the display. |
| Draw shapes       | Draw rectangles and circles on the display (filled or unfilled) |


## Getting Started
Basic example of initialising the screen and drawing a string on the screen.
```
// Initialise i2c
OLED_init();    // Initialise the sh1106 oled screen
OLED_clear_buffer();  // Ensure the oled buffer is cleared when initialised.

// Draw string to the buffer. Position (0, 0), size 16 font, 2 pixel spacing between chars, and normal orientation.
OLED_draw_string("Hello world", 0, 0, 16, 2, 0);

OLED_display_buffer();  // Send the data in the buffer to the display.
```
![hello_word_example](https://github.com/tomedwa/SH1106_OLED/assets/135190075/5e105857-3d99-44c2-98ae-87ad05cdbd66)


## Methods
For descriptions of the methods take a look at the function comments in the SH1106.c file.
