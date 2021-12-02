# Neopixel-XL

*A 3W Addressable RGB LED similar to NeoPixel*

Neopixel LEDs aka **WS2812b** addressable RGB LEDs are very fun to play with because it has integrated driver IC built in which allows us to control tons of such LEDs using **single Data line** from the microcontroller. But if you feel a single WS2812B led isn't bright enough for a certain project then **Neopixel-XL** will fill that gap. 

<img src="https://github.com/palsayantan/Neopixel-XL/blob/main/3D/3d_preview-removebg-preview.png" width="430px" />

It consists of a **3W RGB LED**, a **WS2811 LED driver IC** and 3 mosfets with complimentary resistors to boost the week signal from the WS2811 outputs to drive the high power LED. 

It shared the same pinout as the original WS2812B led. And you can also daisy chained them together. But make sure to use a separate power supply that can deliver enough power to drive all these high power LEDs.

## Specifications: 

- Input voltage : DC 5v 
- Input Current : 1A 
- Power Consumption : 3W 
- Dimension : 20mm x 20mm 
- Shared the same pinout as WS2812 
- Compatible with FastLED library 
- works with any microcontroller

## Getting Started

#### Using [FastLED](https://github.com/FastLED/FastLED) library

```BASH
#include <FastLED.h>
#define NUM_LEDS 1
#define DATA_PIN 4
CRGB leds[NUM_LEDS];
void setup() { FastLED.addLeds<WS2811, DATA_PIN, RGB>(leds, NUM_LEDS); }

void loop() {
  leds[0] = CRGB::Red; FastLED.show(); delay(500);
  leds[0] = CRGB::Black; FastLED.show(); delay(500);

  leds[0] = CRGB::Green; FastLED.show(); delay(500);
  leds[0] = CRGB::Black; FastLED.show(); delay(500);

  leds[0] = CRGB::Blue; FastLED.show(); delay(500);
  leds[0] = CRGB::Black; FastLED.show(); delay(500);
}
````

### [tutorial video](https://youtu.be/idW8pqdVyIg)

### [Buy this Project](https://www.tindie.com/products/electropoint/neopixel-xl/)

### [Follow me on Instagram](https://www.instagram.com/electropoint4u/)
