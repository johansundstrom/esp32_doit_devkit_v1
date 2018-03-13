# ESP32 på devkit v1 från DOIT
Först, varför publicerar jag detta? -Jo, för att just de billiga (55 SEK på Banggood) ESP-Wroom-32 utvecklingskorten från t.ex. Banggood.com verkar vilja sälja bort en serie utvecklingskort till förmån för nya serier ellre så rör det sig om piratkopierade utvecklingskort med äkta ESP-chip.

## Vad skiljer?
ESP32 DEVKIT V1 från DOIT har 2x18 pinout (36pin). Just detta kort är obefintligt beskrivet på Internet/Banggood/DOIT. Utvecklingskortet bär ett ESP-WROOM-32 chip som är väldokumenterat. Problemet diskuteras bl.a som ett issue på Github https://github.com/espressif/arduino-esp32/issues/544 senast 3 mars 2018 ock på banggood https://forum.banggood.com/forum-topic-258596.html?page=2. 

## Pin out/Pin map
Problemet handlar om mappningen mellan _pinout_ - allstå anslutsningspinnarna till kortet och ESP32-pinnarna på chipet. Utvecklingskortet från DOIT har 2x15 pins

## Pinout - 2x15 pins versionen
<img src="images/pinoutDOIT32devkitv1.png">
<img src="https://github.com/johansundstrom/esp32_doit_devkit_v1/blob/master/images/esp32-banggod.jpg">


Dokumentationen delas upp i två delar
1. Tech spec på ESP32
2. Tech spec på DevKit V1 från DOIT

## Block Diagram
<img src="images/esp32-block.jpg">

