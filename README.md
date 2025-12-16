# PlatformIO port of the factory demo for the ESP32 S3 Touch LCD 2
This is a working Arduino [PlatformIO](https://platformio.org/) example of the [ESP32 S3 Touch LCD 2](https://www.waveshare.com/wiki/ESP32-S3-Touch-LCD-2) demo `01_factory`. The [current code](https://files.waveshare.com/wiki/ESP32-S3-Touch-LCD-2/ESP32-S3-Touch-LCD-2-Demo.zip) supplied by Waveshare has several pain points to get working with PlatformIO.

This code has very minor tweaks from Waveshare's [supplied code](https://files.waveshare.com/wiki/ESP32-S3-Touch-LCD-2/ESP32-S3-Touch-LCD-2-Demo.zip), and the majority of change lies in the platformio.ini config file.

This repo supplies all required libraries, so it should be the case of cloning, opening vscode and clicking `build` in the platformio extension. Updating versions (specifically major versions of LVGL) will require additional work.

Note: The existing implementation of the factory demo seemed to have an issue regarding `LV_COLOR_16_SWAP`. This was initially set to `1`, causing the camera to display the correct colours, but the UI to display incorrectly. As a result, I've added a quickfix to swap pixels for the camera, allowing the UI to remain unchanged. Due to processing times of this operation, a double buffer was required. 