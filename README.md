# Neopixel-XL

A 3W Individually Addressable RGB LED similar to Neopixel
---

## Overview

Neopixel LEDs aka **WS2812b** addressable RGB LEDs are very fun to play with because it has integrated driver IC built in which allows us to control tons of such LEDs using **single Data line** from the microcontroller. But if you feel a single WS2812B led isn't bright enough for a certain project then **Neopixel-XL** will fill that gap. 

<p align="center">
<img src="https://github.com/palsayantan/Neopixel-XL/blob/main/3D/3d_preview-removebg-preview.png" width="430px" />
</p>

## Hardware

It consists of a **3W RGB LED**, a **WS2811 LED driver IC** and 3 mosfets with complimentary resistors to boost the week signal from the WS2811 outputs to drive the high power LED. 

It shared the same pinout as the original WS2812B led. And you can also daisy chained them together. But make sure to use a separate power supply that can deliver enough power to drive all these high power LEDs.

| PCB Layout | PCB Footprint |
| :-------------------------: | :-------------------------: |
| ![PCB Layout](https://github.com/palsayantan/Neopixel-XL/blob/main/PCB/PCB_layout-removebg-preview.png)  | ![PCB Footprint](https://github.com/palsayantan/Neopixel-XL/blob/main/PCB/footprint.png)  |

| Schematics | Dimensions |
| :-------------------------: | :-------------------------: |
| ![Schematics](https://github.com/palsayantan/Neopixel-XL/blob/main/Schematic/NeoPixel_XL_sch.png)  | ![Dimensions](https://github.com/palsayantan/Neopixel-XL/blob/main/PCB/Dimentions.png)  |

### Specifications: 

| Parameter | Ratings | Unit
| ---- | ---- | --- |
| Forward Voltage | 5 | V |
| Forward Current | 0.6 | A |
| Peak Current | 0.8 | A |
| Power Consumption | 3 | W |


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

## Where to Buy
<a href="https://www.tindie.com/products/electropoint/neopixel-xl/"><img src="https://d2ss6ovg47m0r5.cloudfront.net/badges/tindie-mediums.png" alt="I sell on Tindie" width="150" height="78"></a>

## [Tutorial video](https://youtu.be/idW8pqdVyIg)
